# Fillfolio for Claude

Ask Claude about the money you track in [Fillfolio](https://fillfolio.com): stocks, ETFs, funds, wallets, cash, liabilities, bank spending and budgets. The plugin connects Claude to your own Fillfolio account and adds three skills that turn the saved records into clear answers and reviews.

It is read-only. Claude cannot trade, move money, edit your records, or refresh your brokerages, exchanges, wallets or banks. It reads what is already saved in Fillfolio.

## What is included

| Part | What it does |
|---|---|
| Fillfolio connector | Connects to `https://fillfolio.com/api/mcp` with your Fillfolio sign-in. Ten read-only tools and a dashboard panel. |
| `portfolio-chat` skill | Answers questions about your net worth, portfolios, holdings, cash, liabilities, activity, spending and budgets. |
| `portfolio-review` skill | A structured review of what you hold: allocation, concentration, currency mix, and how fresh the data is. |
| `budget-vs-actual` skill | Compares a month's budgets with what was actually spent, category by category. |

None of the skills gives financial advice. They describe your records; decisions are yours.

## Connect

1. Install the plugin.
2. Open the plugin's Connectors tab and connect Fillfolio. In Claude Code the sign-in opens the first time a Fillfolio tool is used.
3. Sign in to Fillfolio and approve read access.

You need a Fillfolio account. What Claude can read is what your account itself can open in Fillfolio. Bank spending, transactions and budgets also need two separate permissions that you turn on in Fillfolio Settings.

## Try it

- "Show my Fillfolio portfolio summary with currencies and data freshness."
- "Review my portfolio: where am I concentrated?"
- "How did I do against my budgets last month?"
- "Open the Fillfolio dashboard."

## Privacy and control

- Claude receives the records a tool returns, and the data of any dashboard view you open. The dashboard's Hide amounts control masks the screen only.
- Revoke the connection at any time in Fillfolio Settings. Access tokens last ten minutes.
- Privacy policy: https://fillfolio.com/privacy
- Support: https://fillfolio.com/contact

## License

MIT, for the files in this repository. See [LICENSE](LICENSE).
