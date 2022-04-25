# Challenge_5 - Financial Planning with APIs and Simulations

In this Challenge, you’ll create two financial analysis tools by using a single Jupyter notebook:

Part 1: A financial planner for emergencies. The members will be able to use this tool to visualize their current savings. The members can then determine if they have enough reserves for an emergency fund.

Part 2: A financial planner for retirement. This tool will forecast the performance of their retirement portfolio in 30 years. To do this, the tool will make an Alpaca API call via the Alpaca SDK to get historical price data for use in Monte Carlo simulations.

There are a number of set steps in the process.  These are found below. 

1. *Collect the data.*

2. *Prepare the data.*

3. *Analyze the data.*
---

We will primarily be focusing on analyzing the data, step 3, although steps 1 & 2 are foundational for any activities in this step.

The steps toward analyzing and the actual analysis are as follows:

The five sets of data under evaluation are:*
    
    A. SOROS FUND MANAGEMENT LLC

    B. PAULSON & CO.INC.

    C. TIGER GLOBAL MANAGEMENT LLC

    D. BERKSHIRE HATHAWAY INC

    E. S&P 500

4. *After finding the daily percent return of each fund (yes, the S&P 500 is considered a fund), we will perform a number of valuable calculations that will provide particular insight as to the behavior of each fund in differing circumstances and over the long haul.*  

## Import the Data
Use the risk_return_analysis.ipynb file to complete the following steps:

Import the required libraries and dependencies.

## Analyze the Performance
Analyze the data to determine if any of the portfolios outperform the broader stock market, which the S&P 500 represents. To do so, complete the following steps:

Use the default Pandas plot function to visualize the daily return data of the four fund portfolios and the S&P 500. Be sure to include the title parameter, and adjust the figure size if necessary.

## Analyze the Volatility
Analyze the volatility of each of the four fund portfolios and of the S&P 500 Index by using box plots. To do so, complete the following steps:

1. Use the Pandas plot function. 

2. Use the Pandas drop function to create a new DataFrame that contains the data for just the four fund portfolios by dropping the S&P 500 column. Visualize the daily return data for just the four fund portfolios by using another box plot. Be sure to include the title parameter, and adjust the figure size if necessary.

## Analyze the Risk
1. Evaluate the risk profile of each portfolio by using the standard deviation and the beta. To do so, complete the following steps:

2. Use the Pandas std function to calculate the standard deviation for each of the four portfolios and for the S&P 500. Review the standard deviation calculations, sorted from smallest to largest.

3. Calculate the annualized standard deviation for each of the four portfolios and for the S&P 500. To do that, multiply the standard deviation by the square root of the number of trading days. Use 252 for that number.

4. Use the daily returns DataFrame and a 21-day rolling window to plot the rolling standard deviations of the four fund portfolios and of the S&P 500 index. Be sure to include the title parameter, and adjust the figure size if necessary.

5. Use the daily returns DataFrame and a 21-day rolling window to plot the rolling standard deviations of only the four fund portfolios. Be sure to include the title parameter, and adjust the figure size if necessary.

*Answer the following three questions:*

1. Based on the annualized standard deviation, which portfolios pose more risk than the S&P 500?

2. Based on the rolling metrics, does the risk of each portfolio increase at the same time that the risk of the S&P 500 increases?

3. Based on the rolling standard deviations of only the four fund portfolios, which portfolio poses the most risk? Does this change over time?

## Analyze the Risk-Return Profile
1. To determine the overall risk of an asset or portfolio, quantitative analysts and investment managers consider not only its risk metrics but also its risk-return profile. After all, if you have two portfolios that each offer a 10% return but one has less risk, you’d probably invest in the smaller-risk portfolio. For this reason, you need to consider the Sharpe ratios for each portfolio. To do so, complete the following steps:

2. Use the daily return DataFrame to calculate the annualized average return data for the four fund portfolios and for the S&P 500. Use 252 for the number of trading days. Review the annualized average returns, sorted from lowest to highest.

3. Calculate the Sharpe ratios for the four fund portfolios and for the S&P 500. To do that, divide the annualized average return by the annualized standard deviation for each. Review the resulting Sharpe ratios, sorted from lowest to highest.

