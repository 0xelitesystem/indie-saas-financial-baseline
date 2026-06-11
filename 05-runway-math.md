# 05. Runway math

How to calculate runway honestly. Most founders compute runway with overly generous assumptions and run out of money sooner than they think.

## The basic runway calculation

```
runway_months = cash_on_hand / monthly_burn_rate
```

Where:
- `cash_on_hand` = liquid funds available in the next 90 days
- `monthly_burn_rate` = monthly expenses minus monthly revenue

If you have $30,000 cash and your monthly burn is $5,000, you have 6 months of runway.

This is the high-school version. Below is the actual version.

## What counts as cash on hand

Include:
- Business checking and savings balances
- Funds available within 30 days from any source (open invoices that will pay in 30 days, etc)

Exclude:
- Tax reserves (you don't actually own this money)
- Credit lines (using these is debt, not runway)
- Loans you "might" be able to get
- Future revenue you "expect"
- Money in personal accounts unless you've committed to putting it into the business

The principle: cash on hand means cash you can actually spend in the business this month.

## What counts as burn

Burn rate is total monthly expenses minus monthly revenue.

Total monthly expenses:
- Fixed costs (salaries, rent, recurring subscriptions, hosting baseline)
- Variable costs (API costs scaling with usage, contractor work, advertising, transaction fees)
- One-time costs amortized (legal setup, tools purchased outright)

Monthly revenue:
- MRR after refunds
- Minus payment processor fees (these are real costs)
- NOT including expected revenue you haven't earned

## The mistakes founders make

### Mistake 1: counting tax reserves as runway

You owe ~25-30% of profit to the IRS. That money is the IRS's, not yours. If you include it in runway, you'll be short on tax payment day.

Set aside tax reserves in a separate account. Don't include them when calculating runway.

### Mistake 2: counting future revenue

"We have $40K in our checking, and we expect to make $5K/month, so we have effectively $X months of runway." This is wrong.

Runway calculations should be based on what you have, not what you expect. Use sensitivity analysis (the `breakeven-runway-calculator` companion tool) to model scenarios with different growth rates.

### Mistake 3: smoothing burn over the year

Burn varies. Annual subscriptions hit certain months. Conferences and travel are seasonal. Hiring increases burn the moment you do it, not when revenue grows.

Calculate burn on the worst likely 3 months, not the trailing average.

### Mistake 4: counting personal savings

Unless you've made a hard commitment to put $X into the business if needed, your personal savings are not runway. They're an option you might exercise if things go badly.

Keep personal and business separate in mental accounting as well as in the bank.

## Honest runway calculation

```
honest_cash = checking_balance + savings_balance - tax_reserves - committed_outflows_next_90_days
honest_burn = (last_3_months_expenses_sum / 3) - (last_3_months_revenue_sum / 3)
honest_runway = honest_cash / honest_burn
```

Where:
- `tax_reserves` = 25-30% of YTD profit (or whatever your CPA says)
- `committed_outflows_next_90_days` = annual subscriptions, taxes due, vendor invoices already accrued

This number is shorter than the "rosy runway" most founders carry in their heads. It's also the number that matters.

## Sensitivity: what if growth slows?

Runway calculations should account for the case where growth slows. If your runway assumes 15% MRR growth per month and the actual growth is 5%, runway shortens significantly.

The `breakeven-runway-calculator` tool computes runway at 100%, 75%, 50%, and 25% of your assumed growth rate. Use it monthly.

If your runway at 50% growth is too short, you're depending on growth that may not materialize. Either:
- Cut burn now
- Raise (if you're VC-backed)
- Charge more
- Accept that the business will need to break even sooner

## Cash flow vs runway

Cash flow is the rate of change of cash. Runway is the projection forward.

You can have positive cash flow (revenue > burn) and still have a runway problem (cash is low, growth is brittle).

You can have negative cash flow (burn > revenue) and not have a runway problem (cash is high, growth is high enough that breakeven is in sight).

Track both. They're different metrics.

## What to do at different runway levels

| Runway | What it means | What to do |
|---|---|---|
| 24+ months | Comfortable | Focus on growth and improving metrics |
| 12-24 months | Standard for bootstrappers | Build the buffer toward 18+ months |
| 6-12 months | Getting tight | Cut non-essential costs, push revenue activities |
| 3-6 months | Concerning | Aggressive cost cutting, scenarios for revenue acceleration |
| 0-3 months | Crisis | All hands on deck: secure cash via revenue, financing, or shutdown decisions |

The right time to act on shortening runway is when it crosses 6 months, not 3. By 3 months, options are limited and decisions are forced.

## Tracking runway

Update your runway number monthly. Add it to your monthly review (see 08). Track it over time so you see the trend, not just the current number.

A runway number that's slowly increasing month over month means the business is heading toward sustainability. Decreasing means the opposite. Flat means you're treading water; not failing but not progressing.

The runway trend matters more than the absolute number.
