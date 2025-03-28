
# Stock Prediction with TFT model and News Sentiments 
<img width="650" alt="image" src="https://github.com/user-attachments/assets/74856233-d4b8-4d0f-bc95-0d22254fe9e6" />

## About this Project  

Instead of commonly used LSTM model. This project utilized state-of-art attention model, TFT(Temporal Fusion Transformer) model, with sentiment analysis of financial news to create powerful stock prediction model. 


## Objective 
The Objective of this model is to predict stock price of next day. The model takes various market indicators as well as financial news as the features used for prediction. 

## Data Collection 
This notebook contains script to collect daily stock data and financial news related to each company. Top 100 S&P companies stock data and related financial news. After getting the data, finbert model is used to compute sentiment for each news

## Feature Engineering & Data Pre-processing
Process the data and create features that are useful for the prediction. The notebook contains examples of feature engineering. Features includes:
- Moving Average
- Log history
- Market Index (such as Nasdaq)
- Volatality Index
- Sector Index
- Computed Sentiment Scores of Financial News

## Model Development & Training
The next notebook show how you can define TFT model, tune hyperparameter, and training the model
### Hyperparmeter Tuning
Use pen source hyperparameter tuner Optuna to find the best set of hyperparameters
### Model Training
Train the model with the computed hyperparameters. Apply techniques such as early stopping and learning schedule to save the best model.

## Evaluation & Visualization
Use the trained model to make prediction. Plot the resultd and visualize how close the model predicted compared to actual stock price

<img width="593" alt="image" src="https://github.com/user-attachments/assets/bb919b09-cf3e-45c8-ad61-fbe4dd44df9d" />
<img width="650" alt="image" src="https://github.com/user-attachments/assets/74856233-d4b8-4d0f-bc95-0d22254fe9e6" />
<img width="622" alt="image" src="https://github.com/user-attachments/assets/1cdf1028-87f4-4183-ac36-e106f3439719" />

