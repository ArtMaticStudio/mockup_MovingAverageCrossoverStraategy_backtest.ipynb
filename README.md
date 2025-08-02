# 📈 Moving Average Crossover Backtest for AAPL

This Python script performs a simple **Moving Average Crossover** backtest on Apple Inc. (AAPL) stock data using historical data from Yahoo Finance. It also visualizes the trading signals and evaluates the performance of the strategy.

## 🧠 Strategy Overview

The **Moving Average Crossover** strategy works by comparing two moving averages:

* **Short-Term Moving Average** (e.g., 40 days)
* **Long-Term Moving Average** (e.g., 100 days)

A **buy signal** is generated when the short-term MA crosses above the long-term MA.
A **sell signal** occurs when the short-term MA crosses below the long-term MA.

## 🛠 Features

* Downloads historical stock data via [yfinance](https://pypi.org/project/yfinance/)
* Calculates short-term and long-term moving averages
* Generates trading signals based on crossover
* Simulates portfolio value with initial capital
* Calculates performance metrics:

  * Total return
  * Maximum drawdown
  * Percentage of winning days
  * Sharpe ratio (annualized)
* Plots price chart with buy/sell markers

## 📦 Dependencies

You can install the required Python packages using pip:

```bash
pip install yfinance pandas numpy matplotlib
```

## 🚀 How to Run

Simply execute the script in your Python environment:

```bash
python backtest_moving_average.py
```

Make sure to update the ticker symbol, date range, or moving average windows as needed.

## 🧾 Output Metrics Example

Sample output after running the backtest:

```
Dropped 99 rows due to NaN values using dropna() without subset after MA calculation.
Total Return: -5.34%
Maximum Drawdown: -5.34%
Percentage of Winning Days: 0.44%
Sharpe Ratio (Annualized): -1.08
```

## 📊 Plot Example

The script will generate a plot that includes:

* Blue line: Closing price of AAPL
* Green triangles (^): Buy signals
* Red triangles (v): Sell signals

This helps visualize the entry and exit points of the strategy over time.

## 📁 File Structure

```
backtest_moving_average.py     # Main script
README.md                      # This file
```

## ⚠️ Notes

* Yahoo Finance may return data with **MultiIndex columns** (e.g., `('Close', 'AAPL')`). The script handles both MultiIndex and flat DataFrames.
* The script avoids `dropna(subset=['Daily_Return'])` to prevent KeyErrors and instead uses manual filtering.
* Results will vary depending on stock ticker and selected date range.
* This is a basic backtest — it does **not** include slippage, transaction costs, or risk management.

## ✅ TODOs (optional)

* Add transaction fee simulation
* Implement trailing stop loss
* Add more performance metrics (e.g., CAGR, Sortino Ratio)
* Extend to multiple tickers or use portfolio backtesting framework

## 📜 License

This project is provided for educational purposes and is licensed under the MIT License.

---

Let me know if you want a version in Bahasa Indonesia or if you'd like to convert this into a GitHub-friendly format with badges and advanced features.
