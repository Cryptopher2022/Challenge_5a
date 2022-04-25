# Challenge_5 - Financial Planning with APIs and Simulations

In this Challenge, we will envision the role of a financial planner with a client that wants to evaluate two distinct situations.  These are found below.  

We will employ two separate technologies to accomplish this task.  We will be utilizing APIs (Application Programming Interface).  Many web sites employ APIs to assist their clients and/or customers connect in a structured way.  We will be connecting with data sites primarily and pulling a variety of data sets to use in the evaluation of investment types and using financial libraries in Python and specific tools to perform detailed analyses in a variety of useful ways.  For our efforts in this program, we will do the following two items: 

Part 1: A financial planner for emergencies. The members will be able to use this tool to visualize their current savings. The members can then determine if they have enough reserves for an emergency fund.  In this example, the client wishes to estimate an Emergency reserve fund would be three months of their current income.  

Part 2: A financial planner for retirement. This tool will forecast the performance of their retirement portfolio in 30 years. To do this, the tool will make use of a data repository and trading vehicle called Alpaca.  An Alpaca API call will be made via the Alpaca SDK (Software Development Kit) to get historical price data for use in Monte Carlo simulations.  Information regarding a Monte Carlo simulation can be found by following this link from Investopedia.  [API] (https://www.investopedia.com/terms/m/montecarlosimulation.asp#:~:text=A%20Monte%20Carlo%20simulation%20is,in%20prediction%20and%20forecasting%20models).

#Part 1 - Creat a Financial Planner For Emergencies

In this section, we'll create a personal financial planner for emergencies. To develop the prototype, the client has made the following requirements that we will use as our baseline criteria:  

The average monthly household income for each credit union member is $12,000.

Each credit union member has a savings portfolio that consists of a cryptocurrency wallet, stocks, and bonds.

#Part 2 - Evaluate the Cryptocurrency Wallet by Using the Requests Library

In this section, the program will determine the current value of a member’s cryptocurrency wallet and collect the current prices for the Bitcoin and Ethereum cryptocurrencies by using the Python Requests library. For the prototype, we’ll assume that the member holds:

A. 1.2 Bitcoins (BTC) and, 

B. 5.3 Ethereum coins (ETH). To do all this, complete the following steps:

The program uses the Requests library to get the current price (in US dollars) of Bitcoin (BTC) and Ethereum (ETH) by using the API endpoints that the starter code supplied.

Navigate the JSON response object to access the current price of each coin, and store each in a variable.

Calculate the value, in US dollars, of the current amount of each cryptocurrency and of the entire cryptocurrency wallet.

#Evaluate the Stock and Bond Holdings by Using the Alpaca SDK

In this section, the program determine the current value of a member’s stock and bond holdings, make an API call to Alpaca via the Alpaca SDK to get the current closing prices of the SPDR S&P 500 ETF Trust (ticker: SPY) and of the iShares Core US Aggregate Bond ETF (ticker: AGG). For the prototype, assume that the member holds: 

A. 110 shares of SPY, which represents the stock portion of their portfolio and,

B. 200 shares of AGG, which represents the bond portion.

Further analyses will evaluate the Emergency Fund.  

#Part 2 - Create a Financial Planner for Retirement

In this section, the program will use the Alpaca API to get historical closing prices for a retirement portfolio. It will then run Monte Carlo simulations to forecast the portfolio performance 30 years from now. The program will use the simulated data to approximate a client's portfolio and answer questions in your Jupyter notebook about the portfolio.

## Technologies


This project leverages python 3.7 with the following library packages:

* [os](https://docs.python.org/3/library/os.html) - Miscellaneous operating system interfaces

* [requests](https://docs.python-requests.org/en/master/user/quickstart/) - Making requests such as API via HTTP.

* [json](https://docs.python.org/3/library/json.html) - JSON encoder and decoder.

* [pandas](https://pandas.pydata.org/) - A fast, powerful, flexible and easy to use open source data analysis and manipulation tool, built on top of the Python programming language.

* [dotenv](https://pypi.org/project/python-dotenv/) - Read key-value pairs from a .env file and set them as environment variables.

* [alpaca_trade_api](https://pypi.org/project/alpaca-trade-api/0.29/) - https://pypi.org/project/alpaca-trade-api/0.29/.

* [MCForecastTools](https://pypi.org/project/forecast-tools/  Tolls to support the forecasting process in Python

---

## Installation Guide

Before running the application first install the following dependencies.

~~~import os

import requests

import json

import pandas as pd

from dotenv import load_dotenv

import alpaca_trade_api as tradeapi

from MCForecastTools import MCSimulation

%matplotlib inline
~~~

In the repository, select "./financial_planning_tools.ipynb" to initiate the program.  Follow the commented instrutions.
---

## Usage

To evaluate a galaxy of stock, bond and crypto investment assets over varying timeframes and other very useful sensitivities that can be assembled by the User.  
---

---

## Contributors

Brought to you by Christopher Todd Garner

---

## License

[Pinnacle DeFi, LLC](www.pinn-defi.com)
