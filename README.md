# CapFlow Analytics

Commercial analytics portfolio project built to demonstrate Strategy Analyst capabilities.
Built as a preparation project for a Strategy Analyst role at YouLend.

## The Scenario

CapFlow is a UK-based embedded finance company providing revenue-based financing to small
businesses through three partner platforms: ShopBase, MarketHub, and RetailCloud.

The Head of Commercial flagged three problems:
- Funded volume came in 18% below forecast last quarter
- MarketHub conversion rate has been declining for three consecutive months
- The pricing team wants to know whether reducing the ShopBase factor rate by 0.5% is worth it

This project builds the analytical infrastructure to answer all three.

## Deliverables

| # | Deliverable | Status |
|---|---|---|
| D1 | Variance Decomposition Report | Done |
| D2 | Partner Performance Dashboard | Scoped, not built |
| D3 | Conversion Rate Investigation | Done |
| D4 | ShopBase Pricing Model | Done |
| D5 | Commercial Forecast Model | Done |
| D6 | Strategy Brief | Done |

## Key Findings

**Q4 Miss:** £1.3M shortfall (14.9% below forecast) driven by conversion decline (£947k)
and lead volume shortfall (£830k), partially offset by a favourable mix shift (£559k).

**MarketHub:** Approval rate fell from 35.9% to 31.2% over six months, costing an
estimated £672k in funded volume. Isolated to MarketHub -- ShopBase and RetailCloud
were flat over the same period.

**ShopBase Pricing:** The rate cut breaks even at just 2.2% volume uplift (31 extra deals).
All three scenarios are NPV-positive. Recommended approach is a 60-90 day controlled
test before full rollout.

## Tech Stack

- Python (Pandas, NumPy, Matplotlib, scikit-learn, statsmodels, openpyxl)
- SQLite
- Excel (dynamic pricing and forecast models with live formulas)
- Google Colab
- Git / GitHub

## Structure

capflow-analytics/
├── data/               # SQLite database (capflow.db)
├── notebooks/          # Single notebook with all analysis (capflow_analytics.ipynb)
├── models/             # Excel pricing and forecast models
│   ├── shopbase_pricing_model.xlsx
│   └── forecast_model.xlsx
├── reports/            # Charts and validation outputs
│   └── validation_charts/
├── sql/                # SQL queries for Metabase dashboard (scoped, not built)
└── metabase/           # Docker config (scoped, not built)

## Setup

```bash
pip install -r requirements.txt
```

Open `notebooks/capflow_analytics.ipynb` in Google Colab and run each section in order.
Mount your Google Drive when prompted and update PROJECT_ROOT to match your Drive path.

## How to Talk About This Project

The project covers five analytical areas:

1. **Variance decomposition** -- price-volume-mix methodology, waterfall chart, exec brief
2. **Conversion investigation** -- network-wide analysis, logistic regression, revenue impact
3. **Pricing model** -- breakeven analysis, scenario modelling, dynamic Excel output
4. **Forecast model** -- bottom-up construction, scenario toggles, variance tracker
5. **Strategy brief** -- two-page exec summary translating all findings into recommendations
