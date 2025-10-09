# Forecasting UK Vacancy Levels 

Monthly ONS vacancies: scrape latest vintages, consolidate, highlight patterns, and build simple baselines (STL+ARIMA, Holt-Winters).

## Data source
Office for National Statistics (AP2Y). Scraper uses a polite User-Agent and handles 429 with backoff.

## Quick start
```bash
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab  # or jupyter notebook

Open notebooks/forecasting_vacancy_levels.ipynb and run cells in order:
1. Scrape (respects ONS limits)
2. Consolidate (monthly obs + vintage_date)
3. Visualise patterns (STL)
4. Forecast (STL+ARIMA and Holt-Winters)

Outputs
- data/raw/AP2Y_prev_*.csv (downloaded files)
- data/processed/vacancies_vintages.csv (tidy panel)

Notes / limits
- Scrapes latest ~20 vintages, so older months often appear “final”.
- Proper evaluation should be vintage-aware (rolling backtest vs first-published targets).

License
- MIT