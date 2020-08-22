# Stock Prediction: Project Overview 
* Building a stock prediction model using LSTM (Long-Short Term Memory) Algorithm
* Data used was a daily stock prices of 500 companies from 2013 to 2018 from Kaggle
* Data consisted with 7 columns and 1259 rows for each company
* Model predicts open stock prices of GOOGL
* Building visualization for prediction model plot

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, sklearn, numpy, matplotlib, keras, TensorFlow

## Dataset
To predict stock using LSTM, datased used was a daily stock prices of 500 companies from 2013 to 2018 with details are following:
*	Name
*	Date
*	Open
*	High
*	Low 
* Close
* Volume
<br />In this project I chose to predict open stock price for 1 company, which is GOOGL

## Data Pre-Processing
First, I did a feature scaling to the data to get optimal performance by using Scikit- Learn’s MinMaxScaler and scale the dataset to numbers between zero and one.
<br />After that, since LSTM expect data to be in 3D format, I converted the data into a 3D dimension array with X_train samples, 60 timestamps, and one feature at each step.

<br />![](https://github.com/novaldi21/ds_stock_prediction/blob/master/Stock_Prediction.png)
