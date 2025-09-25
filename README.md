# 📊 Stock Price Forecasting using ARIMA  

This project focuses on forecasting **TCS (Tata Consultancy Services)** stock prices using **time series analysis** and the **ARIMA (AutoRegressive Integrated Moving Average)** model.  
The goal is to model historical stock price trends and forecast future values, which is highly relevant in finance and trading.  

---

## 📌 Introduction  
Stock market prediction is a classic problem in finance and data science.  
In this project, we:  
- Cleaned and preprocessed **TCS stock price data**.  
- Performed **stationarity tests** and transformations.  
- Built an **ARIMA model** for forecasting.  
- Visualized forecasts with confidence intervals.  

---

## 🎯 Objectives  
- Prepare and clean stock market time series data.  
- Handle duplicates, missing values, and date irregularities.  
- Check and ensure stationarity using **ADF test**.  
- Train and evaluate an **ARIMA model**.  
- Forecast **future TCS stock prices** with visualizations.  

---

## 📂 Dataset  
- **Company:** Tata Consultancy Services (TCS)  
- **Type:** Daily stock price data (Closing price)  
- **Characteristics:**  
  - Indexed by **DateTime**  
  - Missing values on weekends and holidays  
  - Occasional duplicate entries  

---

## 🔧 Methodology  

### 1️⃣ Data Preprocessing  
- Removed duplicate records by date.  
- Converted dataset index to **DateTimeIndex**.  
- Forward-filled missing values and set frequency to **Business Days (B)**.  

### 2️⃣ Exploratory Data Analysis  
- Computed **rolling mean** and **exponential weighted mean**.  
- Analyzed **quarterly high/low prices**.  
- Visual inspection revealed the data was **non-stationary**.  

### 3️⃣ Stationarity Check  
- **Augmented Dickey-Fuller (ADF) Test:**  
  - Initial p-value > 0.05 → Data is **non-stationary**.  
  - Applied **first-order differencing**.  
  - New p-value < 0.05 → Data is now **stationary**.  

### 4️⃣ Model Building (ARIMA)  
- Used **ACF and PACF plots** to determine AR (`p`) and MA (`q`) terms.  
- Built ARIMA(p,d,q) with `d=1`.  
- Trained the model on **TCS stock prices**.  

### 5️⃣ Forecasting  
- Forecasted **future TCS stock prices**.  
- Plotted results with **confidence intervals**.  

---

## 📊 Results  
- Differencing made the series stationary.  
- ARIMA successfully modeled and forecasted TCS stock prices.  
- Forecast plots aligned with realistic stock market trends.  

---

## ⚙️ Tools & Libraries  
- Python 3.8+  
- Pandas  
- NumPy  
- Matplotlib / Seaborn  
- Statsmodels  

---

## 🔮 Future Work  
- Extend model to **SARIMA** for seasonality.  
- Compare with **LSTM/GRU deep learning models**.  
- Include **volume, sentiment, and macroeconomic indicators**.  
- Deploy as a **real-time dashboard** (Flask / Streamlit / Dash).  

---

## 🙌 Acknowledgements  
- TCS Stock Price Data (publicly available financial datasets, e.g., Yahoo Finance).  
- `statsmodels` ARIMA documentation.  
- Tutorials on time series forecasting and stationarity testing.  

---

✨ *"Forecasting tomorrow’s market with today’s data."* 📈  
