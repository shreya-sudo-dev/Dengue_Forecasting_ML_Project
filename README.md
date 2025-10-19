# Dengue Cases Prediction using XGBoost Regression

## Project Overview
This project aims to forecast dengue cases across Indian Districts using climatic and vegetation parameters.
It leverages a **Machine Learning Model (XGBoost Regressor)** trained on time-series data of dengue cases, temperature, precipitation, and leaf area index (LAI).

---

## Technologies Used
- Python
- Google Colab
- Pandas, Numpy, Matplotlib
- Scikit-learn
- XGBoost

---

## Dataset Used
**Name** -  'Weekly District-Wise all-India multi-epidemics Climate-Health Dataset for accelerated GeoHealth research'
The dataset contains dengue case counts across Indian states and districts with daily meteorological data such as temperature, precipitation, and vegetation index (LAI).

---

## Data Preprocessing
1. Null value handling and type conversion for `Cases`  
2. Creation of lag features (`cases_lag1`, `Cases_lag7`) and moving averages (`cases_ma7`, `Cases_ma14`)  
3. One-hot encoding for categorical variables (`state_ut`, `district`)  
4. Standardization using `StandardScaler`

## Model Description
**Algorithm:** XGBoost Regressor  
- `n_estimators = 200`  
- `learning_rate = 0.1`  
- `objective = reg:squarederror`  

The model learns from past cases, weather, and vegetation patterns to predict the number of dengue cases for a given date and location.

---

## Model Evaluation
| Metric | Value |
|:-------|:------:|
| MAE | *5.41* |
| MSE | *148.92* |
| RMSE | *12.20* |
| R² Score | *0.95* |

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/shreya-sudo-dev/Dengue_Forecasting_ML_Project
