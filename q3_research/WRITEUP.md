# Q3 — Research process memo (idea validation / kill criteria)

## How I validate a trading idea

1. **Write the hypothesis** in one sentence (what edge, on what horizon, why it should exist).
2. **Code a minimal test** on public/sample OHLC — no curve-fitting marathon before a first read.
3. **Score with fixed risk** ($100k · 1.25% per trade) so P&L talk stays in R.
4. **Apply kill triggers** before “liking” the story:

| Code | Trigger | Action |
|------|---------|--------|
| K1 | Rolling expectancy ≤ 0 | Pause |
| K2 | Drawdown exceeds budget | Cut size / archive |
| K3 | Live process ≠ written rules | Immediate stop |
| K4 | Costs / data invalidate assumption | Archive |
| K5 | Daily loss kills cluster | Reduce frequency |

5. **Log the retirement** so dead ideas stay dead (`kill_log.csv` → `run_kill_log.py`).

## Why this matters for a QR intern

DTL’s Quantitative Researcher internship is about designing and backtesting models under senior guidance. Showing a **kill path** proves you can research without falling in love with every chart story — and that you document when an idea is dead.
