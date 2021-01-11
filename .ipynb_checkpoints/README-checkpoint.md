# LSTM Stock Predictor
This project is related to Deep Learning, specifically, using custom LSTM RNNs (Recurrent Neural Networks) to predict cryptocurrency prices.  One RNN is based on actual Bitcoin closing prices, while the other RNN is based on the Bitcoin Fear and Greed Index (FNG).  The goal is to determine which model provides a better signal for cryptocurrency closing prices.

Please note, this notebook was created in Google Colab, downloaded to local computer as a .ipynb, and then uploaded to Jupyter Notebook.  Mac Big Sur does not run TensorFlow within Jupyter Lab, so it was necessary to run the actual code in Google Colab, and *then* copy that .ipynb to Jupyter Lab.

### 10-day window Bitcoin Closing Prices Model:
#### Loss:
![closing_price_10_day_loss](/Screenshots/closing_price_10_day_loss.png?raw=true)
#### Real vs. Predicted Values:
![closing_price_10_day_real_predicted](/Screenshots/closing_price_10_day_real_predicted.png?raw=true)

### 5-day window Bitcoin Closing Prices Model:
#### Loss:
![closing_price_5_day_loss](/Screenshots/closing_price_5_day_loss.png?raw=true)
#### Real vs. Predicted Values:
![closing_price_5_day_real_predicted](/Screenshots/closing_price_5_day_real_predicted.png?raw=true)


### 10-day window Bitcoin Fear and Greed Index Model:
#### Loss:
![fg_10_day_loss](/Screenshots/fg_10_day_loss.png?raw=true)
#### Real vs. Predicted Values:
![fg_10_day_real_predicted](/Screenshots/fg_10_day_real_predicted.png?raw=true)

### 5-day window Bitcoin Fear and Greed Index Model:
#### Loss:
![fg_5_day_loss](/Screenshots/fg_5_day_loss.png?raw=true)
#### Real vs. Predicted Values:
![fg_5_day_real_predicted](/Screenshots/fg_5_day_real_predicted.png?raw=true)

## Conclusions:
### Comparing 10 day window of Bitcoin closing prices model to 10 day window of Bitcoin fear and greed index values model: the Closing Prices model appears to be better:
- Closing Prices Loss: 0.0616.  Fear & Greed Loss: 0.1219.
- Tracking Values over Time: The model based on closing prices appears to track the actual values better over time than does the model based on the Fear & Greed Index.  Comparing the charts for the two models of Real vs. Predicted values over time, the predictions based on Closing Prices more closely reflect the true values than do the predictions based on the Fear & Greed Index.

### Comparing 10 day window of Bitcoin closing prices model to 5 day window of of Bitcoin closing prices model: the 5 day window appears to be a better model:
- 5-Day Closing Prices Loss: 0.0459.  10-Day Closing Prices Loss: 0.0616.
- Tracking Values over Time: The model based on the 5-day window of Bitcoin closing prices appears to track the actual values better over time than does the model based on the 10-day window of Bitcoin closing prices.  Comparing the charts for the two models of Real vs. Predicted values over time, the predictions based on the 5-day window more closely reflect the true values than do the predictions based on the 10-day window, similar to the models based on Bitcoin Fear and Greed Index values.


### Comparing 10 day window of Bitcoin Fear and Greed Index values model to 5 day window of Bitcoin Fear and Greed Index values model: the 5 day window appears to be a better model:
- 5-Day F&G Loss: 0.1180.  10-Day F&G Loss: 0.1219.
- Tracking Values over Time: The model based on the 5-day window of Bitcoin Fear and Greed Index values appears to track the actual values better over time than does the model based on the 10-day window of Bitcoin Fear and Greed Index values.  Comparing the charts for the two models of Real vs. Predicted values over time, the predictions based on the 5-day window more closely reflect the true values than do the predictions based on the 10-day window, similar to the models based on Bitcoin closing prices.