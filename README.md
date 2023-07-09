# Trading_Strategy_Nasdaq_100

## Introduction

Our strategy implementation uses technical indicators, taught in class and some taken from online resources. We have selected stocks from Nasdaq 100 to generate signals from each of these indicators.

These indicators include the Simple Moving Average based on Adj. Close, which gives us a clear insight into the average price of a stock over a set period of time. We have also used the Simple Moving Average based on Volume, which tracks the average volume of a stock over a set period of time.

We have incorporated the Breakout High-Low 30, which highlights when a stock’s price has broken through its previous high or low. In addition, we have used the Average True Range, which helps us determine the volatility of a stock over a specific period of time.

Furthermore, the Moving Average Convergence Divergence (MACD) indicator has been used, which helps us understand the relationship between two moving averages of a stock's price. Finally, we have also utilized the Bollinger Bands, which helps us to identify potential buying or selling opportunities based on a stock's volatility.

Based on the returns from each of these technical indicators, we have taken the top-performing stocks to build a portfolio. We then went a step further by building an Equal vs. Vol Weighted portfolio by combining all the strategies to obtain combined returns.

This strategy, performs better than the individual stocks and other strategies that we had implemented. Our goal is to outperform a standard buy-and-hold strategy of the SPY ETF over a defined period of time. 

## Dataset

First, a list of Nasdaq-100 company tickers is obtained from Wikipedia. Then we use pandas datareader to get daily data from Yahoo Finance for each ticker from January 2009-01-01 to the present. The final dataset includes the following information, for every ticker, before further calculations.

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/c6e66ece-464e-43f9-bb6f-861339f62456)

## Technical Indicators

We have selected 6 Trading Strategy:

Simple Moving Average Based on Adj. Close
Simple Moving Average Based on Volume
Breakout High-Low 30
Average True Range
Moving Average Convergence-Divergence (MACD)
Bollinger Bands

We will go through the results from each of the technical indicators in the following pages, for in detail code and results we have shared ipynb notebook in the final submission.

### Simple Moving Average Based on Adj. Close

Calculating the moving average of a stock serves the purpose of creating a constantly updated average price, which helps to smooth out the price data. By doing so, the impact of random, short-term fluctuations on the price of a stock over a specified period of time is minimized. Additionally, we use the golden cross as a tool to track trading signals, which is interpreted by analysts and traders as an indication of an upward turn in the market. When the short-term moving average crosses above the long-term moving average, we identify buying signals. To illustrate how this trading strategy based on simple moving average (price) signals could be used, we have provided an example plot of trading Apple stock from January 2022 to present. We have use 10 as the short term moving average and 30 as the long term moving average.

### Simple Moving Average Based on Volume

Volume based simple moving averages can assist traders in identifying trend strength and changes in volume by mitigating the impact of isolated spikes in volume activity in an index. Buying signals are identified when the SMA volume 10 crosses SMA volume 30.



