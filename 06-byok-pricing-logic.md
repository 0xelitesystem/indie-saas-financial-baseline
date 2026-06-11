# 06. BYOK pricing logic

When BYOK (bring your own key) pricing is the right model, when bundled is right, when hybrid is right. The math behind the choice.

## What BYOK means

In a BYOK model, your customer brings their own API key for the underlying service (LLM, third-party API, etc) and you charge them for the platform/wrapper.

Example: You build a tool that uses Anthropic's API. Instead of charging $29/month bundled, you charge $9/month and require the customer to provide their own Anthropic API key. They pay Anthropic directly for the usage.

## The economic argument for BYOK

Bundled SaaS pricing puts API variability on you. If a heavy user costs $30/month in API, and you charge $29/month bundled, you lose money on them.

BYOK puts API variability on the customer. You charge a thin platform fee and your COGS becomes nearly zero.

This matters when:

1. **API costs are high relative to your price.** If API cost averages 5% of revenue, BYOK doesn't help much. If it's 40%+, BYOK transforms your margin.

2. **Usage varies dramatically across users.** A few power users consuming 10x the API cost of average users would cripple bundled pricing. BYOK lets you serve them without margin damage.

3. **Customers are sophisticated enough to manage API keys.** Developer tools, technical SaaS, productivity tools for technical professionals. Not consumer tools.

## The friction argument against BYOK

BYOK adds onboarding friction. Customers must:
- Sign up at the API provider (OpenAI, Anthropic, etc)
- Add a payment method to the API provider
- Generate an API key
- Paste it into your tool

Each step is 5-15% drop-off. Total drop-off can be 30-50% compared to a bundled signup.

For some audiences, this friction is acceptable (developers, technical users). For others, it's a non-starter (general SMB, consumers).

## When bundled is right

Bundled is right when:

- API cost is a small percentage of revenue (<20%)
- Usage is relatively predictable per customer
- Customer onboarding sensitivity is high (consumer or non-technical)
- You can absorb variability in margin

Examples:
- Chat tools for non-technical teams ($20-50/mo per seat)
- Document-processing tools for SMB
- Most B2C AI products

## When BYOK is right

BYOK is right when:

- API cost is large percentage of revenue (>30%)
- Usage varies dramatically (power users vs casual users)
- Customer audience is technically sophisticated
- You want minimal margin volatility

Examples:
- Developer tools that call LLMs
- Power-user automation tools
- Technical productivity tools where the audience knows what an API key is

## When hybrid is right

Hybrid: small base price for the platform + BYOK for the API. Best of both, complicated.

Hybrid is right when:

- You have an audience mix (some power users, some casual)
- You want predictable base revenue plus elastic scaling
- Onboarding sophistication varies

Hybrid is wrong when:

- The math doesn't justify the complexity (you save 5% margin for 3x more pricing-page words to explain)
- Customer support cost increases due to confusion about what's included

## The decision matrix

| Factor | BYOK favored | Bundled favored |
|---|---|---|
| API cost as % of price | Above 30% | Below 20% |
| Usage variability | High | Low |
| Audience sophistication | Technical | General |
| Conversion sensitivity | Low (people will jump through hoops) | High |
| Margin priority | Margin > volume | Volume > margin |
| Operational simplicity | More important | Less important |

If you score 3+ on "BYOK favored", lean BYOK.
If you score 3+ on "Bundled favored", lean bundled.
Mixed score: consider hybrid.

## How to price BYOK

Don't undersell. The most common BYOK mistake is pricing too low because "the API is paid separately, so my price is just for the wrapper."

The wrapper has real value:
- UI and workflow
- Caching and request optimization
- Error handling and retry logic
- Customer support
- Updates as APIs change

Price BYOK at $5-15/month for hobbyist tools, $19-49/month for prosumer tools, $49+ for B2B.

Compare to the price of bundled equivalents in your category and undercut by 40-60%, because the customer is taking on the API cost.

## How to price hybrid

Hybrid base price covers your fixed costs (infra, support, baseline). API usage is BYOK.

Example: $19/month base + your own Anthropic key.

The base price should cover infrastructure per user (typically $1-3/user/month) + processor fees + a contribution to fixed costs and profit. For most indie SaaS, $15-25/month base is the sweet spot.

## Migration: bundled to BYOK

If you're currently bundled and considering switching:

1. **Don't force existing customers to BYOK.** Grandfather them. The friction will cost you customers who were happy with bundled.

2. **Offer BYOK as a new tier.** "Pro Bundled" at $X and "Pro BYOK" at $Y, where Y is significantly lower.

3. **Communicate the tradeoff honestly.** "Pro BYOK costs less because you pay the API directly. Pro Bundled costs more because we handle that."

4. **Track conversion rates per tier.** If BYOK conversion is significantly worse, accept that and price-anchor against the bundled tier.

## Common BYOK mistakes

### Mistake 1: storing customer API keys insecurely

If you accept API keys, you must encrypt at rest, never log them, rotate them periodically, and provide a way for customers to delete them.

See companion repo `byok-security-checklist`.

### Mistake 2: pricing as if the wrapper is free

The wrapper has costs and value. Don't price BYOK at $3/month because "we just call the API." You have infrastructure costs, support costs, and intellectual property.

### Mistake 3: not testing customer ability to set up

The first 5-10 BYOK signups will struggle to add their API key. Watch them (with permission), see where they get stuck, fix the onboarding.

### Mistake 4: charging recurring for a one-time setup

Some tools could be one-time purchases if BYOK (the user owns the wrapper, the API cost is theirs). Consider this for low-touch tools.

## The math: when does BYOK save you money

Quick check: if (API cost per user) > (revenue per user × 30%), BYOK saves you significantly. If API cost is 10-30% of revenue, BYOK saves moderately. Below 10%, BYOK's friction probably costs more than it saves.

For a more thorough analysis, use the `indie-saas-pricing-calculator` companion tool.
