# Stock Price Forecasting

In this project, our primary focus was on forecasting the closing price of stocks for the next trading day through an analysis of historical stock price data. Initially, we implemented Long Short-Term Memory (LSTM) to capture short-term patterns and forecast the day's closing prices. Additionally, we utilized feature engineering techniques, incorporating the previous day's [open, high, low, close, volume] as input features for predicting the current day's close price. This approach effectively captured short-term trends. Currently, our aim is to enhance the model's capabilities by exploring various deep learning and traditional machine learning techniques, along with further feature engineering on the data.

## Dataset

- Source: [Yahoo Finance](https://in.search.yahoo.com/?fr2=inr)

Initially, we used the last 12 years' stock price data of Amazon. We split this dataset into the below category

#### Train: 2010 - 2020

#### Validation: 2021 - 2021

#### Test: 2022 - 2022

## Workflow

```mermaid
stateDiagram-v2
    DataCollection --> DataPreprocessing
    DataPreprocessing --> EDA
    EDA --> Modeling
    Modeling --> ModelEvaluation
    ModelEvaluation --> ModelPerformance
    ModelPerformance --> Modeling: Bad
    ModelPerformance --> Forecasting: Good
    Forecasting --> Deployment

```
## Result
| Model | Loss | Val Loss | RMSE |
|----------|----------|----------|----------|
| LSTM   | 0.0044   | 0.0521   | 0.085   |

Note: RMSE calculated without performing inverse transform. In the next update, we'll gonna update the RMSE score.

## Acknowledgements

 - [Machine Learning Mastery](https://machinelearningmastery.com/persistence-time-series-forecasting-with-python/)

