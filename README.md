# mockup_MovingAverageCrossoverStraategy_backtest.ipynb
mockup Moving Average Crossover Straategy back test

# 📈 Moving Average Crossover Strategy Backtest (AAPL)

This repository contains a Jupyter notebook that implements a backtest of a simple Moving Average Crossover trading strategy using historical stock data from Yahoo Finance.

The strategy uses two moving averages:
- Short-term moving average (40 days)
- Long-term moving average (100 days)

Buy and sell signals are generated when the short MA crosses above or below the long MA.

---

## 📌 Project Overview

- **Ticker used**: AAPL (Apple Inc.)
- **Period**: 2020-01-01 to 2023-12-31
- **Data source**: [Yahoo Finance](https://finance.yahoo.com/)
- **Tools used**: Python, `yfinance`, `pandas`, `numpy`, `matplotlib`
- **Key Metrics Calculated**:
  - Total Return
  - Maximum Drawdown
  - Percentage of Winning Days
  - Sharpe Ratio (Annualized)

---

## 🧠 Logic Summary

1. **Download data** using `yfinance`.
2. **Calculate short and long moving averages** of the closing price.
3. **Generate signals** based on MA crossover:
   - Buy when short MA > long MA
   - Sell when short MA < long MA
4. **Simulate trades and returns**.
5. **Evaluate performance** using common metrics.
6. **Visualize** price chart with buy/sell signals.

---

## 🖼️ Sample Output

![Strategy Plot Example](screenshot.png) <!-- Optional: Add screenshot of matplotlib output -->

---

## ▶️ How to Run

1. Clone this repo:

   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
````

2. Install dependencies:

   ```bash
   pip install yfinance pandas numpy matplotlib
   ```

3. Open the notebook:

   ```bash
   jupyter notebook mockup_MovingAverageCrossoverStraategy_backtest.ipynb
   ```

4. Run all cells and view the output.

---

## ⚠️ Notes
* The code includes handling for:
  * Data download errors
  * Missing values after moving average calculation
  * MultiIndex vs flat index column access
* A manual workaround is used instead of `dropna(subset=...)` to avoid `KeyError`.

---

## 📄 License

This project is open for learning and experimentation. You are free to copy, modify, or redistribute with attribution.

---

## 🙌 Acknowledgements

* [Yahoo Finance API](https://pypi.org/project/yfinance/)
* Inspired by classic technical analysis strategies
