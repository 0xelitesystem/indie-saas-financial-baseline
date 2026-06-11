# 01. Separate accounts

Set this up before doing anything else. Mixing personal and business finances is the most common indie founder mistake. It causes tax problems, legal problems, and operational confusion.

## What to set up

Three accounts, minimum:

1. **Business checking account** - for revenue and operating expenses
2. **Business credit or debit card** - for purchases that need to flow through the business
3. **Business savings account** - for tax reserves and runway

These can be at any bank. Mercury, Relay, Novo, and Wise are popular with indie operators. Chase, Bank of America, and other traditional banks also work, often with stricter account-opening requirements.

## What "separate" means

- Business revenue lands in the business checking account, never your personal account
- Business expenses are paid from the business account, never your personal card
- When you pay yourself, you do a deliberate transfer from business to personal (an "owner's draw" if you're a sole prop or single-member LLC, payroll if you're an S-corp)
- Personal expenses never go through the business card, even if you'll pay yourself back later

The principle: every transaction belongs to either the business or you, and there's no ambiguity which.

## Why this matters

### Tax reasons

If business and personal funds mix, the IRS treats your business as suspicious. In an audit, you'd need to prove which transactions were business vs personal. With mixed accounts, that's impossible. With separate accounts, your business bank statement is the source of truth.

### Legal reasons

If you're an LLC: mixing funds is called "piercing the corporate veil" and removes your liability protection. The whole point of an LLC is that business creditors can't come after your personal assets. If you mix funds, a court can rule the LLC was a fiction and your personal assets are exposed.

### Operational reasons

When you can see only business transactions in one place, you can:
- Tell whether the business is profitable this month
- Spot duplicate subscriptions
- Catch fraud quickly
- Know your runway without doing mental math

## What about Stripe / payment processors

Stripe (or similar) deposits revenue into one bank account. That bank account should be your business checking, not your personal account.

When you set up Stripe, the bank account you connect is the bank account that receives every cent of revenue. Get this right at setup; changing it later is annoying.

## What about expenses paid by mistake from personal funds

It happens. You're at a coffee shop, you're using your personal card on file, you pay for a business book. The fix:

1. Log it as a "reimbursable" item in your accounting
2. At month-end, your business writes a check to you (or transfers via the business bank) to reimburse
3. Document what was reimbursed and what the business purpose was

Do this rarely. Treating personal funds as a backup business card defeats the point of separation.

## The minimum starter setup

For an indie SaaS at $0-50K ARR, you need:

| Account | Purpose | Approximate balance |
|---|---|---|
| Business checking | Operating | 1-3 months of expenses |
| Business savings | Tax + runway | 25-30% of revenue (tax reserve) + 3-6 months of expenses (runway buffer) |
| Business card | Subscriptions, ads, contractor payments | Pay off monthly |

You do not need: multiple business checkings, a "merchant account" beyond what Stripe provides, business loans, lines of credit. These are scaling problems, not starter problems.

## When to add accounts

Add a separate account when there's a clear reason:

- **Sales tax escrow** (if you're collecting sales tax): a dedicated account holding collected sales tax until remittance. Keeps it separate from operating funds.
- **Profit account** (per Profit First methodology): a savings account where you sweep a fixed percentage of revenue every month. Forces profitability.
- **Foreign currency holding** (if you have significant non-USD revenue): a Wise or similar multi-currency account.

Each additional account is operational overhead. Don't add complexity until the simpler setup is genuinely insufficient.
