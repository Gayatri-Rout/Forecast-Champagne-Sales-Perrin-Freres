# Sales Forecasting Project

## Problem Statement
The objective of this project was to forecast monthly champagne sales for Perrin Freres using time series analysis techniques. The sales data was obtained from the Kaggle dataset: [Perrin Freres Monthly Champagne Sales](https://www.kaggle.com/greymind/perrin-freres-monthly-champagne-sales).

## Steps Performed

### Data Preparation
- Loaded the dataset using Pandas.
- Renamed columns for clarity.
- Converted the 'Month' column to datetime format and set it as the index.
- Removed the last two rows for consistency.

### Exploratory Data Analysis
- Checked for missing values and data types.
- Visualized the sales data over time using a line plot.

### Stationarity Check
- Conducted the Augmented Dickey-Fuller (ADF) test to test for stationarity.
- Found that the data was non-stationary, indicating the presence of a unit root.

### Differencing
- Applied differencing to make the data stationary.
- Checked for stationarity again using the ADF test, confirming stationarity.

### Auto Regressive (AR) Model
- Plotted autocorrelation and partial autocorrelation functions to determine AR model parameters.
- Implemented a non-seasonal ARIMA model with order (1,1,1) for forecasting.

### Seasonal ARIMA Model
- Utilized a Seasonal ARIMA (SARIMA) model with seasonal order (1,1,1,12) for improved forecasting.

### Forecasting
- Predicted sales for the next 2 years using both ARIMA and SARIMA models.
- Visualized the forecasted sales alongside historical data.
