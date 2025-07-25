# 🚗 Electric Vehicle (EV) Charging Demand Prediction Project

This project focuses on forecasting the adoption of Electric Vehicles (EVs) across various counties using historical registration data. The goal is to enable better planning for EV infrastructure like charging stations by predicting future EV trends.

## 📁 Dataset

- **Source:** `Electric_Vehicle_Population_By_County.csv`
- **Columns include:**
  - Date
  - County, State
  - Battery Electric Vehicles (BEVs)
  - Plug-In Hybrid Electric Vehicles (PHEVs)
  - EV Total, Non-EV Total
  - Percent Electric Vehicles

## 📊 Key Features of the Project

### ✅ Data Preprocessing
- Handled missing values using `fillna` and `dropna`.
- Removed outliers using the Interquartile Range (IQR) method.
- Converted relevant columns to numeric data types.

### 🧠 Feature Engineering
- Extracted year, month, and numeric date from the `Date` column.
- Created lag features (`lag1`, `lag2`, `lag3`) for EV totals.
- Computed rolling means and percentage changes over time.
- Calculated EV growth slope using linear regression on rolling windows.
- Label-encoded county names.

### 🔍 Model Training
- Used **RandomForestRegressor** for EV prediction.
- Tuned hyperparameters using **RandomizedSearchCV**.
- Trained on engineered features and evaluated using:
  - **MAE**, **RMSE**, and **R² Score**

### 📈 Forecasting
- Forecasted EV growth for the next **3 years (36 months)** per county.
- Plotted:
  - Actual vs Predicted values for a selected county.
  - Cumulative EV growth.
  - Top 5 counties with the highest future EV adoption.

### 💾 Model Persistence
- Saved the trained model using `joblib`.
- Demonstrated model reusability by reloading and testing predictions.

## 📉 Visualizations
- Bar charts for vehicle type breakdown.
- Line plots showing EV trends (historical vs forecasted).
- Cumulative EV adoption for top 5 counties.

## 🧪 Evaluation Metrics
- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)
- **R² Score** (Coefficient of Determination)

## 📦 Requirements

Install the following Python libraries before running the notebook:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn joblib
```
---

**Author:** **HimanshuC_07** 

---
