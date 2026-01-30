# digital-asset-hoi-dataset

Dataset for “A Multi-scale Network Framework in Digital Asset Markets Based on High-Order Information Dynamics”: cryptocurrency CSVs (raw + processed).
Coverage: 2020-08 to 2025-11. Intervals: 2h/6h/12h/1d. Symbols: ADAUSDT, AVAXUSDT, …, XRPUSDT.
 `raw_data/` contains OHLCV-style candles; `processed_data/` contains derived features (definitions follow the paper). 

## Structure

- `raw_data/` — source CSV files, grouped by sampling interval:
  - `12h/`, `2h/`, `6h/`, `1d/`
  - File pattern: `<SYMBOL>_<INTERVAL>_2020-08_2025-11.csv` 
- `processed_data/` — processed CSV files, grouped by sampling interval:
  - `12h/`, `2h/`, `6h/`, `1d/`
  - File pattern: `processed_<SYMBOL>_<INTERVAL>_2020-08_2025-11.csv` 

Symbols included in this repository:
`ADAUSDT`, `AVAXUSDT`, `BNBUSDT`, `BTCUSDT`, `DOGEUSDT`, `DOTUSDT`, `ETHUSDT`, `LINKUSDT`, `LTCUSDT`, `SOLUSDT`, `TRXUSDT`, `XRPUSDT`.

## `raw_data/` schema (per-file CSV)

Columns:

- `open_time` — timestamp in milliseconds
- `open`
- `high`
- `low`
- `close`
- `volume`
- `close_time` — timestamp in milliseconds
- `quote_asset_volume`
- `number_of_trades`
- `taker_buy_base_asset_volume`
- `taker_buy_quote_asset_volume`
- `ignore`
- `symbol`

## `processed_data/` schema (per-file CSV)

Columns:

- `date`
- `return`
- `volatility`
- `volume change`
- `order flow imbalance`
- `illiquidity`
