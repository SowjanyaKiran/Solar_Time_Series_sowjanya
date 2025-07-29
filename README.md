# ⚡ Load & Solar Generation Forecasting using Time Series Analysis (ARIMA & SARIMA)
This project uses ARIMA and SARIMA time series models to forecast Italy’s hourly electricity load and solar generation.
It covers EDA, stationarity checks, seasonal analysis, model building, and forecasting to compare model performance.

#  📂 Dataset
Source: Italy 2016 Load & Solar Generation Data

# Frequency: Hourly readings

# Features:

utc_timestamp → Date & time (UTC)

IT_load_new → Electricity load in MW

IT_solar_generation → Solar generation in MW

# 🛠️ Project Workflow
1️⃣ Install Dependencies
bash
Copy
Edit
pip install pandas matplotlib seaborn statsmodels scikit-learn
2️⃣ Data Preprocessing
Convert timestamps to datetime format

Handle missing values using forward fill

Remove flat periods if necessary

Visualize trends for load & solar generation

3️⃣ Stationarity Check
ADF Test to determine stationarity

Apply differencing if needed

4️⃣ ACF & PACF Plots
Identify AR & MA orders

Seasonal patterns observed at daily level (m=24)

5️⃣ Model Building
ARIMA: (p, d, q)

SARIMA: (p, d, q, m) with seasonal component

Train on 80% of the data, test on 20%

6️⃣ Model Evaluation
Compare RMSE for ARIMA & SARIMA

SARIMA captures seasonality better

# 🧠 Model Summary
Load Forecasting:

ARIMA (2, 0, 2) → RMSE: 7714.95

SARIMA (2, 0, 2, 24) → RMSE: 5611.62

Solar Generation Forecasting:

ARIMA (2, 0, 7) → RMSE: 2484.25

SARIMA (1, 0, 1, 24) → RMSE: 1379.21

# ✅ SARIMA performs better for both series.

# 📊 Results
SARIMA captures daily seasonality (m=24)

Lower RMSE values compared to ARIMA

Forecasts closely follow actual trends in test data

# 💻 Tech Stack
Python

Pandas, Matplotlib, Seaborn

Statsmodels

Scikit-learn

# 📁 License
Educational use only. Dataset belongs to its respective provider.

# 👤 Author
Sowjanya Kiran
📧 usowjanyakiran@gmail.com
🌐 [GitHub](https://github.com/SowjanyaKiran/Solar_Time_Series_sowjanya/)

