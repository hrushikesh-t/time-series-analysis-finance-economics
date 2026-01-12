# Time Series Analysis of Financial and Economic Data
This project applies classical time series analysis techniques to real-world financial and economic datasets. 
ARMA and SARIMA models are used to analyze and forecast BlackRock (BLK) stock returns and the unemployment rate in California, 
demonstrating how statistical modeling supports risk assessment and economic decision-making.
## Project Overview
The project analyzes two different types of time series data to highlight the contrast between 
non-seasonal financial data and seasonal economic data. Each dataset is modeled using the 
Box–Jenkins methodology, including identification, estimation, diagnostic checking, and forecasting.
## Datasets

### 1. BlackRock (BLK) Stock Returns
- Source: Yahoo Finance
- Frequency: Daily (Jan 2025 – Nov 2025)
- Prices converted to daily returns to ensure stationarity

### 2. California Unemployment Rate
- Source: Federal Reserve Economic Data (FRED)
- Frequency: Monthly (Jan 1976 – Aug 2025)
- Exhibits strong trend and seasonal behavior
## Methodology

### Financial Time Series (Non-Seasonal)
- Converted stock prices to daily returns to achieve stationarity
- Evaluated stationarity using the Augmented Dickey-Fuller (ADF) test
- Analyzed ACF and PACF plots to identify candidate models
- Fitted AR, MA, and ARMA models
- Selected the final model using Akaike Information Criterion (AIC)
- Performed residual diagnostics to confirm white noise behavior

**Final Model:** ARMA(1,1)

---

### Economic Time Series (Seasonal)
- Identified trend and seasonality using ACF and PACF plots
- Applied first-order differencing and seasonal differencing (period = 12)
- Fitted multiple SARIMA models with fixed seasonal structure
- Selected the optimal model using AIC
- Validated model adequacy using residual diagnostics and Ljung-Box test

**Final Model:** SARIMA(1,1,1)(1,1,1)[12]
