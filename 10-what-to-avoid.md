# 10. What to avoid

Patterns that cause financial damage to indie SaaS operators. Each is common; each is preventable.

## 1. Commingling personal and business funds

The most common mistake. Already covered in file 01.

What it looks like:
- Personal credit card paying for business expenses "I'll reimburse myself later"
- Business revenue deposited into personal checking
- Personal Venmo used to collect business payments
- Buying personal items with the business card

Why it matters:
- Loses LLC liability protection (piercing the corporate veil)
- Makes tax filing inaccurate or impossible
- Triggers audit risk
- Creates legal exposure in disputes

Fix: separate accounts from day one. If you've already commingled, untangle now. Set up the right accounts and never go back.

## 2. Late tax filings

Sole prop or single-member LLC tax returns are due April 15 with personal returns. S-corp returns are due March 15. Penalties for late filing: 5% per month of the unpaid tax, capped at 25%.

What it looks like:
- "I'll deal with taxes when I have time"
- Filing extensions every year without solving the underlying problem
- Owing taxes you didn't reserve for

Fix: 
- Engage a CPA by November of the year you're filing for
- Have all bank statements and expense categorizations ready by January
- File before the deadline. Extensions push the filing date but not the payment date.

## 3. Underpayment of estimated tax

Already covered in file 07. Underpayment penalty is 5-8% annualized on the shortage.

Fix: pay quarterly estimated tax. Set up calendar reminders. Use the safe harbor (pay 100% of last year's tax, or 110% if AGI > $150K) if you don't want to project current year income.

## 4. Ignoring sales tax until audit

Already covered in file 03. Some states can collect back taxes 3-7 years.

Fix: track sales by state from day 1. Register and start collecting when you cross nexus.

## 5. Not setting aside taxes

Already covered in file 07. The most common cash flow disaster.

Fix: 25-30% of every revenue deposit moves immediately to a separate tax reserve account. Automate if possible.

## 6. Buying customers with promotions you can't sustain

What it looks like:
- "First 6 months 70% off!" without modeling what happens at month 7
- Lifetime deals priced below your COGS at scale
- Free tier that costs you real API money

Fix: model the unit economics before launching any promotion. If the customer never becomes profitable, the "acquisition" is just a loss.

A 70% discount that converts to full price in month 7 is fine IF you can survive the discount period. A 70% discount where customers churn at month 7 because they were never going to pay full price is a bad deal.

## 7. Subscriptions you forgot you have

Every indie operator has them. The $19/month tool you signed up for 18 months ago and haven't used. The annual subscription that auto-renewed and you didn't notice.

What it looks like:
- Stripe statement showing $200-500/month in software you don't recognize
- Multiple tools doing the same thing (two project management tools, three writing tools)
- "Lifetime deals" on AppSumo that you never use

Fix:
- Quarterly: list every subscription. Cancel any you haven't used in 60 days.
- Use a tool like Truebill (now Rocket Money) or just a spreadsheet to track recurring charges.
- Before any new subscription: check whether something you already pay for does the job.

## 8. Buying premium tools too early

What it looks like:
- Paying for QuickBooks Online ($30-200/month) when you have 20 transactions a month
- Subscribing to enterprise analytics tools at $300+/month when you have 50 customers
- Buying "founder coaching" before you have product-market fit

Fix: use the free or simplest paid tier of any tool until you're clearly outgrowing it. Premium features that "would be nice" rarely deliver enough value to justify the cost at small scale.

## 9. Not raising prices

Most indie SaaS operators charge less than the market would pay.

Signs you're underpricing:
- Customers say "this is too cheap to be true"
- No one asks for discounts
- Conversion rate from trial is over 30% (indicates the price was a no-brainer)
- You spend support time on people whose subscription doesn't justify the time

Fix: raise prices on new customers periodically. 10-25% raises every 6-12 months are normal. Grandfather existing customers if you want to.

The trap: not raising prices ever because "what if customers leave." Some will. The math usually works out positive because the customers who stay paying more cover the lost revenue from the few who leave.

## 10. Hiring before you can afford it

What it looks like:
- Hiring a full-time employee at $80K when your revenue is $5K/month
- Hiring multiple contractors when your processes aren't documented
- Promising salary that requires growth you haven't proven yet

Fix: hire contractors for specific, defined tasks before hiring full-time. Confirm the contractor relationship works for 3-6 months before considering full-time. Confirm the revenue can support the hire for 12 months before committing.

## 11. Borrowing against the business

What it looks like:
- Personal loan to cover business losses
- Credit card debt accumulated on business card
- "Friends and family round" without paperwork

Fix:
- If the business needs more capital than it generates, the right answer is usually to cut costs, not borrow.
- If you must borrow, do it formally (a documented loan with terms) and pay it back like a real obligation.
- Avoid personal guarantees on business debt where possible (this defeats the LLC protection).

## 12. Selling the business badly

What it looks like:
- Accepting the first offer without understanding the multiple
- Selling without involving a lawyer or M&A advisor
- Asset sale when an equity sale would be better (or vice versa)
- Earn-outs you don't trust the buyer to honor

Fix: if you're seriously selling, hire an M&A advisor and a lawyer. Even at small scale ($500K-$2M business sales), professional help pays for itself in better terms.

Typical SaaS multiples in 2026:
- Profitable, growing 30%+: 4-6x ARR
- Profitable, growing 10-30%: 2-4x ARR
- Profitable, flat: 1-2x ARR
- Not profitable: based on revenue and unit economics

If someone offers you 1x ARR for a growing business, they're significantly underpaying. Negotiate or wait.

## 13. Not tracking gross margin

If you don't know your gross margin per customer (and overall), you can't make pricing decisions. You'll continually undercharge for high-cost customers and lose money on them.

Already covered in file 04. The minimum: monthly review includes gross margin calculation.

## 14. Spending on conferences and travel that don't return

Conferences are seductive. The case for going is usually "I'll meet customers and partners." The reality: most conferences produce 0-3 useful contacts for indie operators.

Cost: $1,500-5,000 per conference (registration + travel + lodging + time).

Fix: budget total conference spending annually. Pick conferences with specific outcomes in mind. Skip the ones that are mostly networking with no clear ROI. Track whether each conference produced revenue within 6 months.

## 15. Letting accounting fall behind

If your bank statements are unreconciled for 6+ months, you don't actually know your numbers.

What it looks like:
- Behind on QuickBooks categorization
- Mixing personal and business expenses on the books (even if accounts are separate)
- No idea what last month's profit was without 3 hours of work

Fix:
- Categorize transactions weekly (10 minutes) or biweekly (20 minutes)
- Use the monthly review (file 08) to catch issues
- Hire a bookkeeper if monthly reconciliation takes more than 1 hour ($150-400/month at small scale)

## 16. Accepting bad customers

Some customers cost more than they pay:

- Constant support requests despite a low-tier subscription
- Heavy API usage on a flat-rate plan
- Chargebacks and refund requests
- Demanding features you don't want to build

Fix: identify your worst 5% of customers each quarter. Consider whether to:
- Raise their price
- Move them to a higher tier
- Discontinue serving them (refund and cancel)

Indie SaaS often loses money on the bottom 10% of customers. Cutting them improves the business.

## The pattern across all of these

The common thread: small problems caught early are small. The same problems caught months later are crises.

The monthly review (file 08) catches most of these. Set up the review. Do it. The 30 minutes saves multiple hours and thousands of dollars over a year.
