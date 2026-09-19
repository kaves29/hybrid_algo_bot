# Machine Learning Trading Bot

## 1. What I Built

I built a machine learning-based trading bot that uses historical stock data and technical indicators to identify potential short-term opportunities. The project trades a portfolio of seven stocks: AAPL, MSFT, JNJ, JPM, KO, TSLA, and PG.

I first built the data and feature pipeline, then trained an XGBoost classification model to predict whether a stock could reach a 3% profit target within the next 10 trading days. I then combined the model's prediction with technical trading rules to decide when to buy and sell.

The bot also manages a simulated $10,000 portfolio, tracks positions and trades, accounts for transaction fees and slippage, and evaluates its performance against a passive S&P 500 benchmark.

## 2. How I Built It

The project was built in Python using `yfinance` to collect historical market data and `pandas` and `numpy` to process it. I generated technical indicators including 50-day and 200-day moving averages, RSI, MACD, Bollinger Bands, and ATR using the `ta` library.

For machine learning, I used `XGBoost` to train a classifier on these indicators. The model was trained on historical data from 2020–2022, while the 2022–2025 period was used as a separate testing period. The trading system uses the model's predicted probability along with technical conditions to control position sizing and trade execution.

I also built the backtesting and performance-analysis portion from scratch, including portfolio tracking, trade history, transaction costs, slippage, equity curves, drawdowns, rolling Sharpe ratio, volatility, win rate, profit factor, and Monte Carlo simulations.

## 3. Tools & Analysis

**Languages & Libraries**

* Python
* Pandas
* NumPy
* Matplotlib
* scikit-learn
* XGBoost
* yfinance
* TA

**Main techniques used**

* Supervised machine learning
* Technical analysis
* Historical backtesting
* Portfolio and position management
* Risk-adjusted performance analysis
* Monte Carlo simulation

The main goal of this project was to combine machine learning with traditional quantitative trading methods and build the entire pipeline myself, from collecting market data and engineering features to making trades and analyzing the results.

