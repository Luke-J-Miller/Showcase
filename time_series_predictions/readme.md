# Stock Price Predictor using LSTM and ARIMA

This repository contains an exploration of stock price prediction using Long Short-Term Memory (LSTM) and AutoRegressive Integrated Moving Average (ARIMA) models. 

The main purpose of this project is to demonstrate how we can leverage both Machine Learning (LSTM) and traditional statistical models (ARIMA) to predict stock prices. This project should serve as a starting point for more sophisticated models and feature engineering.

## Overview

We use LSTM, a type of Recurrent Neural Network (RNN) that is capable of learning long-term dependencies, which is ideal for time-series data like stock prices. We also utilize the ARIMA model, a popular statistical method for time-series forecasting. 

The project involves the following steps:

- Fetching and preprocessing the stock data.
- Implementing and training an LSTM model.
- Implementing an ARIMA model.
- Making predictions using both models.
- Evaluating the performance of the models.
- Visualizing the predictions.

## Results

After training our LSTM and ARIMA models on 80% of the data, we then tested these models on the remaining 20% of the data. Our LSTM model achieved a Root Mean Squared Error (RMSE) of 12.15%.

Our LSTM model's predictions visualization:

![LSTM Predictions Visualization](./lstm_visualization.png)

ARIMA model's predictions visualization:

![ARIMA Predictions Visualization](./arima_visualization.png)

## Future Work

Future work includes:

- Performing more extensive feature engineering.
- Tuning the hyperparameters of the models for better performance.
- Trying ensemble methods to combine predictions from multiple models.
- Incorporating domain knowledge to make better predictions.
- Improving the robustness of our model's evaluation.
- Implementing more robust error handling and testing.

## Acknowledgements

This project was made possible by using data provided by Alpha Vantage's API. 

## Usage

To run the scripts, you will need to install several dependencies. Refer to the code and comments in `check_installed_and_import()` function.

You will also need an Alpha Vantage API key. This should be placed in a text file at the path specified in the script (`/kaggle/input/api-key/API_KEY.txt` by default).

---

Please feel free to fork this project, submit issues, and contribute to improving it. Pull requests are welcome!
