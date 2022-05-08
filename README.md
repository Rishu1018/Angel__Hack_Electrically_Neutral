# NASDAQ-Forecasting-With-Stacked-LSTM

Made a Deep learning model, which could predict NASDAQ stock prices (National Association of Securities Dealers Automated Quotations).
The NASDAQ stock price dataset was obtained from YAHOO Finance. Dataset included opening and closing prices of the last five years (September 2016 to September 2021).
Before fitting the data to our model, it had to be preprocessed :
1) LSTM model works efficiently with scaled values of data, so it was scaled with MinMaxScaler using sklearn.preprocessing library.
2) The dataset was then split into training and test set with 80 % of data for training while 20 % for testing.
3) To feed the data to our model, we need to split the data into discrete values, i.e., features and values.
4) Since the LSTM model takes input a 3 Dimensional array, the 2 Dimension array was expanded to 3 Dimensions.

The model was built using Tensorflow Sequential API :
1) A stacked LSTM was made with three LSTM layers, two Dropouts layers, and one final output layer.
2) Since our task was stock price prediction, mean squared error loss was used with ‘adam’ optimizer for gradient descent.
3) LearningRateScheduler was used as a callback. With the help of callback, we can customize our model; I was able to decrease the learning rate by 2% after every two epochs using LearningRateScheduler.

Google Colab Project : https://colab.research.google.com/drive/1OfA9R0ePR88ibLOIBDGmj3mDABfdanNh?usp=sharing

![alt text](https://miro.medium.com/max/1400/1*xR4m0oOKz_jRgQU4Oge53g.jpeg)

