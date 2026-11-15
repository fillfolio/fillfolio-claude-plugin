---
name: portfolio-review
description: Use when the user asks for a review, check-up or breakdown of their Fillfolio investments - allocation, diversification, concentration, biggest positions, currency exposure, or how up to date the data is.
argument-hint: "[portfolio name]"
---

# Fillfolio portfolio review

Produce a structured, factual review of what the user holds, from their saved Fillfolio records.

**Important**: This skill describes the portfolio. It does not provide financial or investment advice and never recommends buying, selling or holding anything.

## Steps

1. Call `get_portfolio_summary`, `list_portfolios` and `list_holdings`. If the user named a portfolio, review only that one. Call `list_cash_and_liabilities` only if the user asked for net worth context; if Fillfolio refuses it, continue without it and say so.
2. Use only returned values. Work in the summary's reporting currency. If a holding has no value or no cost basis, list it under data gaps; do not estimate it.
3. Compute shares as value divided by total holdings value. Show your basis when a number is partial.

## Report, in this order

1. **Snapshot**: total value, number of holdings and portfolios, total return if returned, reporting currency, and the date of the data.
2. **Allocation by asset type**: stocks, ETFs, funds, crypto, other: value and share.
3. **Concentration**: the five largest positions with value and share; the combined share of the top five; any single position above 10% of holdings.
4. **By portfolio or account**: value and share of each.
5. **Currency mix**: share by holding currency, if more than one is present.
6. **Data quality**: quotes older than the summary date, holdings without cost basis or price, partial-data warnings, sync times.
7. **Questions to consider**: up to three neutral observations phrased as questions (for example, "One position is 34% of holdings; is that intended?"). No recommendations.

Keep it to one screen unless the user asks for detail. Use a table for sections 2 to 5. Keep currency labels on every amount.
