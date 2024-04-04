# Amazon Stock Price Forecasting

This repository contains a Python script that demonstrates the process of forecasting Amazon's stock prices using an LSTM (Long Short-Term Memory) neural network. The script processes historical stock price data, trains an LSTM model, and makes predictions on the stock's future closing prices. I started this project to learn more about LSTMs.

## Overview

The script utilizes `pandas` for data manipulation, `numpy` for numerical operations, `matplotlib` for plotting, and `torch` with its neural network module for building and training the LSTM model.

The data for Amazon's stock prices (`AMZN.csv`) includes the following columns: Date, Open, High, Low, Close, Adj Close, and Volume. The script focuses on the 'Date' and 'Close' columns to forecast the closing prices.

## Data Processing

The data is first loaded and then narrowed down to two columns: 'Date' and 'Close'. The 'Date' column is converted to a datetime format, and the data is visualized to show the stock's closing prices over time.

The script then prepares the data for the LSTM model by creating a shifted dataframe, where the closing prices are shifted to create a series of input sequences for the model to learn from. This data is then scaled using MinMaxScaler to improve the training process.

## LSTM Model

An LSTM model is defined with specific input size, hidden layer size, and number of layers. The model includes an LSTM layer followed by a fully connected layer to predict the closing price.

## Training and Validation

The dataset is split into training and testing sets, and the model is trained over several epochs, printing the loss after every epoch to monitor the training process. After training, the model's performance is evaluated on the testing set.

## Prediction and Visualization

The script makes predictions on the training and testing sets and inversely transforms the predicted values to compare them with the actual stock prices. Plots are generated to visualize the actual vs. predicted closing prices for both sets.

## Usage

To run this script, ensure you have the necessary libraries installed (`pandas`, `numpy`, `matplotlib`, `torch`) and the `AMZN.csv` file in your directory. Execute the script using Python, and it will process the data, train the model, and display the plots showing the forecasted stock prices.

