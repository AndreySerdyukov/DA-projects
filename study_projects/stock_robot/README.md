# Trading Strategy with Moving Averages and Stop-Loss

This project implements a trading strategy based on short and long moving averages, with the addition of a stop-loss mechanism to minimize potential losses. The strategy buys stocks when the short moving average crosses above the long moving average, and sells when the short moving average crosses below the long moving average or the stop-loss condition is met.

## Overview

- **Goal**: To simulate a trading strategy using real daily stock price data from exchanges (e.g., NYSE, Moscow Exchange).
- **Objective**: The strategy aims to maximize profits while minimizing losses by using stop-loss orders and leveraging moving averages for trade signals.

## Key Parameters

The following parameters should be defined at the start of the script:

1. **money**: Initial amount of cash (1,000,000).
2. **start**: Start date of the time period (e.g., "2015-01-01").
3. **finish**: End date of the time period (e.g., "2020-12-31").
4. **stop_loss**: Stop-loss threshold (e.g., 5%).
5. **short_window**: Short moving average window (e.g., 30 trading days).
6. **long_window**: Long moving average window (e.g., 90 trading days).

The moving averages are calculated using a simple moving average (SMA).

## Trading Signals

- **Buy Signal (sig_buy)**: The short moving average crosses above the long moving average.
- **Sell Signal (sig_sale)**: The short moving average crosses below the long moving average.
- **Stop-Loss**: A stop-loss is triggered if the stock price falls by more than the specified threshold from the purchase price.

## Trading Rules

1. **Buying**: When a **sig_buy** signal is triggered, the entire available cash is used to buy as many shares as possible at the opening price of the next trading day.
2. **Selling**: When a **sig_sale** signal occurs, all shares are sold at the opening price.
3. **Stop-Loss**: If the stock price falls by more than the stop-loss percentage on any given day, the shares are sold at the price where the stop-loss is triggered.

## Data Structure

The input data should be in a Pandas DataFrame with the following structure:

- **Index**: Date/Time
- **Columns**: 
  - **Open**: Opening price for the day
  - **High**: Highest price during the day
  - **Low**: Lowest price during the day
  - **Close**: Closing price for the day

## Output

The resulting DataFrame should contain the following columns:

1. **date**: The date of the transaction.
2. **signal**: The type of action (sig_buy, sig_sale, buy, sale, stop-loss).
3. **num_shares**: The number of shares held in the portfolio.
4. **share_price**: The price per share at the time of the transaction.
5. **share_value**: The total value of the shares held.
6. **cash**: The remaining cash after the transaction (rounded to two decimal places).

## Final Report

At the end of the simulation:
- The portfolio value should be calculated based on the final share sale or stop-loss event.
- The percentage change in the initial investment should be displayed.
- A visualization of the trading strategy's performance should be generated.

## Visualization

The project should include two visualizations:
1. **Top window**: The stock price along with the short and long moving averages.
2. **Bottom window**: A plot of the portfolio value over time.
