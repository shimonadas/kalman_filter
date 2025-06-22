<!-- PROJECT TITLE -->
<!-- PROJECT SHIELD -->

# Pairs Trading with Kalman Filters

### A dynamic statistical arbitrage strategy which uses real-time hedge ratio estimation.

#### [Explore the Docs »](https://github.com/shimona-das/Pairs-Trading-Kalman-Filters)  
#### [Report a Bug](https://github.com/shimona-das/Pairs-Trading-Kalman-Filters/issues)  
#### [Request a Feature](https://github.com/shimona-das/Pairs-Trading-Kalman-Filters/issues) 
---

## About The Project

Pairs trading is a market-neutral strategy where two correlated assets are traded based on their price spread. Instead of using a **fixed hedge ratio**, this project utilizes a **Kalman filter** in order to dynamically adjust the hedge ratio over time. This allows for **more accurate and adaptive trading decisions**.

### **Why Use a Kalman Filter?**
- Traditional pairs trading assumes a fixed hedge ratio (e.g., Ordinary Least Squares regression).
- However, in real markets, stock relationships **change over time**.
- A **Kalman filter** helps us continuously **update** the hedge ratio, improving trading accuracy.

---

## **How It Works**
1. **Data Collection**: Fetches stock price data from Bloomberg.
2. **Preprocessing**: Cleans data, removes missing values, and normalizes prices.
3. **Dynamic Hedge Ratio Estimation**: Uses the Kalman filter to adjust hedge ratios in real-time.
4. **Trading Signals**:
   - If the spread is **too wide**, we **bet on it returning to normal**.
   - If the spread is **too narrow**, we **exit the trade**.
5. **Backtesting**: Simulates past trades to evaluate strategy performance.

---

## **Getting Started**
### **Prerequisites**
Before running the project, install the required libraries:
```bash
pip install numpy pandas yfinance statsmodels pykalman matplotlib

Pairs-Trading-Kalman-Filters/
│── data/                   # Historical stock data
│── notebooks/              # Jupyter notebooks for testing
│── src/
│   ├── kalman_filter.py    # Implements the Kalman filter
│   ├── trading_strategy.py # Generates buy/sell signals
│   ├── backtest.py         # Evaluates performance
│── config.py               # User settings (tickers, thresholds)
│── README.md               # Project documentation
│── requirements.txt        # Dependencies

