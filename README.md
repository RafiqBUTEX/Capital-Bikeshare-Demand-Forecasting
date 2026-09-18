# Capital Bikeshare Demand Forecasting

**Author:** Rafiqul Islam  
**Context:** PhD Technical Assessment Submission

## 📌 Project Overview
An end-to-end time-series machine learning pipeline for predicting rental bike demand using the UCI Capital Bikeshare dataset. 

To prevent temporal data leakage, the model enforces a strict cutoff temporal split (days 1–20 reserved for training/validation, days 21–end for testing).

## 📊 Performance Metrics
- **Primary Model:** Gradient Boosting Regressor (with cyclical time encoding, lagged features, and out-of-fold target encoding)
- **$R^2$ Score:** `0.8788`
- **RMSE:** `63.06`
- **MAE:** `39.01`

## 🗂️ Repository Structure
- `PhD_Technical_Assessment_Rafiqul_Islam.ipynb`: Complete executable Jupyter notebook with data preprocessing, feature engineering, model training, and evaluation logs.
- `hour.csv`: Capital Bikeshare hourly dataset (UCI Machine Learning Repository).
