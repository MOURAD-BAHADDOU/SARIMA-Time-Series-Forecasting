# SARIMA-Time-Series-Forecasting
# SARIMA Time Series Forecasting Project

**A Python implementation of Seasonal SARIMA for time series analysis and forecasting.**

## Overview
This project demonstrates how to build, tune, and evaluate a **SARIMA model** for time series forecasting. Ideal for data with trends and seasonality (e.g., sales, weather, stock prices).

## 🛠 Features
- **SARIMA modeling** with `statsmodels` (auto-ARIMA included).
- **Grid search** for optimal `(p,d,q)(P,D,Q,s)` parameters.
- **Visual diagnostics**: ACF/PACF plots, forecast vs. actuals.
- **Metrics**: MAE, RMSE, AIC/BIC, and residual analysis.

## Dataset
- **Data**: `data/monthly-milk-production (1).csv` 

## Setup
1. **Clone the repo**:
   ```bash
   git clone https://github.com/MOURAD-BAHADDOU/SARIMA-Time-Series-Forecasting.git
