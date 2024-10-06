Welcome to the Prescient Coding Challenge 2024!

The Problem Description
You have been provided with price and financial data for 100 US stocks. Your task is to generate 1-day-ahead trading signals for each stock. Additionally, you need to select the top 10 stocks each day to form a portfolio. The performance of your selected portfolio will be evaluated based on the total return index over the evaluation (test) period.

This type of trading is known as swing trades. You are only allowed long positions, i.e. you matrix of buys will only contain 1's and 0's.

You are given files

README.md - this file
data0.csv - 1st data file
data1.csv - 2nd data file
returns.csv - returns file
solution.py - a skeleton structure with sample solution for the problem description
The Data
The data provided is a mix of daily, monthly, and yearly data. Where possible the data has been issued daily otherwise forward filled to match the pricing data availability.

The file data0.csv contains the security sector data
The file data1.csv contains price, historical returns, financial ratios and the 1-day-ahead price change label for each security and trading day
A brief description of the columns in the data are:

date - close of business day
security - the instrument code, in this case its the stock ticker
sector - the security's sector classification
price - closing day price in USD
ratio_pe - price to earnings ratio
ratio_pcf - price to cash flow ratio
ratio_de - debt to equity ratio
ratio_roe - return on equity
ratio_roa - return on assets
label - a 0 or 1 label, with 0 indicating a loss taking bet and 1 a positive winning bet
Ratios Reading

The Output
We are interested in the total payoff for the buys in the testing period 2024-01-01 to 2024-06-30. The high level steps are

Generate buy-signals
Create a buy-matrix of 1s (buys) and 0s (don't buy) with each row summing to 10 (10 buys)
Generate payoff chart
Your buy-matrix will create your payoff chart using the plot_payoff function.
