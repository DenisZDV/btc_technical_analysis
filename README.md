# BTC Technical Analysis

Two standalone browser tools for Bitcoin market analysis. No backend, no dependencies to install — open and run.

## Tools

<img width="750" height="619" alt="image" src="https://github.com/user-attachments/assets/153d067f-1a69-49bf-bced-66239efbc638" />

### `btc_distribution.html` — Return Distribution
Daily return distribution for BTC over the last 365 days with interactive probability calculator.

- Histogram of real daily returns vs normal distribution curve
- Fat tails visualization — where BTC diverges from theory
- Interactive threshold slider: P(x > threshold) calculated in real time
- Preset buttons: +5%, +10%, −5%, −10%
- Stats: mean (μ), volatility (σ), days of data

**Data:** CoinGecko API · 365 days · daily closes

---

<img width="750" height="831" alt="image" src="https://github.com/user-attachments/assets/7f03ebcf-f4b4-4ca7-907d-8c447d8cd0a6" />

### `volume_profile.html` — Volume Profile
Volume distribution across price levels with Point of Control and Value Area detection.

- Candlestick chart with POC / VAH / VAL horizontal levels
- Volume Profile bars — volume at each price level
- Value Area band (70% of total volume) highlighted on chart
- Period selector: 7D / 30D / 90D / 180D

**Key levels:**
- **POC** (Point of Control) — price level with maximum traded volume
- **VAH** (Value Area High) — upper boundary of 70% volume zone
- **VAL** (Value Area Low) — lower boundary of 70% volume zone

**Data:** Binance → Bybit → OKX fallback · OHLCV klines

---

## Usage

Download the file and open in any browser. No server required.

```
btc_distribution.html  →  open in browser
volume_profile.html    →  open in browser
```

Both tools fall back to generated demo data if exchange APIs are unreachable.

## Stack

Vanilla JS · Canvas API · Chart.js · Binance API · Bybit API · OKX API · CoinGecko API

---

*Part of [DenisZDV](https://github.com/DenisZDV) analytics toolkit*
