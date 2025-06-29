Trading Bot Project Explanation

Overview

This project is an automated algorithmic trading bot designed to analyze stock market data, generate trading signals, and log results. It targets NSE stocks like RELIANCE.NS, HDFCBANK.NS, and INFY.NS, using historical data to simulate trades and predict profitability.

Logic Behind the Project

The bot fetches 6 months of daily data using yfinance, calculating technical indicators like RSI, SMA20, SMA50, and MACD with a pandas fallback since TA-Lib installation failed.
It generates buy signals when RSI drops below 40 and SMA20 exceeds SMA50, and sell signals when RSI exceeds 70 or SMA20 falls below SMA50.
A Decision Tree model predicts next-day price movements, training on features like RSI and volume, with accuracy and F1 scores logged.
The backtest strategy simulates trades with a 100-share position size, calculating P&L for each sell.
Results are logged to Google Sheets in three tabs: Trade Log (individual trades), Summary P&L (per-stock performance), and Portfolio Analytics (overall metrics).

Tools and Implementation

Built in Google Colab, the project uses yfinance for data, pandas for indicators, scikit-learn for ML, and gspread for Google Sheets integration. The script handles errors with logging to troubleshoot issues like data fetch failures or sheet updates.

Results and Demonstration

The bot successfully logged trades, with INFY.NS showing a sample buy at 1507.45 and sell at 1626.70, yielding a 11,925 P&L. The sheet reflects accurate summaries, proving the logic works with yfinance data. This demo highlights automation, data-driven decisions, and real-time logging.

Conclusion

This project showcases a practical trading solution, adaptable with threshold tweaks or additional indicators, ready for further enhancement.
