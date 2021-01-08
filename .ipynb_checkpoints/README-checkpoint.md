# LSTM-Stock-Predictor
This project is related to Deep Learning, specifically, using custom LSTM RNNs (Recurrent Neural Networks) to predict cryptocurrency prices.  One RNN is based on actual Closing Prices, while the other RNN is based on the Fear and Greed Index (FNG).  The goal is to determine which model provides a better signal for cryptocurrency closing prices.

## First Graph

## Conclusion:
Comparing this model, which uses a 10 day window of Bitcoin closing prices, to the other model, which uses a 10 day window of Bitcoin fear and greed index values, the Closing Prices model appears to be better:
- Closing Prices Loss: 0.0616.  Fear & Greed Loss: 0.1219.
- Tracking Values over Time: The model based on closing prices appears to track the actual values better over time than does the model based on the Fear & Greed Index.  Comparing the charts for the two models of Real vs. Predicted values over time, the predictions based on Closing Prices more closely reflect the true values than do the predictions based on the Fear & Greed Index.
- Which window size works best for this specific model: