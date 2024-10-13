# Volatility Arbitrage Project Overview
This project aims to build and test a volatility arbitrage strategy in the equity derivatives market. The strategy seeks to profit from discrepancies between implied volatility (as priced in options) and realized volatility (historically observed in the underlying stock). The project leverages statistical models to forecast volatility and backtests a trading strategy using real market data.

The goal is to design a delta-neutral strategy, such as a long straddle, to take advantage of these discrepancies, while minimizing market exposure.

# Objectives
Calculate and compare realized and implied volatility.
Implement and backtest a volatility arbitrage trading strategy.
Analyze performance through various metrics, such as Sharpe ratio and PnL.
Document insights and findings to enhance understanding of volatility-driven trading strategies.

# Key Concepts
1. Volatility Arbitrage: A strategy that profits from the difference between implied volatility (from options) and realized volatility (historically observed).

2. Implied Volatility (IV): Market's forecast of a likely movement in a security's price. IV is extracted from the prices of options using models like Black-Scholes.

3. Realized Volatility (RV): Actual historical volatility of a stock, typically calculated as the standard deviation of past returns over a specified period.

4. Delta-Neutral Strategy: A strategy that seeks to profit from volatility without exposure to the direction of price movements.

# Methodology 
1. Data Collection <br>
- **Historical Prices**: We obtain stock price data for various equities. <br>
- **Options Data**: Implied volatility is extracted from option chains.<br>
- **Realized Volatility Calculation**: Rolling standard deviation of historical returns is used to calculate RV. <br>
2. Volatility Analysis <br>
- **Implied vs. Realized Volatility**: We calculate the difference between the two and look for arbitrage opportunities. <br>
- **Volatility Forecasting**: A GARCH model is used to predict future realized volatility based on historical data. <br>
3. Trading Strategy <br>
We implement a delta-neutral strategy (e.g., long straddle) to profit from volatility arbitrage. The strategy is designed to exploit periods where implied volatility is significantly mispriced relative to realized volatility. <br>
4. Backtesting <br>
The strategy is backtested on historical data to evaluate performance, including metrics such as:
- **PnL (Profit and Loss)**: Measures the overall profit or loss of the strategy over the backtesting period.
- **Sharpe Ratio (risk-adjusted returns)**: Evaluates the returns of the strategy relative to its risk, helping determine whether the returns are worth the risk taken.
- **Max Drawdown (risk metric)**: Represents the maximum observed loss from a peak to a trough during the backtesting period.
- **Win/Loss ratio (success rate of trades)**: The proportion of profitable trades compared to the total number of trades executed.

5. Optimization <br>
The trading model is refined based on performance data, adjusting parameters like volatility windows, option expiration periods, and trade size.
