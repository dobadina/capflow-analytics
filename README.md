# CapFlow Analytics

Commercial analytics portfolio project built to demonstrate Strategy Analyst capabilities.

## The Scenario

CapFlow is a UK-based embedded finance company providing revenue-based financing to small
businesses through three partner platforms: ShopBase, MarketHub, and RetailCloud.

## Deliverables

| # | Deliverable | Status |
|---|---|---|
| D1 | Variance Decomposition Report | In progress |
| D2 | Partner Performance Dashboard | Not started |
| D3 | MarketHub Conversion Investigation | Not started |
| D4 | Pricing Impact Model | Not started |
| D5 | Commercial Forecast Model | Not started |
| D6 | Written Strategy Brief | Not started |

## Tech Stack

- Python (Pandas, NumPy, Matplotlib, scikit-learn, XGBoost, statsmodels)
- SQLite
- Metabase via Docker
- Excel (openpyxl)
- Google Colab

## Setup

```bash
pip install -r requirements.txt
```

## Structure
capflow-analytics/
├── data/               # SQLite database and raw CSVs
├── notebooks/          # Jupyter notebooks, one per deliverable
├── models/             # Excel pricing and forecast models
├── reports/            # PDFs and charts
├── sql/                # Standalone SQL queries for Metabase
└── metabase/           # Docker config

