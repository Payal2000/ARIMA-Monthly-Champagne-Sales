# 📈 ARIMA Forecasting on Monthly Champagne Sales

This project demonstrates the application of ARIMA and Seasonal ARIMA modeling for time series forecasting using monthly champagne sales data. The workflow includes visualization, stationarity checks, differencing, correlation analysis, and prediction.



## 📂 Dataset

**Source:**  
[Perrin Freres Monthly Champagne Sales (1964–1972)](https://raw.githubusercontent.com/Payal2000/ARIMA-Monthly-Champagne-Sales/refs/heads/main/perrin-freres-monthly-champagne-.csv)

**Features:**
- `Month`: Time period from January 1964 to September 1972
- `Sales`: Champagne sales in millions



## 🔍 Project Workflow

### 1. Visualize the Time Series Data
- Plot the raw sales data.
- Observations:
  - 📈 Increasing trend
  - 🔁 Clear annual seasonality
  - 📊 Rising variance over time

### 2. Make the Time Series Stationary
- First-order differencing to remove trend.
- Seasonal differencing with lag=12 to eliminate seasonality.

### 3. Test for Stationarity
Used **Augmented Dickey-Fuller (ADF) Test**:

- **Before differencing:**
  - ADF Statistic ≈ -1.83
  - p-value ≈ 0.36 → Not stationary
- **After seasonal differencing:**
  - ADF Statistic ≈ -7.62
  - p-value ≈ 2e-11 → Strongly stationary

### 4. Plot ACF and PACF Charts
- **ACF (Autocorrelation Function)**: Helps determine MA (q) terms.
- **PACF (Partial Autocorrelation Function)**: Helps determine AR (p) terms.

### 5. Build ARIMA / SARIMA Model
- Parameters selected based on ACF/PACF plots and differencing (d, D).
- Used to model and forecast champagne sales for future months.

### 6. Forecast Future Steps
- Predict future values using the trained ARIMA/SARIMA model.
- Visualize predicted values against actual sales.



## 🛠️ Technologies Used

- Python (Pandas, Matplotlib, Statsmodels)
- Google Colab
- Time Series Analysis
- ARIMA/SARIMA Modeling



## 📌 Key Learnings

- ARIMA requires a stationary series (constant mean and variance).
- Seasonal differencing is effective for monthly data with yearly cycles.
- ACF and PACF plots are critical for identifying model parameters.
- Proper preprocessing is essential for accurate time series forecasting.



