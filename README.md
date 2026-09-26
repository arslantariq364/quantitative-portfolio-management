# Quantitative Risk & Portfolio Analytics

Python learning notebooks for investment returns, volatility, Sharpe ratios, wealth indexes and historical drawdowns. These are analytical exercises, not a portfolio optimization or trading system.

## Files
- `Returns Lab Basics.ipynb`: percentage returns, compounding and annualization examples.
- `Risk Adjusted Returns.ipynb`: volatility annualization and Sharpe calculations.
- `LabSessionDrawdown.ipynb`: wealth indexes, previous peaks and drawdown exploration.

## Setup

```bash
git clone https://github.com/arslantariq364/quantitative-portfolio-management.git
cd quantitative-portfolio-management
python3 -m venv .venv
source .venv/bin/activate
python -m pip install numpy pandas matplotlib jupyter
jupyter notebook
```

Before running the two market-data notebooks, change their CSV references to the committed filename `Portfolios_Formed_on_ME_monthly_EW (1).csv` or provide a local copy at the filename they request.

## Known limitations

The reusable `drawdown()` helper is missing parentheses: the intended expression is `(wealth_index - previous_peaks) / previous_peaks`. The earlier top-level expression includes them. Clear stale notebook outputs and rerun after fixing it. Some cells are exploratory or intentionally show incorrect intermediate attempts. No automated correctness suite is provided.

This revision does not implement historical/Gaussian/Cornish-Fisher VaR, CVaR, Sortino, efficient-frontier optimization, quadratic programming, allocation constraints, turnover constraints or benchmark strategy comparisons. No investment-performance claim is made.
