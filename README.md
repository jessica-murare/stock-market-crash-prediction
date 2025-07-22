# stock-market-crash-prediction

# Overview
This project provides a comprehensive analysis of historical stock market data, specifically focusing on the Sensex index, to identify and visualize periods of significant market downturns (crashes). It calculates daily returns and drawdowns to pinpoint crash events and offers an early warning system based on rolling mean returns and volatility.

# Features
## Data Loading and Preprocessing:

Reads historical Sensex data from a CSV file (sensex.csv).

Cleans and transforms the data, including converting the 'Date' column to datetime objects and setting it as the index.

## Daily Return and Crash Identification:

Calculates daily percentage change in closing prices.

Identifies "daily crash" events where the daily return falls below a predefined threshold (e.g., -5%).


## Drawdown Analysis:

Computes the cumulative maximum of the closing prices.

Calculates the drawdown as the percentage drop from the cumulative maximum, highlighting periods of significant market decline (e.g., below -20%).

Clusters consecutive drawdown events to identify prolonged crash periods.

## Interactive Visualizations (using Plotly):

Plots the Sensex closing price over time, with daily crash days highlighted.

Visualizes market drawdown over time, with a threshold line to indicate significant downturns.

Provides zoomed-in plots of closing prices, daily returns, and drawdowns for specific historical crash periods (e.g., 1997, 2008-2009, 2020).
<img width="1777" height="744" alt="image" src="https://github.com/user-attachments/assets/854b14bc-f01a-452c-87d4-feda400cdb3e" />


## Early Warning System (EWS):

Calculates rolling mean returns and rolling volatility over a specified window.

Identifies early warning signals for potential crashes based on a combination of negative rolling mean returns and high rolling volatility.

Generates a synthetic dataset for 2025 to demonstrate the EWS in action, highlighting potential future crash signals.

<img width="1798" height="530" alt="image" src="https://github.com/user-attachments/assets/6c59ab5e-7a57-43f0-91ca-6154ea64542f" />


# Data
The core of this analysis relies on historical Sensex data, expected to be in a CSV file named sensex.csv. The CSV should contain at least the following columns:

Price (or Date): Date of the trading day.

Close: Closing price of the Sensex.

High: Highest price of the day.

Low: Lowest price of the day.

Open: Opening price of the day.

Volume: Trading volume for the day.

Note: The provided Jupyter notebook assumes the sensex.csv file is located at /content/sensex.csv. You may need to adjust the path if your file is located elsewhere.
