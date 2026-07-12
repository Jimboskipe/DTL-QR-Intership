# Alpha sample write-up (DTL QR internship)

## Hypothesis

Fade stretched short-horizon returns only when a longer trend filter agrees — a minimal, falsifiable research loop (not a claimed live edge).

## Method

- Sample OHLC → residual stretch vs lookback mean  
- Enter when stretch exceeds a z-style threshold **and** 50-bar trend agrees  
- Risk framing: **$100,000** account · **1.25%** risk per trade  
- Metrics: trade count, win rate, expectancy in R, total P&L  

## Keep / kill

DTL’s QR intern work is design + backtest under senior guidance. This packet shows:

1. Write the idea clearly  
2. Code a first test without curve-fitting theatre  
3. Score in R  
4. Kill when expectancy / DD / process breaks — see `../q3_research/`

## Honesty

Sample bars can produce losing or empty results. That is acceptable for a process demo. Replace with better data (e.g. MT5 fetch) before claiming anything tradable.
