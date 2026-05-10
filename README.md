# Portfolio Signals Dashboard (Brief)

## What this script does
This is a **single-file, browser-only stock analysis dashboard** that generates **BUY / HOLD / TRIM / SELL signals** by combining technical analysis, company fundamentals, and recent news sentiment.

It runs fully in the browser (no backend) and is designed to work reliably with **free API tiers**.

---

## Signal Strategy (Quick Overview)
Each stock is evaluated using **three independent scores (0–100)**, then combined into one final signal.

---

### 1. Technical Analysis (Price Action)
Calculated locally using daily candles:
- RSI (14)
- SMA 20 / 50 / 200 (trend direction)
- MACD histogram (momentum shifts)
- Bollinger Bands (volatility extremes)
- Volume vs 20‑day average

**Candle source logic:**
- Primary: Finnhub `/stock/candle`
- Auto‑fallback: Alpha Vantage daily candles (when Finnhub is blocked)
- Fail‑safe: If unavailable, technical score defaults to **neutral (50)**

---

### 2. Fundamental Analysis (Business Quality)
Based on Finnhub key metrics:
- Revenue growth
- EPS growth
- Return on equity (ROE)
- Operating margin
- Debt‑to‑equity
- P/E and PEG ratios
- Free cash flow

Higher scores favor profitable, growing, financially healthy companies.

---

### 3. Sentiment Analysis (News Tone)
- Uses recent company news headlines
- Keyword‑weighted positive vs negative scoring
- Produces a short‑term sentiment score

Sentiment affects timing but does not dominate decisions.

---

## Composite Score

```
Composite Score =
  40% Technical
+ 40% Fundamental
+ 20% Sentiment
```

---

## Signal Mapping

| Conditions | Signal |
|-----------|--------|
| Strong trend + strong fundamentals | BUY MORE |
| Neutral or mixed signals | HOLD |
| Overbought or weakening setup | TRIM |
| Breakdown in trend or fundamentals | SELL |

Signals are **rule‑based, explainable, and deterministic**.

---

## Design Philosophy
- No black‑box AI
- No over‑fitting
- Minimal trading noise
- Graceful handling of API limits

Built for **portfolio monitoring and decision support**, not day trading.

---

## Disclaimer
This tool is for **educational purposes only** and is not financial advice.
Always do your own research before making investment decisions.
