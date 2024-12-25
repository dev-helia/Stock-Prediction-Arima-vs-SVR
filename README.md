
# Stock Returns Prediction: Comparison between ARIMA and SVR

This repository contains the implementation of **ARIMA** and **Support Vector Regression (SVR)** models for predicting stock returns. The study compares these two models using data from major stock indices, showcasing the strengths of machine learning techniques over traditional statistical methods.

## Project Overview

### Background
Forecasting stock prices and returns is a challenging yet critical task for financial markets. Traditional statistical models like ARIMA and advanced machine learning models like SVR are commonly used for this purpose. This project aims to:
- Compare the performance of **ARIMA** and **SVR** models on historical stock data.
- Highlight the advantages of machine learning in capturing non-linear relationships in time series data.

### Key Contributions
1. **Comprehensive Model Comparison**: Evaluation of ARIMA and SVR using performance metrics such as RMSE, MSE, and MAE.
2. **Feature Engineering**: Use of ACF/PACF for time series stationarity checks and grid search for optimal hyperparameter selection.
3. **Data Insights**: Analysis of four major stock indices, including NASDAQ, S&P 500, Dow Jones, and NYSE Composite.

## Dataset
The dataset consists of **logarithmic daily returns** of four major indices:
- **NASDAQ Composite**
- **S&P 500**
- **Dow Jones Industrial Average**
- **NYSE Composite**

The data spans from **January 1, 2012** to **September 1, 2023**, obtained from Yahoo Finance. It includes:
- Opening prices
- Closing prices
- High and low prices

## Results
The experimental results demonstrate that **SVR** consistently outperforms **ARIMA** in terms of prediction accuracy across all indices:

| Model   | RMSE       | MSE        | MAE        |
|---------|------------|------------|------------|
| **ARIMA** |            |            |            |
| Dow Jones | 0.010171   | 0.000103   | 0.007645   |
| S&P 500   | 0.011882   | 0.000141   | 0.008936   |
| NASDAQ    | 0.015607   | 0.000244   | 0.011872   |
| NYSE      | 0.010569   | 0.000112   | 0.008043   |
| **SVR**   |            |            |            |
| Dow Jones | **0.002758** | **0.000008** | **0.002133** |
| S&P 500   | **0.002944** | **0.000009** | **0.002323** |
| NASDAQ    | **0.002158** | **0.000005** | **0.001693** |
| NYSE      | **0.001313** | **0.000002** | **0.001029** |

## Model Descriptions

### ARIMA
The **ARIMA model** is a linear statistical approach comprising:
1. **Autoregressive (AR)**: Dependency on past values.
2. **Integrated (I)**: Differencing to achieve stationarity.
3. **Moving Average (MA)**: Dependency on past error terms.

### SVR
**Support Vector Regression (SVR)** is a machine learning model that captures non-linear relationships using:
1. Kernel functions (e.g., RBF).
2. Hyperparameters such as **C** and **epsilon**.
3. Feature extraction techniques like PCA.

## Installation and Usage

### Requirements
Install required Python libraries:
```bash
pip install -r requirements.txt
```

### Running the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/river-d/Stock-Returns-Prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Stock-Returns-Prediction
   ```
3. Train and test the models:
   - **ARIMA**:
     ```bash
     python arima_model.py
     ```
   - **SVR**:
     ```bash
     python svr_model.py
     ```
4. View the results:
   Output will include RMSE, MSE, MAE, and visualizations of predicted vs. actual values.



## Contact
For questions or feedback, contact:
- **Tao He**: [Email](mailto:hetaoo.c@gmail.com)