4. Visualize the Sharpe ratios for the four funds and for the S&P 500 in a bar chart. Be sure to include the title parameter, and adjust the figure size if necessary.

5. Answer the following question: Which of the four portfolios offers the best risk-return profile? Which offers the worst?

## Diversify the Portfolio
1. Based on your analysis so far, choose two portfolios that you’re most likely to recommend as investment options. To start your analysis, complete the following step:

2. Use the Pandas var function to calculate the variance of the S&P 500 by using a 60-day rolling window. Visualize the last five rows of the variance of the S&P 500.

3. Next, for each of the two portfolios that you chose, complete the following steps:

4. Using the 60-day rolling window, the daily return data, and the S&P 500 returns, calculate the covariance. Review the last five rows of the covariance of the portfolio.

5. Calculate the beta of the portfolio. To do that, divide the covariance of the portfolio by the variance of the S&P 500.

6. Use the Pandas mean function to calculate the average value of the 60-day rolling beta of the portfolio.

7. Plot the 60-day rolling beta. Be sure to include the title parameter, and adjust the figure size if necessary.

# Technologies

This project was completed almost entirely in Jupyter Notebook.  The README.md was modified in VS Code.  

There were three main libraries used in this project:
pandas libraries
Path from pathlib
matplotlib (inline) - inline means:  "sets the backend of matplotlib to the 'inline' backend: With this backend, the output of plotting commands is displayed inline within frontends like the Jupyter notebook, directly below the code cell that produced it. The resulting plots will then also be stored in the notebook document" - source: https://stackoverflow.com/questions/43027980/purpose-of-matplotlib-inline#:~:text=%25matplotlib%20inline%20sets%20the%20backend,stored%20in%20the%20notebook%20document.

More information can be found regarding each of these libraries at the following links:

pandas - https://pandas.pydata.org/
Path from pathlib - https://docs.python.org/3/library/pathlib.html
matplotlib - https://matplotlib.org/

This program was written and will run on Windows 10.  

---

## Installation Guide

In this section, you should include detailed installation notes containing code blocks and screenshots.

From the Command Line in Git Bash, navigate your directory to the location of the file package.  Then, type "Jupyter Notebook" to launch the application used to write and run this program.  It's outside of the scope of this README.md file to explain the installation of Jupyter Notebook.  The program itself can be found in this directory:(http://www.github.com/cryptopher2022/Challenge_4)


---

## Usage

Screenshots of the code and graphs are found below, stepwise with the process of evaluating.  I will provide a sample of the different analyses described in more detail above.  

1. This shows the process of importing the data:
![Import Data](../Challenge_4/images/1.%20Import%20the%20data.png)

2. This shows the probably the most important set of calculations throughout this analysis as all other functions will rely on the Daily Return Percentage: ![Daily Return %](../Challenge_4/images/2.%20Calculate%20daily%20percentage%20change.png)

3. As a part of the analysis, visualization of the data can reveal certain characteristics not readily seen from numbers in a table.  Therefore, plotting the data in different ways can prove very important.  ![Visualization](../Challenge_4/images/3.%20Visualization%20of%20data.png)

4. Different types of plots can be employed to reveal various factors important to a financial analyst.  Such as this box plot. This can tell us a lot about the volatility of each fund. ![Box Plot](../Challenge_4/images/4.%20Box%20plot.png)

5. Plots of standard deviations, variances, covariances, Sharpe Ratios and the like all have their place in financial analysis and are provided in this program.  ![STD](../Challenge_4/images/5.%20Plots%20of%20STD%20and%20others.png)

6. The Sharpe Ratio is one of the most useful of all ratios.  But, it must be used in conjunction with the balance of the methodologies employed in this program to determine an appropriate portfolio.  ![Sharpe Ratio](../Challenge_4/images/6.%20Sharpe%20Ratio.png)


    



---

## Contributors

This was done solely by Christopher Todd Garner

---

## License

Feel free to use this program and happy hunting for arbitrage profits.  Add some for loops or the like and optimal profits can be achieved.  
