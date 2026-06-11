# 03. Sales tax nexus

When you need to collect sales tax on SaaS. The rules are jurisdiction-by-jurisdiction and changed dramatically after the 2018 Wayfair decision in the US.

This file covers US states and a brief overview of EU VAT. Operational guidance only; talk to a tax professional once you cross thresholds.

## What "nexus" means

Nexus = connection between your business and a jurisdiction sufficient to require you to collect that jurisdiction's sales tax.

Two kinds:
1. **Physical nexus**: you have an office, employee, or inventory in the state.
2. **Economic nexus**: you have enough revenue or transaction volume in the state, even without physical presence.

For most indie SaaS, economic nexus is the relevant trigger.

## US economic nexus thresholds for SaaS

Each state sets its own threshold. Common patterns:

- $100,000 in sales in the state, OR
- 200 transactions in the state

When you exceed either threshold in a calendar year, you have economic nexus.

Some states use only revenue ($100K, $500K depending on state). Some use only transactions. Some use both (whichever comes first triggers nexus).

A handful of states (California, Texas, New York, others) have higher thresholds, typically $500K.

## Is SaaS taxable?

Depends on the state. As of 2026 (verify current state):

- **Taxable in:** approximately 25 states, including Texas, Washington, Pennsylvania, Connecticut, Massachusetts, New York (depending on type), Iowa, Tennessee.
- **Not taxable:** approximately 18 states, including California, Florida, Illinois, Virginia, North Carolina.
- **Conditional/gray area:** Ohio, Utah, Wisconsin, and others depend on whether your SaaS counts as "data processing", "computer services", or "remote access to software."

**Critical:** rules change. What's not taxable in 2026 may be taxable in 2027. Check current rules per state, especially when you hit nexus.

## What you actually need to do

### Below all thresholds

No action required. Operate normally. Watch your sales by state.

### Approaching a threshold

Track sales by state monthly. Most accounting software (QuickBooks, Stripe Tax) or sales tax tools (TaxJar, Avalara, Anrok) do this.

### When you cross a threshold

Within 30-60 days of crossing:

1. Register for a sales tax permit in the state
2. Start collecting sales tax on all taxable transactions in that state
3. File and remit sales tax to the state (monthly, quarterly, or annually depending on state and volume)

You typically have a grace period after crossing the threshold (usually the next calendar quarter), but don't wait.

### Once you have nexus in 5+ states

Get sales tax automation. Stripe Tax, TaxJar, or Anrok handle:
- Real-time tax calculation per state
- Automated registration
- Filing and remittance

This costs $50-200/month for small operators. The alternative (doing it manually) is hours per state per month.

## EU VAT (and UK VAT post-Brexit)

If you sell SaaS to customers in the EU:

- Below €10,000 in cross-border EU sales: charge VAT at your home country's rate (if EU-based) or no VAT (if non-EU)
- Above €10,000: register for VAT in each EU country you sell to, OR use the "One Stop Shop" (OSS) system to file all EU VAT in one return

For non-EU sellers selling to EU consumers: you should be charging EU VAT from your first euro of sales. The "Non-Union OSS" (IOSS for goods, OSS for services) lets you file one VAT return covering all EU countries.

UK VAT (post-Brexit):
- £85,000 UK revenue threshold for registration
- Above that, register for UK VAT, file quarterly

## What about B2B?

In most jurisdictions, sales to other businesses (B2B) require:
- Collecting the customer's VAT number / sales tax exemption certificate
- Applying reverse charge (B2B in EU) or exemption (US states with proper exemption certificates)

Tools like Stripe Tax handle this automatically if you collect VAT IDs at checkout.

## The "I'll deal with it later" mistake

Common indie pattern: ignore sales tax until you're at $200K ARR, then panic.

Problems with this approach:
- States can collect back taxes for years before you registered (typically 3-7 years lookback)
- Penalties accumulate
- Interest accrues
- Some states impose criminal penalties for willful non-collection (rare but possible)

The right approach: track sales by state from day 1. Register when you cross thresholds. Don't wait.

## What to do right now

Regardless of revenue size:

1. Know which states (or countries) your customers are in. Stripe shows this in the dashboard.
2. Track total sales by state monthly. A simple spreadsheet works at small scale.
3. Set a reminder when any state exceeds $50K (well before the $100K nexus threshold) so you can plan registration.
4. Bookmark the [Streamlined Sales Tax Project](https://www.streamlinedsalestax.org/) site for state-by-state guidance.
5. Consider sales tax automation once you have nexus in 3+ states.

## When to get professional help

- When you first cross nexus in any state
- When you have customers in 10+ states
- When you have EU or international customers
- When you receive a notice from a state department of revenue
- Annually, for a review

Sales tax CPAs and tax compliance specialists cost $1,500-5,000 to set you up, then $200-1,000/month ongoing depending on scale. For most indie SaaS this is overkill until you have nexus in 5+ states.
