## How to run
1) Clone the repo
2) pip install -r requirements.txt
3) Open notebooks/forecasting_vacancy_levels.ipynb
4) Run all cells in order:
   - Step 1 scrapes and downloads ≥20 vintages into data/raw/
   - Step 2 consolidates into data/processed/vacancies_vintages.csv
   - Step 3 shows a revision plot
   - Step 4 trains a simple ETS forecast
Notes: If you see HTTP 429 (rate limited), re-run the scrape cell; it will resume and skip already-downloaded files.
