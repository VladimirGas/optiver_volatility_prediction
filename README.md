# optiver_volatility_prediction

Submission to the Kaggle competition by Optiver: https://www.kaggle.com/c/optiver-realized-volatility-prediction

The notebook contains:

1. FEATURE ENGINEERING:
   Features generated from the limit order book data:
       vol_wap(_/1/2) - volatility of the weighted average price 
       wap_std(_/1/2) - the standard deviation of the weighted average price
       wap_mad(_/1/2) - median absolute deviation of the wap
       
       where 
          _ - refers to all layers of the order book
          1 - refers to the first best bid and ask
          2 - refers to the second best bid and ask
       
       bid1_std - std of the best bid
       bid2_std - std of the second best bid
       ask1_std - std of the best ask
       ask2_std - std of the second best ask
       high / low - the high and low of the 10-min session
       range - the difference between the high and low of the session
       
       
   Features generated from matket order data:
   
       vol_price - volatility of the market order price
       price_std_x - 
       price_std_y
       price_mad
       size_mad
       ordercount_std
       ordercount_mad
       ordercount_max


2. TRAINING A SIMPLE LGB MODEL:

  Trained an LGB model with 4-fold Kfold and early stopping rounds set at 500.
  The final RMSPE is 0.22609
  
  
