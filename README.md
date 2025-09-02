#  Stock Market Time Series Analysis & Forecasting  

This project applies **time series analysis** to stock market data, focusing on returns forecasting using classical statistical models. Using Apple (AAPL) stock data from 2015–2023, it demonstrates data preprocessing, exploratory analysis, and implementation of **ARIMA and SARIMA models** for forecasting.  

---

##  Key Features  
- **Data Collection**: Historical stock data retrieved via `yfinance`  
- **Exploratory Analysis**: Visualization of stock prices and daily returns  
- **Data Splitting**: Training (80%) and testing (20%) sets for model validation  
- **Forecasting Models**:  
  - **ARIMA** – Autoregressive Integrated Moving Average  
  - **SARIMA** – Seasonal ARIMA with weekly seasonality  
- **Custom Evaluation Metrics**:  
  - MAE (Mean Absolute Error)  
  - RMSE (Root Mean Square Error)  
  - MAPE (Mean Absolute Percentage Error)  
  - Directional Accuracy (trend prediction capability)  
- **Visualization**: Forecast plots with confidence intervals for comparison  

---

##  Dataset  

The dataset is sourced directly from **[Yahoo Finance](https://finance.yahoo.com/)** using the Python library `yfinance`.  

- **Ticker Used**: Apple Inc. (**AAPL**)  
- **Time Period**: January 2015 – December 2023  
- **Data Fields**: Open, High, Low, Close, Adj Close, and Volume  
- **Focus**: The **Closing Price** was extracted and converted into **daily returns** for time series forecasting.  

This approach ensures the dataset is always **up-to-date and reproducible** without requiring manual file uploads.  

---

##  Results  

The models were evaluated on Apple (AAPL) daily returns using standard error metrics.  

| Model  | MAE   | RMSE  | MAPE   | Directional Accuracy |
|--------|-------|-------|--------|-----------------------|
| ARIMA  | 0.0134 | 0.0182 | ∞ (due to near-zero returns) | 53% |
| SARIMA | 0.0135 | 0.0183 | ∞ (due to near-zero returns) | 53% |

 Both **ARIMA** and **SARIMA** provided similar performance in terms of error metrics.  
 **Directional accuracy (~53%)** shows the models were only slightly better than random guessing for predicting the direction of returns.  
 MAPE is reported as **infinite** because stock returns can be very close to zero, making percentage errors unstable.  

---

##  Conclusion  

- Classical time series models like **ARIMA** and **SARIMA** can capture patterns in stock returns but have **limited predictive power**.  
- Forecasting stock market **returns** is inherently challenging due to noise and volatility.  
- The results highlight the importance of exploring **more advanced approaches** (e.g., LSTM, Prophet, hybrid models) for better predictive performance.  

---

##  Tech Stack  
- Python  
- yfinance  
- statsmodels  
- scikit-learn  
- matplotlib & plotly  

---
