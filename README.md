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

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/1b3c3ec6-364c-492c-991e-a625e017fe33)

### Breakout High-Low 30

A breakout strategy is a popular approach in trading, which involves entering a trade as soon as the price breaks out of its range. Using this strategy we can capitalize on strong momentum, which can result in significant market movements. The moment at which the price manages to break out of its range is a key event in the market, and is seen as a signal to enter a position. In this way, we can aim to profit from the market movement that typically follows a breakout. Here, we have used 30 day high-low as our breakout range.

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/b40298c9-9570-4421-9e9b-de504a550fe3)

### Average True Range 

The higher the ATR (Average True Range), the greater the volatility of its stock. While ATR can help to identify the ideal timing for entering or exiting a trade, it is not typically used to determine the direction in which to trade the stock. We can use ATR to identify signals of inflection and high volatility, which can serve as key indicators for making trading decisions. In particular, buying signals are identified when the short-term ATR crosses above the long-term ATR.

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/d7e1e101-0437-4ffd-aa02-1091f182e04c)

### Moving Average Convergence-Divergence (MACD)

Moving average convergence divergence is a momentum indicator used to track trends, which illustrates the relationship between two exponential moving averages (EMAs) of a security’s price. This type of moving average places greater weight and significance on more recent data points. We calculate the MACD value by subtracting the 10-period EMA from the 30-period EMA. In addition to the MACD line, we also calculate the MACD signal by taking the 10-period EMA of the MACD line itself. To identify buying signals, we label instances where the MACD value is above the MACD signal. Conversely, selling signals are identified when the MACD value falls below the MACD signal.

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/4a495f6b-3312-4d43-892e-15c8779d20da)

### Bollinger Bands

Bollinger bands are used to measure stock volatility and identify overbought/oversold conditions. They consist of a moving average line, upper and lower bands set at 2 standard deviations from the average. Buy signals occur when adjusted close price drops below the lower band; sell signals when it rises above the upper band. Combining Bollinger bands with other technical indicators and fundamental analysis can improve trading strategy.

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/3ad8c1b5-228b-42b1-aeed-a061e90ddb9f)

## Trading Strategy

Our trading strategy makes use of all of the above mentioned technical indicators. Based on the signals generated from the technical indicators we calculate the return for each of our individual strategies. At any point in time we are either long, short or have no position.

Further, we rank top 10 stocks from each of the indicator results based on Sharpe. From these results we compare the sharpes to select the top 5 best performing stocks with respect to the top technical indicator returns. 

![image](https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/b7ea2441-bd01-453c-a2fb-177e691199d5)

We further proceed to build a Equal Weighted and Vol Weighted Portfolio to compare the returns and Sharpe ratios, along with the drawdowns for each of them. To access the strategy, we have submitted final excel sheet.

## Results

Please find below the top 10 results for each technical indicators.

<img width="783" alt="image" src="https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/1243e028-71c4-4e61-a560-f332f7db7832">

We can observe that bollinger bands have a general better performance and breakout have the top 2 stocks outperforming by huge margins. ATR and MACD have 1 stock outperforming the rest while other have an even performance distribution.

### Equal Vs Vol Weighted Analysis

<img width="771" alt="image" src="https://github.com/AAKASHKSHETTY/Trading_Strategy_Nasdaq_100/assets/58876667/c592cee8-51ea-43d5-9461-c67f4623ee3c">

## Conclusion

The results show that our trading strategy yielded a Sharpe of 1.991 which outperformed a buy and hold SPY strategy with Sharpe 0.67. The addition of indicators and weighted portfolio proved very useful in predicting buying and selling opportunities.
