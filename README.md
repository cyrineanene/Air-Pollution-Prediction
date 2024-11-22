# Air-Pollution-Prediction-and-Forecasting

This repository contains the implementation of a machine learning project to predict and forecast Air Quality Index (AQI) values. The project is divided into two main tasks: 

1. **Predicting AQI Values** using Regression models.
2. **Forecasting AQI Trends** using the Prophet model.

## Project Overview

Air quality is an essential indicator of environmental health and public safety. This project aims to predict AQI values based on historical data and identify trends in air quality over time.

### Objectives

1. Build a robust regression model to predict AQI values based on historical data.
2. Forecast future air quality trends using the Prophet model for time-series forecasting.

## Datasets

### 1. **Air Quality Index Dataset**
- **Source**: [Kaggle Link](https://www.kaggle.com/datasets/azminetoushikwasi/aqi-air-quality-index-scheduled-daily-update)
- **Description**: This dataset contains Air Quality Index of most the countries of the world.
- **Rows**: 15,987
- **Columns**:
  - `Date`: The timestamp of the recorded AQI value.
  - `Country`: The country where AQI was measured.
  - `Status`: A qualitative indicator of air quality.
  - `AQI Value`: The numerical AQI value.

### 2. **AirQuality UCI Dataset**
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/360/air+quality)
- **Description**: Contains air quality metrics for forecasting AQI trends.
- **Metrics**: Concentrations of various pollutants like CO, NO, NO2, O3, SO2, PM2.5, PM10, and NH3.

## Methodology

### Task 1: **Predicting AQI Values**
1. **Data Preprocessing**
   - Handled missing values and ensured data consistency.
   - Encoded categorical variables such as `Country` and `Status`.

2. **Model Comparison**
   - Implemented and compared the following regression models:
     - RandomForestRegressor
     - LinearRegression
     - Ridge
   - Evaluation metrics: Mean Squared Error, Mean Absolute Error, Validation and Test R² scores.

3. **Results**
   - **RandomForestRegressor** was the best-performing model with:
     - **Validation R²**: 0.9049
     - **Test R²**: 0.9424

### Task 2: **Forecasting AQI Trends**
1. **Data Preparation**
   - Filtered and aggregated data to prepare it for time-series analysis.
   - Feature Engineering, adding the `AQI Value Column` and preparing the `ds` Column

2. **Forecasting with Prophet**
   - Utilized the Facebook Prophet model for time-series forecasting.
   - Generated future AQI trends.