# 08. Monthly review

The 30-minute monthly review that keeps your business financially aware. Skip it and you'll be surprised by problems that could have been spotted months earlier.

## When to do it

First week of each month, for the prior month. Schedule it on your calendar; treat it as non-negotiable.

Don't wait until end of quarter. Quarterly reviews catch problems 60 days late.

## The 30-minute checklist

### Minutes 0-5: Cash position

- [ ] Open business checking, business savings
- [ ] Note total cash on hand (excluding tax reserves)
- [ ] Note this month's change vs last month

If cash is decreasing: by how much? Is that intentional or surprising?

### Minutes 5-10: Revenue

- [ ] Pull last month's revenue from Stripe (or your processor)
- [ ] Calculate MRR (monthly recurring revenue) at the end of last month
- [ ] Calculate MRR change vs the previous month
- [ ] Note any unusual one-time revenue

Trend questions:

- Is MRR growing? At what rate?
- Are there refunds eating into gross revenue?
- Are there churned customers you didn't know about?

### Minutes 10-15: Expenses

- [ ] Sum business credit card statement for last month
- [ ] Sum business bank account debits for last month
- [ ] Categorize: fixed vs variable, by type

Trend questions:

- Did expenses spike? Why?
- Are there subscriptions you're not using?
- Are vendor prices increasing?

### Minutes 15-20: Margin and unit economics

- [ ] Calculate gross margin: (revenue - COGS) / revenue
- [ ] Calculate per-customer revenue and per-customer COGS (see file 04)
- [ ] Note customer count and customer count change

Trend questions:

- Is gross margin holding? Improving? Eroding?
- Are heavy users disproportionately driving COGS?
- What's the trend in customer count vs MRR (revenue per customer drift)?

### Minutes 20-25: Tax reserve and runway

- [ ] Calculate YTD profit
- [ ] Calculate tax owed at 25-30% of YTD profit
- [ ] Compare to balance in tax reserve account
- [ ] Move money to tax reserve if behind

Then:

- [ ] Calculate current runway: (cash on hand - tax reserves) / monthly burn
- [ ] Note the runway and compare to last month

Trend questions:

- Is runway growing or shrinking?
- What would runway be if growth slowed 50%? (Use the calculator.)

### Minutes 25-30: Anomalies and decisions

Look at the month overall. Any of:

- Surprise expense?
- Unusual customer activity?
- Subscription you forgot about?
- Refund spike?
- Failed payments not retried?

Note them. Decide whether to act this month or watch for another month.

If anything was concerning enough to act on: write down the action and put a date on it.

## What to track over time

Keep a simple spreadsheet with these monthly values:

| Month | Cash | MRR | Customers | Gross margin | Burn | Runway |
|---|---|---|---|---|---|---|

After 6 months, the spreadsheet shows the actual trajectory of the business, not your gut feeling.

After 12 months, you can see seasonality, growth rate trend, and whether the business is becoming more sustainable.

## What you DON'T need to do monthly

Skip these for the monthly review; do them quarterly or annually:

- Categorize every expense in your accounting software (do it quarterly)
- Reconcile every transaction (do it before tax filing)
- Update your business plan (do it quarterly at most)
- Review investor reporting (you have no investors)
- Strategic planning (do it quarterly)

The monthly review is about awareness and operational adjustments, not strategic planning.

## When the monthly review reveals a problem

Most months, the review is reassuring. Occasionally, something surfaces.

### Problem 1: cash declined more than expected

Possible causes:
- Tax payment hit
- Annual subscription renewal hit
- Refund wave you didn't track
- Reduced revenue you didn't notice mid-month

Action: investigate which one, decide whether it's a one-time event or a trend.

### Problem 2: MRR is flat or declining

Possible causes:
- Net new is being eaten by churn
- A big customer reduced their plan or churned
- Pricing changes weren't accepted by market

Action: pull customer-level data. Identify the specific customers driving the change.

### Problem 3: Gross margin eroded

Possible causes:
- API vendor raised prices
- Power users using more API
- Discounts you offered without raising the bundled tier

Action: drill into per-customer COGS. Find the customers driving the change.

### Problem 4: tax reserve is short

Possible cause: you weren't moving 25-30% per deposit.

Action: catch up immediately. Set up automatic transfer if your bank supports it.

### Problem 5: runway dropped meaningfully

Possible causes:
- Expenses grew faster than revenue
- One-time expense
- Reduced revenue

Action: figure out which. If it's a trend, plan cost cuts. If it's one-time, note and move on.

## Tools that help

You can do the monthly review with:

- Business bank statements (online)
- Stripe dashboard
- A spreadsheet for trend tracking

Optional:
- **Wave / QuickBooks Self-Employed**: pulls bank transactions and categorizes them. Useful at higher transaction volume.
- **Baremetrics / ChartMogul**: SaaS metrics dashboards that calculate MRR, churn, LTV automatically. Useful at $5K+ MRR.

The minimum: bank statements, Stripe, a spreadsheet. Tools are optional until you outgrow the manual process.

## The monthly review as a discipline

This isn't about precision. A monthly review with rough numbers is more valuable than a quarterly review with precise numbers.

The point is awareness. Small problems caught early are small problems. The same problems caught quarterly are crises.

Block 30 minutes on the first Tuesday or Wednesday of every month. Don't skip it.
