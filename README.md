# Forex Trend Hunter MT5

Forex Trend Hunter MT5 is an expert advisor that aims to maximize profits by identifying trends in the forex market. This code is provided as a sample and is not developed or endorsed by ForexRobotEasy. It is intended to demonstrate how the expert advisor works based on the provided code.

## Product Description

Forex Trend Hunter MT5 is a powerful expert advisor designed to take advantage of trending market conditions in the forex market. It uses a moving average crossover strategy to identify buy and sell signals.

#### Key Features:

- Take Profit: 100 pips
- Stop Loss: 50 pips
- Lot Size: 0.01
- Maximum Trades: 10

The expert advisor initializes by setting up the necessary account and money management system. It sets the expert magic number, take profit, stop loss, and lot size.

The expert advisor then retrieves the moving average series using the `iMA` function. It calculates the moving average based on the close price of the 5-minute chart with a period of 14.

In the `OnTick` function, the expert advisor checks if the maximum number of trades has been reached. If not, it checks if a buy signal is generated when the current moving average value is greater than the previous value. If a buy signal is generated, the expert advisor opens a buy position using the `Buy` function and adds the position identifier to the `positions` array.

Similarly, if a sell signal is generated when the current moving average value is less than the previous value, the expert advisor opens a sell position using the `Sell` function and adds the position identifier to the `positions` array.

The expert advisor then checks for stop loss or take profit levels for each position in the `positions` array. If the position's profit reaches the take profit level or goes below the stop loss level, the position is closed using the `PositionClose` function and removed from the `positions` array.

In the `OnDeinit` function, the expert advisor ensures that any remaining positions are closed before deinitializing.

For detailed reviews and trading results of this product, please visit the [Forex Trend Hunter MT5 Review](https://forexroboteasy.com/forex-robot-review/forex-trend-hunter-mt5-review-maximize-profits-this-black-friday/) on ForexRobotEasy's website. Please note that ForexRobotEasy is not the official developer of this product. To find the official developer, please refer to the MQL5 platform.
