# Sales Forecasting Project

## Problem Statement
The objective of this project was to forecast monthly champagne sales for Perrin Freres using time series analysis techniques. The sales data was obtained from the Kaggle dataset: [Perrin Freres Monthly Champagne Sales](https://www.kaggle.com/greymind/perrin-freres-monthly-champagne-sales).

## Steps Performed

### Data Preparation and EDA
- Loaded the dataset using Pandas.
- Renamed columns for clarity.
- Converted the 'Month' column to datetime format and set it as the index.
- Removed the last two rows(Had missing values) for consistency.

### Stationarity Check
- Conducted the Augmented Dickey-Fuller (ADF) test to test for stationarity.
- Found that the data was non-stationary, indicating the presence of a unit root.

### Differencing
- Applied differencing to make the data stationary.
- Checked for stationarity again using the ADF test, confirming stationarity.

### Auto Regressive (AR) Model
- Plotted autocorrelation and partial autocorrelation functions to determine AR model parameters.
- Implemented ARIMA model with order (1,1,1) for forecasting.
- ![image](https://github.com/Gayatri-Rout/Forecast-Champagne-Sales-Perrin-Freres/assets/70259060/7461c765-51e9-4c43-b6c4-e832215cd725)
- <b>OBSERVATION:</b> Data was originally seasonal(non-stationary), even after converting it to stationary, the forecasting is poor as illustrated in the above graph.


### Seasonal ARIMA Model
- Utilized a Seasonal ARIMA (SARIMA) model with seasonal order (1,1,1,12) for improved forecasting.
  ![image](https://github.com/Gayatri-Rout/Forecast-Champagne-Sales-Perrin-Freres/assets/70259060/f6232483-9cfb-4cc2-99d6-6d7d5c20d32b)
  

### Forecasting
- Predicted sales for the next 2 years using SARIMA model.
  ![image](https://github.com/Gayatri-Rout/Forecast-Champagne-Sales-Perrin-Freres/assets/70259060/96e5fa37-fa76-40bd-a424-11b007dacc3c)

