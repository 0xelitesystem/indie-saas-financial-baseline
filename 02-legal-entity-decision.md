# 02. Legal entity decision

What legal structure your business uses. The wrong choice creates tax headaches; the right choice protects you and saves money.

## The four options for indie operators (US-centric)

| Entity | When it fits | What it costs |
|---|---|---|
| **Sole proprietorship** | Pre-revenue or very early stage | $0 setup, no separate tax return |
| **Single-member LLC** | Once you have revenue or liability exposure | $50-500 to form (state-dependent), $0-800/year (state-dependent) |
| **S-corporation election (on top of LLC)** | $80K+ net profit annually | LLC costs + payroll setup + accountant ($1500-3000/year extra) |
| **C-corporation** | Raising VC, multiple founders, employees with equity | $500+ to form, more complex tax filing |

If you're outside the US, the equivalents vary. UK: sole trader vs Ltd. Canada: sole proprietor vs corporation. EU: varies wildly by country. The principles below still apply.

## Sole proprietorship

Default. If you start making money without setting anything up, you're a sole proprietor.

**Pros:**
- Zero setup cost
- No separate tax return; report business income on Schedule C of your personal tax return
- Simple

**Cons:**
- Zero liability protection. Business creditors can come after your personal assets.
- Less professional perception (some clients require LLCs or corps)
- No ability to issue equity, take on partners, or build for sale

**When it fits:** the first 3-12 months of validating an idea, before you have revenue or contracts at stake.

## Single-member LLC

Limited liability company with one owner. Most indie SaaS operators end up here.

**Pros:**
- Liability protection: business creditors generally can't reach personal assets
- Simple tax treatment by default (taxed as sole prop, reported on Schedule C)
- Looks more professional than sole prop
- Can be converted to other structures later

**Cons:**
- State-dependent setup cost and annual fees (Delaware: ~$300/year, Wyoming: ~$60/year, California: $800/year minimum)
- Some states require an "operating agreement" (just a written document; templates available)
- You still need to file Schedule C unless you elect different tax treatment

**When it fits:** as soon as you have paying customers, contracts, or any meaningful liability exposure. For most indies, this is month 3-12.

**State to form in:** there are three reasonable choices.

1. **Your home state.** Simplest. You'll operate there anyway. Pay your state's fees.
2. **Wyoming or Delaware.** Lower fees, no state income tax (Wyoming). But you'll still need to register as a "foreign LLC" in your home state if you operate there, which often means paying both sets of fees. Most indie operators don't actually save money this way.
3. **Delaware** is conventional for businesses planning to raise VC funding. Not necessary for indies.

Default: form in your home state. The "Wyoming LLC for privacy" trend is largely overblown for legitimate businesses.

## S-corporation election

This is not a different entity; it's a tax election on top of your LLC (or C-corp). You elect to be taxed as an S-corp by filing Form 2553 with the IRS.

**Pros:**
- Can reduce self-employment tax. As a sole prop or default LLC, all profit is subject to 15.3% self-employment tax. As an S-corp, only your "reasonable salary" is subject to it; remaining profit is distributed as dividends (no SE tax).
- Tax savings can be $5,000-20,000/year for $100K+ profit businesses.

**Cons:**
- Requires running payroll (you pay yourself a salary). Payroll services cost $40-150/month.
- Requires more careful bookkeeping
- "Reasonable salary" is a moving target the IRS scrutinizes. Pay yourself too little and you'll get audited.
- Requires a separate corporate tax return (Form 1120-S)

**When it fits:** when net profit (after expenses, before paying yourself) exceeds about $80K/year. Below that, S-corp savings don't justify the overhead.

## C-corporation

Standard corporate structure. Required if you're raising VC funding or have outside investors expecting equity.

**Pros:**
- Standard for venture funding
- Can issue different share classes (common, preferred)
- Easier to bring on employees with stock options

**Cons:**
- Double taxation: corporation pays tax on profit, shareholders pay tax on dividends
- Complex tax filing
- Annual maintenance requirements (board meetings, minutes)

**When it fits:** if you're raising a priced round, planning to. Otherwise, skip.

## Decision tree for indie SaaS operators

```
Are you raising VC funding?
├── Yes → C-corp (Delaware)
└── No → Continue

Do you have paying customers or significant liability exposure?
├── No → Sole prop is fine for now. Plan to upgrade.
└── Yes → Continue

Is net profit > $80K/year?
├── No → Single-member LLC, taxed as sole prop. Default.
└── Yes → Single-member LLC with S-corp election. Talk to a CPA.
```

## When to revisit

- When you cross $100K revenue (consider S-corp election if not already)
- When you hire your first employee (W-2 vs 1099 implications, payroll setup)
- When you add a co-founder (multi-member LLC, partnership agreement)
- When you take on outside investors (almost certainly need C-corp at this point)
- When you sell the business (asset sale vs equity sale has different tax implications)

## What this section is not

This is operational guidance for choosing among common structures. Not tax or legal advice. The right structure depends on your state, your specific liability profile, and your plans. A 30-minute call with a CPA in your state can save you years of bad decisions.
