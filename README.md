# Marketing Campaign Attribution

Analyzes which purchase channels and past marketing campaigns actually performed, using
real customer-level purchase and campaign-response data.

## Problem
A company runs campaigns and sells across web, catalog, in-store, and deals-driven channels but
doesn't have a clear read on which channels and campaigns are actually working. This turns raw
customer purchase and campaign-response data into a channel and campaign performance breakdown.

## What It Does
- Treats each purchase channel (web, catalog, store, deals) as a comparable unit and totals
  purchase volume and share across them
- Computes acceptance rate for every past marketing campaign plus the most recent one
- Breaks channel usage down by income bracket to spot non-obvious spending patterns
- Exports channel totals, campaign acceptance rates, and the income-bracket breakdown for a BI
  dashboard

## Real Results (real dataset, 2,205 customers)
- **Channel split:** in-store still dominates at **39.1%** of purchases, web is a strong second
  at **27.5%**, catalog and deals trail at **17.8%** and **15.6%**
- **Campaign performance:** the most recent campaign (`Response`) hit a **15.10%** acceptance
  rate -- more than double the best-performing prior campaign (`AcceptedCmp4` at **7.44%**), and
  one earlier campaign (`AcceptedCmp2`) badly underperformed at just **1.36%**
- **Counter-intuitive finding:** deal-driven purchases peak in the **middle** income bracket
  (3.07 deals/customer on average), not the top -- high-income customers buy the fewest deals
  (1.38) despite spending the most overall across every other channel

## Tech Stack
Python, Pandas, Matplotlib

## How to Run
Open in Google Colab, run all cells. Dataset auto-downloads via `kagglehub` with a synthetic
fallback if it ever fails.
