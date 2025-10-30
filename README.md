# digital-asset-hoi-dataset
Dataset for “A Multi-Resolution Network Framework in Digital Asset Markets Based on High-Order Information Dynamics”: cryptocurrency CSVs (raw + processed) with O-information–based descriptors (OIR, local OIR, OIR-gradient).

## Structure
- `raw/` — source CSVs (BNBUSDT, BTCUSDT, ETHUSDT, SOLUSDT; multiple periods)
- `processed/` — analysis-ready CSVs used in the paper

## raw/ schema (per-file CSV)
- `timestamp` — milliseconds
- `open`
- `low`
- `high`
- `close`
- `volume`
- `close_time` — milliseconds
- `quote_asset_volume`
- `number_of_trades`
- `taker_buy_base_asset_volume`
- `taker_buy_quote_asset_volume`

## processed/ schema
- `date`
- `return`
- `volatility`
- `volume change`
- `order flow imbalance`
- `illiquidity`

