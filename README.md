<img src="main_pic.png" width="700"/>

# Disclaimer
This project does not advocate or promote the purchase of bitcoin or any other cryptocurrencies.  
It should not be viewed as an investment advise.  
It only serves academic and education purposes.

# Motivation
Remarkable growth and fall of Bitcoin over the last few years created large ammount of interest and speculation. To better understand the nature of cryptocurrency, this project performs time series modelling and prediction of its historical prices.  

It demonstrates that the target variable does not seem to be affected by seasonal or cyclical trends but overall has been following a slight upward trend.  

This porject also illustrates that predictive modelling of Bitcoin on daily basis is not an easy task due to its volatility.  

# Goal
The purpose of this project is to exercise our newly aquired time series analysis and prediction skills.

# Data
This project utilises three types of data:
- bicoin price historical data (source: coinmarketcap.com)
- gold price historical data (source: https://datahub.io/core/gold-prices#data)
- bitcoin google search tredns historical data (Google trends)

# Models 
- ARIMA model  
- ARIMAX model  
- Long short-term memory (LSTM) recurrent neural network (RNN)  

# EDA
The data was webscraped from coinmarketcap and originally had columns containing daily information about the opening, closing, low, and high price for Bitcoin, as well as the volume and market cap from April 28, 2013 to May 28, 2019. There was no missing information and no zeroes in the data. For our purposes we only needed the closing price, so this was information was copied into a separate dataframe. After converting the date to a pandas date time index, the closing price was plotted. 

<img src="https://github.com/AR3441/Mod4TimeSeriesProject/blob/master/Graphs/bitcoin_daily_price.png" width="700"/>


Looking at this graph, one will immediatley see that it is not stationary. To better understand the data, a seasonal decomposition was used:

<img src="https://github.com/AR3441/Mod4TimeSeriesProject/blob/master/Graphs/seasonal_decomposition_daily.png" width="700"/>

Since this is daily data, it was difficult to observe seasonality and the residuals are difficult to interpret as well. To investigate any possible seasonality and trends, the rolling mean was observed for daily data, aggregated monthly data and aggregated yearly data. This can be seen blow respectively, from left to right. 

<p float="left">
  <img src="https://github.com/AR3441/Mod4TimeSeriesProject/blob/master/Graphs/rolling_mu_daily.png" width="275" />
  <img src="https://github.com/AR3441/Mod4TimeSeriesProject/blob/master/Graphs/rolling_mu_monthly.png" width="275" /> 
  <img src="https://github.com/AR3441/Mod4TimeSeriesProject/blob/master/Graphs/rolling_mu_yearly.png" width="275" />
</p> 



