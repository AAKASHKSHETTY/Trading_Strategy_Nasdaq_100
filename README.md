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


