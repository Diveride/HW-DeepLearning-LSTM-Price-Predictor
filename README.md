# HW-DeepLearning-LSTM-RNN-Price-Predictor

## Background

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the Crypto Fear and Greed Index (FNG) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. 
In this notebook, we are looking to build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.
To build the model, we used deep learning recurrent neural networks to model bitcoin closing prices. One model uses the FNG indicators to predict the closing price while the second model will uses a window of closing prices to predict the next closing price.
We used a LSTM RNN model (Long short-term memory) Recurrent Neural Network). To compile the models I used the adam optimizer, and mean_square_error as loss function since the value we want to predict is continuous.


## Price based model results 



## FnG based model results

## Conclusion

While working on this simulation, we tried to answer three key questions : 

1. Which model has a lower loss?

We can conlude that the model based on previous prices (using prices as features) present a significantly better performance  thank the one based on the "fear and greed"(FnG) index (using the Fear and greed score as features)
In our model, we ended up with a loss function of 0.003 for the price based model Vs 0.082 for teh FnG one. 

2. Which model tracks the actual values better over time?

Similar to the loss fonction, the price based model tracks pretty well the actual values (conf chart above).

3. Which window size works best for the model?

Interestingly enough, we would think that the longer the window is the better (i.e based on the belief that the more inputs the better. But by comparing the results of a 10-days, 5-days, 2-days and 1-day window, we can conclude that the 2-days window provides the best output. 





