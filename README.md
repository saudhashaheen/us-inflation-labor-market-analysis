# US Inflation and Labor Market Analysis (1958–2026)

**NYU Stern Data Bootcamp · Group Project · October 2026**

**Contributors:** Myra Rafiq, Muhammad Abdullah, Saudha Shaheen

## Overview

An exploratory study of how well traditional, expectations-augmented, and vacancies-based versions of the Phillips Curve describe US inflation across different economic periods.

## Dataset and methods

We retrieve five monthly economic indicators from the [Federal Reserve Economic Data (FRED)](https://fred.stlouisfed.org/): `UNRATE` (unemployment rate), `UNEMPLOY` (number unemployed), `JTSJOL` (job openings), `CPILFESL` (core CPI), and `CPIAUCSL` (headline CPI). The CPI data is converted to year-over-year percent change via the API.

We use Python, pandas, NumPy, Matplotlib, and Seaborn for data preparation and exploratory visualization. The notebook compares:

1. The traditional unemployment–inflation relationship from 1958 onward.
2. An expectations-augmented proxy using the change in average annual inflation across eras.
3. Core inflation against the ratio of job openings to unemployed persons (V/U) since 2000.

## Key observations

- The unemployment–inflation relationship varies substantially by era.
- The expectations-augmented proxy has a more visible inverse relationship in 1970–1983 than in recent periods.
- Higher V/U buckets generally coincide with higher average core inflation in the available sample.

**Limitations:** This is descriptive analysis, not causal inference. The analysis only covers US data, and the vacancy series has a shorter history. The expectations measure is an approximation using prior inflation, not survey expectations.

## Run locally

1. Install dependencies: `python -m pip install -r requirements.txt`
2. Obtain a personal API key from [FRED](https://fred.stlouisfed.org/docs/api/api_key.html).
3. Set the environment variable in your terminal before starting Jupyter:
   - macOS/Linux: `export FRED_API_KEY="your_key_here"`
   - Windows PowerShell: `$env:FRED_API_KEY="your_key_here"`
4. Start Jupyter: `jupyter notebook` and open `phillips_curve_analysis.ipynb`. Run all cells.

Never commit API keys or `.env` files to Git.

## Files

- `phillips_curve_analysis.ipynb` — analysis code, data cleaning, and visualizations.
- `project_presentation.pdf` — summary presentation of the analysis and findings.
- `requirements.txt` — Python dependencies.

## Authors

- `Saudha Shaheen
- `Muhammad Abdullah 
- `Myra Rafiq
  

## Acknowledgment

Data source: Federal Reserve Bank of St. Louis (FRED).
