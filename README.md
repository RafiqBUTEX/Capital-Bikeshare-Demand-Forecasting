# Micro-Mobility Time-Series Demand Forecasting

## Overview
This repository implements a leak-free time-series demand forecasting pipeline using the Capital Bikeshare dataset (17,379 hourly records).

## Key Highlights
* **Leakage Prevention:** Removed short-term ground-truth lags ($t-1$ through $t-24$) to evaluate multi-day horizons (Days 21–end of month) without lookahead bias.
* **Feature Engineering:** Used sine/cosine cyclical time encodings and out-of-fold target encodings computed exclusively from training data (Days 1–20).
* **Multicollinearity:** Dropped `atemp` due to high correlation with `temp` ($r > 0.98$).

## Results (Days 21+ Test Set)
* **Gradient Boosting:** $R^2 = 0.8788$, $\text{RMSE} = 63.06$, $\text{MAE} = 39.01$
* **Random Forest:** $R^2 = 0.8634$, $\text{RMSE} = 66.94$
* **Ridge Regression:** $R^2 = 0.7783$, $\text{RMSE} = 85.27$


## 🗂️ Repository Structure
- `Md. Rafiqul Islam_BikeSharing.ipynb`: Complete executable Jupyter notebook with data preprocessing, feature engineering, model training, and evaluation logs.
- `hour.csv`: Capital Bikeshare hourly dataset (UCI Machine Learning Repository).
