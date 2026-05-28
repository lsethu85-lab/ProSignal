# Signal Dashboard V5 – Portfolio Autopilot

## What was added
- Upgraded fundamentals scoring
- Upgraded technical scoring
- Consistent risk scoring
- Live holding analysis using existing dashboard market data
- Dynamic target / stop / trailing stop generation
- Partial sell ladder (25% / 25% / 50%)
- Allocation % engine with rebalance suggestions
- Cash balance input and storage in browser localStorage
- Trade sizing suggestions (BUY / SELL / HOLD in shares)
- Risk-On / Risk-Off autopilot summary

## How to use
1. Open `fixed_index_with_holdings_v5.html` in a browser.
2. Go to **My Holdings**.
3. Enter ticker, average price, and shares.
4. Optionally set cash in the **Cash Balance** field and click **Save Cash**.
5. Click **Add Holding** to run live analysis.
6. Use **Refresh** to recalculate all holdings.

## Score interpretation
### Technical
- 80–100: strong trend + confirmation
- 65–79: constructive
- 50–64: neutral
- below 50: weak

### Fundamental
- 80–100: strong quality/growth
- 65–79: good
- 50–64: mixed
- below 50: weak / incomplete

### Risk
- 0–25: low risk
- 26–50: moderate
- 51–75: elevated
- 76+: high risk

## Notes
- This file gives recommendations only.
- It does not place trades automatically.
- Cash is simulated and stored locally in the browser (`portfolioCash`).
- Holdings are stored locally in the browser (`myHoldings`).
