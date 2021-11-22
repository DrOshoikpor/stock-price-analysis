{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "bd6123ae",
   "metadata": {},
   "source": [
    "# Stock Price Analysis and prediction"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "01473deb",
   "metadata": {},
   "source": [
    "##### Monday Oshoikpor"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "37fb3498",
   "metadata": {},
   "source": [
    "## Problem Statement"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "80df5a8d",
   "metadata": {},
   "source": [
    "**A day in the life of a data scientist in an Investment Brokerage Firm**\n",
    "\n",
    "\n",
    "I am a data scientist at CANOJOPA Inc.,a renowned investment brokerage firm in the Bay area of California.This company specializes in buying and selling securities, like stocks, on an exchange market for individuals as well as businesses.\n",
    "\n",
    "One of my many daily task at CANOJOPA Inc.is to run series of analysis on a 5-year historical data of Amazon Inc., Adobe Inc., Microsoft Corporation and Square Inc. and come up with recommendation for our client.I have decided to draft metrics which can measures the performance of the stocks as well as run predictions on adjusted closing prices.\n",
    "\n",
    "The metrics include:\n",
    "\n",
    "- To determine the change in price of the stock over time.\n",
    "\n",
    "- To determine the daily return of the stock on average.\n",
    "\n",
    "- To determine the moving average of the various stocks.\n",
    "\n",
    "- To determine the correlation between different stocks.\n",
    "\n",
    "- To determine how much value we put at risk by investing in a particular stock.\n",
    "\n",
    "- To determine how we can attempt to predict future stock behavior?"
   ]
  },
  {
   "attachments": {
    "pexels-pixabay-210607.jpg": {
    }
   },
   "cell_type": "markdown",
   "id": "afd8686c",
   "metadata": {},
   "source": [
    "![pexels-pixabay-210607.jpg](attachment:pexels-pixabay-210607.jpg)\n",
    "\n",
    "\n",
    "[Image from here](https://www.pexels.com/photo/stock-exchange-board-210607/)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "65905231",
   "metadata": {},
   "source": [
    "## Executive Summary"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2706c13b",
   "metadata": {},
   "source": [
    "I used the yahoo finance Application Programming Interface(API) to  a 5-year historical data of Amazon Inc., Adobe Inc., Microsoft Corporation and Square Inc. for this project. The goal is to make at least one prediction as well as answer the problem statement.\n",
    "\n",
    "The project was carried out in one notebook but different sections with one section answering each of the metrics stated in the problem statement.\n",
    "\n",
    "Conclusions and recommendations were made based on the analysis of each of the sections."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1bfdb9bd",
   "metadata": {},
   "source": [
    "## Sources"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9dae9ba7",
   "metadata": {},
   "source": [
    "1) [Read more about Yahoo finance here](https://finance.yahoo.com/)\n",
    "\n",
    "\n",
    "2) [Image here](https://www.pexels.com/search/stock%20market/)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "de98c129",
   "metadata": {},
   "source": [
    "## Data Dictionary"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "cd156ae0",
   "metadata": {},
   "source": [
    "| column    | Type  | Description                                                                                               |\n",
    "|-----------|-------|-----------------------------------------------------------------------------------------------------------|\n",
    "| High      | float | The maximum stock prices in a given time period                                                           |\n",
    "| Low       | float | The minimum stock prices in a given time period.                                                          |\n",
    "| Open      | float | Open is the prices at which a stock began trading in a given period                                       |\n",
    "| Close     | float | Close is the prices at which a stock ended trading in a given  period                                     |\n",
    "| Volume    | int   | Volume is the total amount of trading activity                                                            |\n",
    "| Adj Close | float | Adjusted Close price including factors in corporate actions such as dividends, stock split and new shares\n",
    "\n",
    "\n",
    "\n",
    "\n",
    "\n",
    "\n",
    "[Data Dictionary Made from Here](https://www.tablesgenerator.com/markdown_tables#)\n",
    "\n",
    "\n",
    "[References about descriptions](https://analyzingalpha.com/open-high-low-close-stocks)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f665f249",
   "metadata": {},
   "source": [
    "## Conclusion"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7ed25216",
   "metadata": {},
   "source": [
    "This project carried out an analysis on stock price for four different companies including Adobe Inc. (ADBE), Amazon.com Inc. (AMZN), Microsoft Corporation (MSFT) and Square Inc. (SQ) for a period of five(5) years starting from 11/19/2016 to 11/19/2021 .\n",
    "\n",
    "The goal of the analysis is:\n",
    "\n",
    " * To determine the change in price of the stock over time.\n",
    " * To determine the daily return of the stock on average.\n",
    " * To determine the moving average of the various stocks.\n",
    " * To determine the correlation between different stocks.\n",
    " * To determine how much value, we put at risk by investing in a particular stock.\n",
    " * To determine how we can attempt to predict future stock behavior?\n",
    "\n",
    "\n",
    "After the analysis, the following were findings for each of the companies investigated.\n",
    "\n",
    "\n",
    "**Adobe**\n",
    "\n",
    " - Adobe closing price started very low in in november,2016 at 105.65 dollars and grew to $688.369995 On November 19th, 2021.\n",
    "\n",
    "\n",
    " - An average return that shows right skewness.\n",
    "\n",
    "\n",
    "- Adobe stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.\n",
    "\n",
    "\n",
    " -  Adobe also shows a positive expected return at slightly above 2.1% risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 3.2% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run value at risk analysis on the returns and turns out that for every initial ADOBE stock you purchase you are putting about 4.10 dollars at risk of investment of $104.12 99% of the time.\n",
    "\n",
    "\n",
    " - We trained a model to predict adobe stock using linear regression (LR)model.\n",
    " \n",
    " \n",
    " - The Mean Absolute Error was 1.5 indicating that our error from the forcast on average is really small\n",
    "\n",
    "\n",
    " - Mean Squared Error was 4.4 telling us how close we are to finding the line of best fit\n",
    "\n",
    "\n",
    " - Root Mean Squared Error was 2.1 which is standard deviation of the unexplained variance\n",
    " \n",
    " \n",
    " - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.\n",
    " \n",
    " - The Cross Validation. score was 99.98% showing the extent of our model performance\n",
    "\n",
    "\n",
    "\n",
    "\n",
    " **Microsoft**\n",
    "\n",
    "\n",
    " - Microsoft closing price started in November 2016 at 60.860001 dollars and grew to $343.109985 in November 2021.\n",
    "\n",
    "\n",
    " - An average return that shows right skewness.\n",
    "\n",
    "\n",
    " - Microsoft stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.\n",
    "\n",
    "\n",
    " - Microsoft also shows a positive expected return at 1.75% risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 2.6% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Microsoft stock you purchase you are putting about 2.34 dollars at risk of investment of $59 99% of the time.\n",
    "\n",
    "\n",
    " - We trained a model to predict Microsoft stock using linear regression (LR)model.\n",
    " \n",
    "\n",
    " - The Mean Absolute Error was 0.6 indicating that our error from the forcast on average is really small\n",
    "\n",
    "\n",
    " - Mean Squared Error was 0.8 telling us how close we are to finding the line of best fit\n",
    "\n",
    "\n",
    " - Root Mean Squared Error was 0.9 which is standard deviation of the unexplained variance\n",
    " \n",
    " \n",
    " - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.\n",
    " \n",
    " - The Cross Validation. score was 99.98% showing the extent of our model performance\n",
    "\n",
    "\n",
    "\n",
    "**Square**\n",
    "\n",
    "\n",
    " - Square closing price started in november, 2016 at 12.22 dollars and grew above $225.139999 in November 2021.\n",
    "\n",
    "\n",
    " - An average return that shows right skewness.\n",
    "\n",
    "\n",
    " - Square stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.\n",
    "\n",
    "\n",
    " - Square also shows a positive expected return at 3.5 % risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 4.7% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Square stock you purchase you are putting about 0.48 dollars at risk of investment of $12.12 99% of the time.\n",
    "\n",
    "\n",
    "- We trained a model to predict Square stock using linear regression (LR)model.\n",
    " \n",
    "\n",
    " - The Mean Absolute Error was 0.9 indicating that our error from the forcast on average is really small\n",
    "\n",
    "\n",
    " - Mean Squared Error was 1.9 telling us how close we are to finding the line of best fit\n",
    "\n",
    "\n",
    " - Root Mean Squared Error was 1.4 which is standard deviation of the unexplained variance\n",
    " \n",
    " \n",
    " - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.97%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.\n",
    " \n",
    " - The Cross Validation. score was 99.97% showing the extent of our model performance.\n",
    "\n",
    "\n",
    "\n",
    "**Amazon**\n",
    "\n",
    "\n",
    " - Amazon closing price started in November,2016 at 743.239990 dollars and grew above $3549.935059 in November 2021.\n",
    "\n",
    "\n",
    " - An average return that was normally distributed.\n",
    "Amazon stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.\n",
    "\n",
    "\n",
    " - Amazon also shows a positive expected return at 1.5 % risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 2.8% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Amazon stock you purchase you are putting about 28.96 dollars at risk of investment of $745.51 99% of the time.\n",
    "\n",
    "\n",
    "- The Mean Absolute Error was 1.5 indicating that our error from the forcast on average is really small\n",
    "\n",
    "\n",
    " - Mean Squared Error was 219.47 telling us how close we are to finding the line of best fit\n",
    "\n",
    "\n",
    " - Root Mean Squared Error was 2.1 which is standard deviation of the unexplained variance\n",
    " \n",
    " \n",
    " - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.\n",
    " \n",
    " - The Cross Validation. score was 99.97% showing the extent of our model performance\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a8fa8eae",
   "metadata": {},
   "source": [
    "## Recommendations"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6be46708",
   "metadata": {},
   "source": [
    "Based on the series of analysis and evaluations we conducted, we recommend the following:\n",
    "\n",
    "\n",
    " - All stock has an upward trend showing a consistent rise in closing price( which forms a major consideration investors) with little fluctuations. Value at risk is low on all stocks for risk averse client as well as clients with high level of risk tolerance. Returns on investments though varies across stocks, there seems to be a decent correlation between stocks which means a combination of investment in the stocks we investigated will return a good yeild.We recommend  for our clients to invest at least 365 days without any interferance with the investment for our recommendations to be fully utilized.\n",
    " \n",
    " - On the part of our model, we were able to show that there is a strong relationship between our predictions and actual price. This means that our trained model can generalize well with unseen but similar data.\n",
    "\n",
    " - As part of our principles on \"growth\" and to improve our services to our clients, we planned a good control system were can build other models such as the Autoregressive Integrated moving avereage(ARIMA) to try to predict closing price in the future."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "de578a43",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.11"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}