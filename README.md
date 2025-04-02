
# 📈 Forecasting Anti-Diabetic Drug Sales Using ARIMA (1,2,1)

This project applies time series forecasting using the **ARIMA(1,2,1)** model to monthly anti-diabetic drug sales data from Australia. The goal is to create a reliable demand forecast and generate actionable insights for healthcare supply planning.

---

## 📊 Dataset Overview

- **Source:** Australian Government (`a10.csv`)
- **Period:** Jan 1991 – Dec 2008 (monthly)
- **Variable:** Monthly sales of anti-diabetic drugs (in AUD millions)
- **Observations:** 216 data points

---

## 🔧 Technologies & Libraries

- Python 3.x
- `pandas`, `numpy`, `matplotlib`
- `statsmodels` (ARIMA, ADF test)
- `sklearn` (for RMSE/MAE)

---

## 📉 Methodology

1. **Stationarity Check**
   - Used ADF test on the original and second-order differenced series
   - Confirmed stationarity with second-order differencing

2. **Model Selection**
   - PACF → p = 1
   - ACF → q = 1
   - Differencing → d = 2  
   → Final model: **ARIMA(1,2,1)**

3. **Train-Test Split**
   - Trained on data until Dec 2007
   - Forecasted for Jan–Dec 2008

---

## ✅ Results

| Metric | Value   |
|--------|---------|
| **RMSE** | 3.43    |
| **MAE**  | ~2.87   |
| **AIC**  | 808.37  |

---

## 📈 Visuals

- Forecast vs. actual sales plotted month-by-month
- Forecast aligns well with historical trends
- Absolute error was low across the test period

---

## 💡 Business Insights

- Demand for anti-diabetic drugs is growing steadily
- Forecasting helps improve:
  - 📦 Inventory planning
  - 🧾 Budgeting
  - ⏱️ Procurement timing
- The model supports **healthcare supply chain optimization**

---

## 🔁 Next Steps

- Extend model with **SARIMA** for seasonality
- Deploy via dashboard for ongoing planning
- Use `auto_arima` for automated model tuning

---

## 📁 Files Included

- `arima_forecast.py`: Full model code and forecast logic
- `forecast_plot.png`: Visualization of results
- `forecast_comparison.csv`: Forecast vs actual values with error
- `README.md`: Project summary (this file)

---

## 🤝 Let’s Connect

If you're working on healthcare analytics, forecasting, or data-driven supply planning, feel free to connect!
