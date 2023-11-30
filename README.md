# Project Gryphon MT4

This is the code for Project Gryphon MT4, a medium-term trading strategy based on wave movement theory. It is an Expert Advisor that can be used in MetaTrader 4 for automated trading.

## Expert Advisor Parameters

- TakeProfit: The take profit level in pips.
- StopLoss: The stop loss level in pips.
- LotSize: The position size.

## Expert Advisor Start Function

The start() function is the main function of the Expert Advisor. It analyzes wave movement and historical data to open and close positions.

### Wave Movement Analysis

The currentPrice variable stores the current bid price of the symbol. The previousPrice variable stores the closing price of the previous candle on the M5 timeframe. The nextPrice variable stores the closing price of the candle before the previous candle on the M5 timeframe.

### Historical Data Analysis

The previousHigh variable stores the highest price of the previous day (D1 timeframe). The previousLow variable stores the lowest price of the previous day (D1 timeframe).

### Position Opening

If the current price is higher than the previous price and higher than the previous high, a buy position is opened. The position size is calculated based on the available equity. The OrderSend() function is used to send a buy order with the specified parameters.

If the current price is lower than the previous price and lower than the previous low, a sell position is opened. The position size is calculated based on the available equity. The OrderSend() function is used to send a sell order with the specified parameters.

### Position Closing

The for loop iterates through all open orders. If an order has the same magic number as the Expert Advisor, it is selected. If the order type is buy, it is closed if the current price reaches the take profit level or if the trend changes (current price is lower than the next price). If the order type is sell, it is closed if the current price reaches the take profit level or if the trend changes (current price is higher than the next price).

## Product Description

Project Gryphon MT4 is a medium-term trading Expert Advisor that implements a trading strategy based on wave movement theory. It analyzes wave movement and historical data to open and close positions. The Expert Advisor has parameters to set the take profit level, stop loss level, and position size.

This Expert Advisor can be used for automated trading in MetaTrader 4. It is designed to take advantage of medium-term trends in the forex market. The strategy is based on the idea that price movements follow waves, and by identifying and trading these waves, it aims to generate profits.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in this product. For detailed reviews and trading results of this product, please visit [Forex Robot Easy - Project Gryphon MT4 Review](https://forexroboteasy.com/forex-robot-review/project-gryphon-mt4-review-wave-based-forex-trading/). To find the official developer of this product, please refer to MQL5.
