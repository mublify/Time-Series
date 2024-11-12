# Sales Forecasting Project

## Introduction
This project aims to forecast monthly sales using advanced time series analysis techniques, specifically focusing on ARIMA and Holt-Winters models to identify patterns and make accurate predictions.

## Data Loading and Preprocessing
- **Data Import**: Loaded sales data from a CSV file.
- **Date Conversion**: Converted the 'Order Date' column to datetime format.
- **Aggregation**: Resampled the data to obtain monthly total sales.

## Data Visualization
- **Trend Analysis**: Plotted the monthly sales data to observe overall sales trends over time.

## Time Series Decomposition
- **Decomposition**: Performed seasonal decomposition to separate the trend, seasonality, and residuals in the time series.

## Stationarity Check
- **ADF Test**: Conducted the Augmented Dickey-Fuller (ADF) test to assess stationarity. Differenced the series if non-stationarity was detected.

## ARIMA Model
- **Model Selection**: Used the `auto_arima` function to automatically determine optimal ARIMA parameters.
- **Model Fitting**: Fitted the selected ARIMA model to the sales data.
- **Forecasting**: Generated forecasts with confidence intervals and visualized the forecast.

## Model Performance
- **Metrics Calculation**: Evaluated model accuracy using metrics like Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE).

## Holt-Winters Model
- **Model Specification**: Tested multiple Holt-Winters configurations, including additive and multiplicative seasonal effects.
- **Best Model Selection**: Chose the model with the lowest RMSE for best performance.
- **Forecasting**: Generated and visualized forecasts using the best-performing Holt-Winters model.
- **Residual Analysis**: Analyzed residuals to assess the goodness of fit of the selected model.

## Multiplicative Trend Parameters
For the best-performing multiplicative trend model, the parameters were as follows:
- **Smoothing Level (0.200)**: Gives moderate weight to recent observations, balancing past trends and current changes.
- **Trend Smoothing (0.100)**: Ensures trend adjustments are gradual, preventing overreaction to short-term changes.
- **Seasonal Smoothing (0.100)**: Adjusts seasonal patterns slowly, reflecting stable seasonal trends.
- **Damping Parameter (0.980)**: Maintains trend stability by allowing it to gradually taper over time, avoiding extreme growth or decline.

These parameter choices helped create a balanced model that captures trends and seasonal patterns effectively without overfitting to recent fluctuations.
