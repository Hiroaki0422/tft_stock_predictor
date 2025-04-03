# Daily Stock Price Forecasting with TFT and News Sentiment Analysis

<img width="650" alt="architecture" src="https://github.com/user-attachments/assets/74856233-d4b8-4d0f-bc95-0d22254fe9e6" />

## 📈 About This Project  
This is a personal project to develop a daily stock price forecasting model using a state-of-the-art attention-based time series model — the **Temporal Fusion Transformer (TFT)**. The model also incorporates sentiment from financial news to improve prediction performance.

---

## 🧠 Model Development

[📓 Notebook for Data Collection & Sentiment Computation](https://github.com/Hiroaki0422/tft_stock_predictor/blob/main/notebook/tft-data-process.ipynb)

### 🎯 Objective  
The model aims to predict the next day’s stock price using a mix of numerical indicators and sentiment scores extracted from financial news. Categorical variables like the month of the year are also used — which the TFT model handles effectively.

### 📊 Data Collection  
- 10 years of historical stock prices for the top 100 S&P 500 companies via Yahoo Finance  
- 10 years of financial news articles matched to corresponding stock tickers  

### 💬 Sentiment Analysis  
- Uses the open-source **FinBERT3** model to assign sentiment scores (scaled -1 to 1) to financial news articles on a per-symbol, per-day basis.

---

## 🔧 Feature Engineering

[📓 Notebook for Feature Engineering](https://github.com/Hiroaki0422/tft_stock_predictor/blob/main/notebook/tft-process-historical-data.ipynb)

Key features engineered include:

- Moving Averages  
- Log Returns  
- Market Index (e.g., NASDAQ)  
- Volatility Index (VIX)  
- Sector Index  
- Sentiment Scores from News  

---

## 🛠️ Data Transformation & Model Training

[📓 Notebook for Model Training & Evaluation](https://github.com/Hiroaki0422/tft_stock_predictor/blob/main/notebook/tft-trainer.ipynb)

- Built using the **PyTorch Forecasting** library  
- Simplifies data transformation and model implementation  
- **Optuna** is used for hyperparameter tuning  
- Training includes techniques like early stopping and learning rate scheduling  
- Best model is saved and evaluated  

---

## 📉 Evaluation & Visualization

Evaluate the trained model's predictions and visualize the results to compare against actual stock prices:

<img width="400" alt="chart1" src="https://github.com/user-attachments/assets/bb919b09-cf3e-45c8-ad61-fbe4dd44df9d" />
<img width="400" alt="chart2" src="https://github.com/user-attachments/assets/74856233-d4b8-4d0f-bc95-0d22254fe9e6" />
<img width="400" alt="chart3" src="https://github.com/user-attachments/assets/1cdf1028-87f4-4183-ac36-e106f3439719" />

---

## 🔄 MLOps & Deployment

For real-time inference and automated model updates, check out the MLOps version of this project:

[📦 MLOps-Enabled Version (tft_stock_preds_mlops)](https://github.com/Hiroaki0422/tft_stock_preds_mlops)
