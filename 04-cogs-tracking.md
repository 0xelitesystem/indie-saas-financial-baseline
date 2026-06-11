# 04. COGS tracking

Cost of Goods Sold (COGS) for SaaS, especially AI-cost-heavy SaaS. Without per-user COGS visibility, you don't know if you're profitable per customer.

## What counts as COGS for SaaS

COGS = costs that scale directly with usage or customer count.

For an indie SaaS:

- **API costs** (OpenAI, Anthropic, third-party APIs you call per request)
- **Infrastructure that scales per user** (per-seat licensing for tools you pass through, storage for user data, bandwidth for serving user content)
- **Payment processor fees** (2.9% + 30¢ for Stripe, etc)
- **Per-user third-party services** (if your product includes a per-user license to another tool)
- **Support cost per customer** (if you have a support contractor paid per ticket)

What is NOT COGS:

- Your own time and salary
- Marketing costs
- Office and equipment
- General SaaS subscriptions you use to run the business
- Domain and email hosting
- One-time setup costs for the business

These are operating expenses, not COGS. The distinction matters for understanding unit economics.

## Why this matters for AI-cost-heavy SaaS

If your product calls OpenAI, Anthropic, or similar APIs on behalf of users, your API cost can easily exceed 30-60% of revenue per user. That's much higher than traditional SaaS (typically 5-15% COGS).

If you don't track this:

- You might price at $19/month with $14/month of API costs (74% COGS)
- You think you're at 81% gross margin (industry-normal SaaS)
- You're actually at 26%
- Your unit economics break and you don't know why

## The minimum COGS tracking

For each paying customer, track per month:

| Item | Source |
|---|---|
| API cost | Vendor dashboard (OpenAI, Anthropic, etc) with usage tagged by customer |
| Infrastructure cost per user | Allocated portion of total infra cost (total infra ÷ active users) |
| Processor fee | Stripe dashboard shows fee per transaction |
| Per-user third-party | Direct from vendor or your own log |

Sum these per customer; that's their COGS. Customer revenue minus COGS = gross profit per customer.

## How to tag API usage by customer

Two approaches:

### Approach 1: Tagged API calls (best)

Most major LLM APIs support metadata tagging on requests. With Anthropic and OpenAI:

```python
# OpenAI - user parameter for tracking
response = client.chat.completions.create(
    model="gpt-4o",
    messages=[...],
    user="customer_12345"  # tagged for per-user attribution
)

# Anthropic - metadata parameter
response = client.messages.create(
    model="claude-opus-4-7",
    messages=[...],
    metadata={"user_id": "customer_12345"}
)
```

Then in the vendor dashboard or via the usage API, filter usage by user_id.

### Approach 2: Track at your application layer

Log every API call with: customer_id, model, input_tokens, output_tokens, cost (calculated from model pricing).

This works if you control the API call path. Store in a usage table:

```sql
CREATE TABLE api_usage (
    id BIGSERIAL PRIMARY KEY,
    customer_id INTEGER NOT NULL,
    timestamp TIMESTAMPTZ DEFAULT NOW(),
    model TEXT NOT NULL,
    input_tokens INTEGER,
    output_tokens INTEGER,
    cost_usd DECIMAL(10, 6),
    request_id TEXT
);
```

Sum cost_usd by customer_id by month. That's their API COGS.

## Operating metrics derived from COGS

Once you have per-customer COGS, you get:

### Gross margin per customer

```
gross_margin = (revenue - cogs) / revenue
```

Healthy SaaS targets 70-85%. AI-heavy SaaS often runs 50-70% (acceptable). Below 40% per customer is a problem.

### Contribution margin (gross margin minus variable acquisition cost)

```
contribution = (revenue - cogs - cac_amortized_per_month) / revenue
```

This tells you whether the customer is profitable when their acquisition cost is amortized over their expected lifetime.

### Pareto check

What percentage of your COGS comes from your top 10% of users? If it's over 50%, you have power-user economics: a few users are subsidized by everyone else.

Either: charge those users more (usage-based or BYOK), or accept the subsidy as a marketing cost.

## Monthly COGS review

Once a month:

1. Pull total revenue from Stripe
2. Pull total API costs from each vendor dashboard
3. Pull total infrastructure costs from your hosting bill
4. Pull total processor fees from Stripe
5. Calculate aggregate COGS: API + infra (% allocated) + processor fees
6. Calculate aggregate gross margin
7. Compare to last month

If gross margin is dropping month-over-month for 2+ months, investigate:

- Heavy users using more API (check the Pareto)
- Vendor price increases
- Customer mix shifting toward smaller customers (lower revenue per customer = same COGS = lower margin)

## What to do if margin is bad

### Option 1: Raise prices

Easiest. Raise prices on new customers. Grandfather existing customers if you want to.

### Option 2: Add a usage cap

Bundled pricing with a usage cap: "$29/month includes 1,000 API calls". Above that, charge per call or downgrade service.

### Option 3: Switch to BYOK

Customer pays the API vendor directly. You charge a thin platform fee. See `06-byok-pricing-logic.md`.

### Option 4: Reduce variable cost

- Switch to a cheaper model (GPT-4o-mini instead of GPT-4o for some tasks)
- Cache aggressive (cache identical requests within a time window)
- Compress prompts (shorter system prompts = lower input tokens)
- Use prompt caching (Anthropic) or batch APIs (cheaper rate for non-real-time work)

### Option 5: Accept lower margin if LTV justifies it

Sometimes margins are low but lifetime value is high (customer stays 5+ years). LTV/CAC math may still work. But this requires actual data, not hope.

## What "infrastructure cost per user" means

Total infrastructure bill (hosting, DB, storage, bandwidth) divided by active users.

If your AWS bill is $400/month and you have 100 active users, infrastructure per user is $4/month.

This rises with scale at small numbers (you're paying for capacity you don't use) and falls at larger numbers (the bill grows slower than user count). At 1000 users with the same $4/user, infra cost is $4000/month, but realistically you'd be at $1-2/user at that scale.

Track infrastructure per user monthly. If it's not declining over time, you have an efficiency problem.
