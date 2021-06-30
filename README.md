# HW-DeepLearning-LSTM-RNN-Price-Predictor

## Background

We did witness an increase of volatility in the crypto market with a major retracement in almost all coins since May 2021. Many reasons are explaining this movement, from Elon Musk tweets to China government new laws and of course the environment impact concern. Sentiment became an increasingly important factor in the crypto market. Investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One indicator that emerged is the Crypto Fear and Greed Index (FNG) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency.
In this notebook, we are looking to build and compare two deep learning models, one based on the FNG values and the other on the simple closing prices. The idea is to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.
We used a LSTM RNN model (Long short-term memory) Recurrent Neural Network) to build the two models. To compile the models we used the adam optimizer, and mean_square_error as loss function since the value we want to predict is continuous.

## Price based model results

 ![CLOSING PRICE MODEL]('../Image/../../Image/Closing%20price%20model.png)

## FnG based model results

 ![FNG MODEL]('../Image/../../Image/FnG%20model.png)

## Conclusion

While working on this simulation, we tried to answer three key questions :

1. Which model has a lower loss?

We can conlude that the model based on previous prices (using prices as features) present a significantly better performance  than the one based on the "fear and greed"(FnG) index (using the FnG score as features).

In our model, we ended up with a loss function of 0.003 for the price based model Vs 0.082 for the FnG one.

2. Which model tracks the actual values better over time?

Similar to the loss fonction, the price based model tracks pretty well the actual values (conf chart above).

3. Which window size works best for the model?

Interestingly enough, we would think that the longer the window is the better (i.e based on the belief that the more inputs the better). But by comparing the results of a 10-days, 5-days, 2-days and 1-day window, we can conclude that the 2-days window provides the best output.
