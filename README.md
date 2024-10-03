## Overview

`ARIMA_Simul` is a Python class for ARIMA (AutoRegressive Integrated Moving Average) time-series forecasting with advanced features. It provides user-controlled differencing, iterative model selection, empirical noise distribution, and simulation generation.

## Features

- Stationarity checking with Dickey-Fuller test
- User-controlled differencing
- Iterative model selection using AIC and p-values
- ARIMA model fitting and evaluation
- Forecast simulation with empirical noise distribution
- Exceedance probability calculation

## Methods

- `check_stationarity`: Check series stationarity using Dickey-Fuller test
- `difference_series`: Difference the time series
- `stationarity_iter`: Iteratively difference until stationarity is achieved
- `run_ARIMA`: Run statsmodels ARIMA model
- `evaluate_arima_models`: Evaluate ARIMA models to minimize AIC
- `remove_p_val`: Remove insignificant parameters from best ARIMA model
- `n_forecasts`: Generate multiple forecast simulations
- `exceedance_prob`: Calculate exceedance probability for forecasts

## Usage

```python
# Example usage
ts = [your_time_series_data]
arima_model = ARIMA_Simul(ts)
arima_model.stationarity_iter(0.05)
arima_model.evaluate_arima_models(range(1,4), range(1,4))
arima_model.n_forecasts(100, 12)
