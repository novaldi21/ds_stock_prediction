# Stock Prediction: Project Overview 
* Building a future stock prediction model using LSTM (Long-Short Term Memory) Algorithm
* Data used was a daily stock prices of 500 companies from 2013 to 2018 from Kaggle
* Data consisted with 7 columns and 1259 rows for each company
* Model predicts open stock prices of GOOGL
* Building visualization for prediction model plot

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, sklearn, numpy, matplotlib, keras, TensorFlow.

## Dataset
To predict future stock using LSTM, datased used was a daily stock prices of 500 companies from 2013 to 2018 with details are following:
*	Name
*	Date
*	Open
*	High
*	Low 
* Close
* Volume
<br />In this project, I chose to predict open stock price for 1 company, which is GOOGL open stock prices.

## Data Pre-Processing
First, I did a feature scaling to the data to get optimal performance by using Scikit- Learn’s MinMaxScaler and scale the dataset to numbers between zero and one.
<br />After that, since LSTM expect data to be in 3D format, I converted the data into a 3D dimension array with X_train samples, 60 timestamps, and one feature at each step.

## Model Building 

First, I built the LSTM model before building the test set. The LSTM model building used Keras library with several adjustments, which are:
<br />1. Adding 50 units which is the dimensionality of the output space to prevent overfitting.
<br />2. Defining Dropout layers by 0.2, meaning that 20% of the layers will be dropped.
<br />3. Adding Dense layer that specifies the output of 1 unit.
<br />4. compile the model using adam optimizer and set the loss as the mean_squarred_error. This will compute the mean of the squared errors.
<br />After adjustments, we fit the model to run on 100 epochs with a batch size of 32.

Finally, I did the future stock prediction of GOOGL open price by merging the training set and the test set on the 0 axis, set the time step as 60, used MinMaxScaler to transform the new dataset, and reshaped the dataset afterward.

The code for model building can be seen [here](https://github.com/novaldi21/ds_stock_prediction/blob/master/Stock_Prediction.ipynb)

## Model plotting
The model plotting visualization between the real price and predicted price presented in the figure below. 
<br />![](https://github.com/novaldi21/ds_stock_prediction/blob/master/Stock_Prediction.png)

From the figure it can be seen that the prediction tools was able to predict the open stock price of GOOGL based on the plot movement on the graph.
