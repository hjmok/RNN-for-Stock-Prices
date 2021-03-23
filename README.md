# RNN-for-Stock-Prices

For this project, an RNN model using LSTM predicts the upward and downward trends of Google and AMD stock prices.

## Dataset and Library
Tensorflow was used as the main module for this model.
The two datasets both contain 2336 rows of data, one for each week day. The two columns of interest are 'Date' and 'Open'. 
The datasets be found the from following link:
https://www.kaggle.com/gunhee/amdgoogle

## RNN Model
For the model input, two sequence sizes were test. The first sequence size was 66. This is due to quarterly earnings reports being once every 3 months, which encompasses roughly 66 financial days. The second sequence size experimented on was 261, which is the number of financial days in a year. In addition, the RNN will predict 1 day into the future for every 66 or 261 weekdays before it.

The model has 4 pairs of LSTM and Dropout layers. Each LSTM layer contains 50 neurons, with a dropout rate of 40% to reduce overfitting. After the 4th LSTM layer, a fully connected layer outputs the final predicted value 1 day into the future. The loss metric used is Mean Squared Error, since this is a regression problem. The Adam optimizer was used for this model. 

## RESULTS
For details on the results, please visit the following: https://hjmok.github.io/josephmok_portfolio/#/StockPriceRNN
