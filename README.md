# Relationship Between Stock Prices, Interest Rates, and Inflation

This repository analyzes the relationship between the S&P 500 stock prices, US real interest rates, and US inflation rates from 1982 to 2023. The study aims to understand:

- Whether higher interest rates are associated with lower stock prices.
- If there is a lag (delay) in the response of stock prices to changes in interest rates.
- Whether inflation rates significantly relate to stock prices.

## Data Sources

- **S&P 500 Data (1982-2023):** Monthly closing prices of the S&P 500, found at https://www.investing.com/indices/us-spx-500-historical-data.
- **US Monthly Inflation Rate (1982-2023):** Derived from CPI data, found at https://data.bls.gov/timeseries/CUSR0000SA0&output_view=pct_1mth.
- **US Monthly Real 10-Year Interest Rate (1982-2023):** Real (inflation-adjusted) 10-year Treasury yield, found at https://fred.stlouisfed.org/series/REAINTRATREARAT10Y.

All data files should be placed in the same directory as the `project.ipynb` notebook:

- `S&P_500_1982-2023.csv`
- `US_Monthly_Inflation_Rate_1982-2023.xlsx`
- `US_Monthly_Real_10Y_Interest_Rate_1982-2023.csv`

## Analysis Steps

1. **Data Preprocessing:**

   - Clean and merge the three datasets into a single monthly time series.
2. **Statistical Analysis:**

   - Compute Pearson correlations between:
     - Interest Rate and S&P 500 Price
     - Inflation Rate and S&P 500 Price
   - Perform a simple linear regression:
     - S&P 500 Price as the dependent variable and Interest Rate as the independent variable.
   - Conduct a lag analysis (cross-correlation) to identify if interest rate changes lead changes in stock prices.
3. **Visualization:**

   - Plot time series of each variable over the period.
   - Scatter plots to visualize relationships.
   - A cross-correlation stem plot to identify lag effects.

## Interpretation

- **Interest Rates and Stock Prices:**
  Typically, higher interest rates make borrowing more expensive, potentially lowering corporate profits and thus stock prices. A negative correlation suggests that as interest rates rise, stock prices tend to fall.
- **Lag Analysis:**
  If a significant lag is found, it suggests that changes in interest rates influence stock prices after a certain time delay, rather than instantaneously.
- **Inflation and Stock Prices:**
  The analysis checks if inflation rates show a noticeable relationship with stock prices. If not significant, it may mean inflation during this period did not substantially impact equity markets in a linear way.

## Requirements

- Python 3.7+
- Jupyter Notebook
- Pandas
- NumPy
- SciPy
- Matplotlib
- openpyxl (for reading Excel files)

Install the required packages with:

```bash
pip install pandas numpy scipy matplotlib openpyxl
```
