# canadian-entertainment-stock-analysis
Python-based analysis of Canadian entertainment and media stocks (2020–2025), featuring data collection, OLS modeling, and moving-average analysis of market performance.


This repository presents my analysis of Canadian entertainment and media companies’ stock performance between **August 2020 and August 2025**.  
The project investigates how **sector focus (core vs. diversified companies)** and **technical indicators** such as moving averages influence stock volatility and returns.  
All data extraction, processing, and modeling were completed in **Python**.

---

## Research Focus

1. **RQ1 – Exploratory Comparison (Team Component)**  
   *How do stock performance patterns differ between core and extra companies?*
   → Addressed through Tableau dashboards by teammates (not included here).

2. **RQ2 – Predictive Modeling of Stock Performance**  
   *Can predictive models identify and explain differences in volatility, cumulative returns, and average daily returns between core and extra companies?*  
   - **H₀:** No significant differences exist between core and extra companies.  
   - **H₁:** Significant differences exist.

3. **RQ3 – Moving Averages and Return Association**  
   *How are short-term (MA5) and medium-term (MA20) moving averages associated with next-day returns?*  
   - **H₀:** No significant association between MA5/MA20 and next-day returns.  
   - **H₁:** Significant association exists.

---

## Methodology

### 1. Data Collection (`entertainment_data_pull.ipynb`)
- Retrieved historical stock data for 8 Canadian entertainment and media firms using the **Yahoo Finance API** (`yfinance`).  
- Computed daily returns, volatility, cumulative returns, and technical indicators (MA5, MA20).  
- Classified companies into *Core* and *Extra* categories based on their business scope.

### 2. RQ2: Core vs. Extra Modeling (`core_vs_extra_ols.ipynb`)
- Built **Ordinary Least Squares (OLS)** models with robust HC3 standard errors.  
- Compared volatility, cumulative return, and average daily return between the two company types.  
- Identified statistically significant performance differences.

### 3. RQ3: Moving Average Analysis (`moving_average_analysis.ipynb`)
- Modeled next-day returns as a function of MA5 and MA20 values.  
- Evaluated direction and significance of coefficients, and overall model fit (R²).  
- Determined whether short- or medium-term trends predict short-term performance.

### 4. Robustness Checks (`alternative_models.ipynb`)
- Explored alternative specifications (e.g., log returns, interaction effects).  
- Verified consistency of findings across model variations.

---

## Key Insights

- **Core companies** exhibited slightly higher cumulative returns and lower volatility than diversified “extra” firms.  
- **OLS regression** results indicate statistically significant differences in some performance measures, partially rejecting the null hypothesis for RQ2.  
- **Moving averages (MA5, MA20)** showed weak predictive power for next-day returns, supporting the null hypothesis for RQ3.  
- Findings suggest that **sector specialization** contributes to more stable long-term returns but not short-term predictability.

---

## Repository Contents

| Path | Description |
|------|--------------|
| `data/entertainment_stocks.csv` | Clean dataset of daily stock metrics (2020–2025) |
| `notebooks/entertainment_data_pull.ipynb` | Data extraction and preprocessing |
| `notebooks/core_vs_extra_ols.ipynb` | OLS models for volatility, cumulative returns, and average returns |
| `notebooks/moving_average_analysis.ipynb` | MA5/MA20 relationship modeling |
| `notebooks/AlternativeModels.ipynb` | Robustness checks and extensions |

---

## Skills Demonstrated

- Python for financial data analytics  
- Time-series feature engineering (returns, volatility, moving averages)  
- Statistical modeling with `statsmodels` (OLS, robust SEs)  
- Data visualization and interpretation using `matplotlib` and `seaborn`  
- Hypothesis testing and research communication  

---

## Data Source

Data retrieved via **Yahoo Finance API** (`yfinance`) for the period **Aug 2020 – Aug 2025**.  
Used solely for academic and portfolio demonstration purposes.

---
