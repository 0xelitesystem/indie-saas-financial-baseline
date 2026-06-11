# 09. When to incorporate

When to move from sole proprietorship to LLC, and from LLC to S-corp election. Triggered by revenue, liability, and tax-savings thresholds.

## Sole prop to LLC

### Revenue triggers

There's no revenue threshold that strictly requires an LLC. The decision is about liability and professionalism, not revenue.

Practical guidelines:

- Below $10K annual revenue: sole prop is fine.
- $10K-$50K annual revenue: LLC is increasingly worth the $50-500 setup cost.
- Above $50K annual revenue: LLC is strongly recommended.

### Liability triggers

Stronger reasons to form an LLC, regardless of revenue:

1. **You sign contracts with vendors or customers.** A contract dispute could expose personal assets.
2. **You handle customer data.** A data breach could trigger lawsuits.
3. **Your product makes recommendations or decisions.** Errors in those could create liability (especially in regulated areas: health, finance, legal).
4. **You hire contractors or employees.** Employment disputes are a real risk.
5. **You're storing customer payment information.** Even if Stripe handles it, you're in the chain.
6. **You sell to other businesses.** B2B contracts typically expect an LLC or corp on the other side.
7. **You own physical inventory** (rare for SaaS but possible).

If any of these apply, form an LLC.

### Operational triggers

Even without liability, form an LLC if:

- You want a separate business credit card and bank account (which you should)
- You're worried about commingling personal and business funds
- You need to look "legitimate" to enterprise customers who require formal entity verification

### How to actually form an LLC

In most states:

1. Choose your business name (check state database for availability)
2. File Articles of Organization with the Secretary of State (online; takes 1-7 days)
3. Pay the filing fee ($50-$500 depending on state)
4. Obtain an EIN (Employer Identification Number) from the IRS (free, immediate)
5. Open a business bank account with the EIN
6. Update your Stripe / payment processor with the new entity

Optional (recommended):
- Operating agreement (even for single-member LLCs)
- Registered agent service ($50-150/year; required in most states)
- Local business license (if your city/county requires one)

This is a one-day project most weeks.

## LLC to S-corp election

S-corp is not a different entity; it's a tax election that changes how your LLC is taxed. You file Form 2553 with the IRS to make the election.

### Profit triggers

S-corp election makes sense around **$80K-$100K net profit per year**.

The math: as a sole prop or default LLC, all profit is subject to 15.3% self-employment tax. As an S-corp, only your "reasonable salary" is subject to SE tax; the remaining profit is distributed as dividends, not subject to SE tax.

At $80K profit, switching to S-corp typically saves $4,000-7,000 in SE tax annually, net of the additional overhead.

Below $80K profit, the S-corp savings don't justify the overhead. Above $200K profit, savings can be $15,000-30,000 annually.

### What S-corp election requires

The overhead:

1. **Payroll setup.** You must pay yourself a "reasonable salary" through payroll, with all the required withholdings (income tax, FICA, etc). Payroll services cost $40-150/month.
2. **Separate corporate tax return.** Form 1120-S, plus K-1 to yourself. CPA cost increases by $500-2000/year.
3. **More careful bookkeeping.** Owner draws vs salary vs dividends must be tracked separately.
4. **"Reasonable salary" decision.** The IRS scrutinizes this. Pay yourself too little and you risk an audit. The rough rule: pay yourself what you'd pay an employee to do your job in your market, then distribute the rest as dividends. Typically 40-60% of total compensation as salary.

### When NOT to elect S-corp

- Below $80K net profit: not worth the overhead
- If you have employees with equity: might complicate things
- If you're planning to raise venture funding: you'll convert to C-corp anyway
- If you're outside the US: S-corp is US-specific

### How to elect

1. Decide with your CPA whether S-corp election makes sense
2. File Form 2553 with the IRS by March 15 of the year you want it to apply
3. Set up payroll (most CPAs help with this; or use Gusto, Justworks, etc)
4. Adjust your bookkeeping to track salary vs distributions

## LLC to C-corporation

You only need to convert to C-corp if you're raising venture capital or have multiple founders expecting different equity classes.

Indie operators almost never need this. Skip unless:

- You're raising a priced round (Series A or beyond)
- You want to issue stock options to employees
- You have international co-founders requiring different shareholder rights
- You're being acquired and the acquirer requires C-corp

C-corp conversion has tax consequences and should be done with a lawyer.

## Hiring triggers

Hiring your first person changes things regardless of entity:

### Hiring a contractor (1099)

You can hire a contractor as a sole prop or LLC. No additional entity changes needed.

Required:

- Form W-9 from the contractor before they start
- Form 1099-NEC at year-end if you paid them $600+
- Track contractor payments separately in your accounting

Contractors are simpler than employees but you must actually treat them like contractors:

- They control how the work gets done (you specify outcomes, not methods)
- They use their own tools and equipment
- They're not full-time exclusively for you
- They invoice you; you don't put them on a regular pay schedule

Misclassifying employees as contractors is a major IRS risk. Talk to a CPA if unsure.

### Hiring an employee (W-2)

Hiring an employee is a bigger step. You need:

- An EIN (you have one as an LLC already)
- State employer registration in the state where the employee works
- Payroll service to handle withholdings and quarterly tax filings
- Workers' compensation insurance (state-dependent)
- Unemployment insurance registration
- Possibly: health insurance offerings (depending on state and company size)
- Liability insurance for employment-related claims

Total setup cost for first employee: 1-2 weeks of work, $1,500-3,000 in setup and first-year compliance costs.

Most indie SaaS operators never hire W-2 employees. Contractors and offshore teams scale further before needing full-time US employees.

## When to revisit your structure

Annually, in October or November (before year-end tax planning):

- Did you cross any revenue or profit thresholds this year?
- Have you taken on new liability (new contracts, new product surface)?
- Are you hiring next year?
- Are you considering selling?

If any answer is meaningful, schedule a 30-60 minute consultation with a CPA. The fee ($150-400) pays for itself if the structure recommendation prevents a tax surprise.
