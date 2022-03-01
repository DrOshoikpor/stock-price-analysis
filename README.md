# Stock Price Analysis and prediction
##### Monday Oshoikpor
## Problem Statement
**A day in the life of a data scientist in an Investment Brokerage Firm**


I am a data scientist at CANOJOPA Inc.,a renowned investment brokerage firm in the Bay area of California.This company specializes in buying and selling securities, like stocks, on an exchange market for individuals as well as businesses.

One of my many daily task at CANOJOPA Inc.is to run series of analysis on a 5-year historical data of Amazon Inc., Adobe Inc., Microsoft Corporation and Square Inc. and come up with recommendation for our client.I have decided to draft metrics which can measures the performance of the stocks as well as run predictions on adjusted closing prices.

The metrics include:

- To determine the change in price of the stock over time.

- To determine the daily return of the stock on average.

- To determine the moving average of the various stocks.

- To determine the correlation between different stocks.

- To determine how much value we put at risk by investing in a particular stock.

- To determine how we can attempt to predict future stock behavior


![pexels-pixabay-210607.jpg](https://images.pexels.com/photos/210607/pexels-photo-210607.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260)


[Image from here](https://www.pexels.com/photo/stock-exchange-board-210607/)
## Executive Summary
I used the yahoo finance Application Programming Interface(API) to  a 5-year historical data of Amazon Inc., Adobe Inc., Microsoft Corporation and Square Inc. for this project. The goal is to make at least one prediction as well as answer the problem statement.

The project was carried out in one notebook but different sections with one section answering each of the metrics stated in the problem statement.

Conclusions and recommendations were made based on the analysis of each of the sections.
## Sources
1) [Read more about Yahoo finance here](https://finance.yahoo.com/)


2) [Image here](https://www.pexels.com/search/stock%20market/)
## Data Dictionary
| column    | Type  | Description                                                                                               |
|-----------|-------|-----------------------------------------------------------------------------------------------------------|
| High      | float | The maximum stock prices in a given time period                                                           |
| Low       | float | The minimum stock prices in a given time period.                                                          |
| Open      | float | Open is the prices at which a stock began trading in a given period                                       |
| Close     | float | Close is the prices at which a stock ended trading in a given  period                                     |
| Volume    | int   | Volume is the total amount of trading activity                                                            |
| Adj Close | float | Adjusted Close price including factors in corporate actions such as dividends, stock split and new shares






[Data Dictionary Made from Here](https://www.tablesgenerator.com/markdown_tables#)


[References about descriptions](https://analyzingalpha.com/open-high-low-close-stocks)
## Conclusion
This project carried out an analysis on stock price for four different companies including Adobe Inc. (ADBE), Amazon.com Inc. (AMZN), Microsoft Corporation (MSFT) and Square Inc. (SQ) for a period of five(5) years starting from 11/19/2016 to 11/19/2021 .

The goal of the analysis is:

 * To determine the change in price of the stock over time.
 * To determine the daily return of the stock on average.
 * To determine the moving average of the various stocks.
 * To determine the correlation between different stocks.
 * To determine how much value, we put at risk by investing in a particular stock.
 * To determine how we can attempt to predict future stock behavior?


After the analysis, the following were findings for each of the companies investigated.


**Adobe**

 - Adobe closing price started very low in in november,2016 at 105.65 dollars and grew to $688.369995 On November 19th, 2021.


 - An average return that shows right skewness.


- Adobe stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.


 -  Adobe also shows a positive expected return at slightly above 2.1% risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 3.2% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run value at risk analysis on the returns and turns out that for every initial ADOBE stock you purchase you are putting about 4.10 dollars at risk of investment of $104.12 99% of the time.


 - We trained a model to predict adobe stock using linear regression (LR)model.


 - The Mean Absolute Error was 1.5 indicating that our error from the forcast on average is really small


 - Mean Squared Error was 4.4 telling us how close we are to finding the line of best fit


 - Root Mean Squared Error was 2.1 which is standard deviation of the unexplained variance


 - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.

 - The Cross Validation. score was 99.98% showing the extent of our model performance




 **Microsoft**


 - Microsoft closing price started in November 2016 at 60.860001 dollars and grew to $343.109985 in November 2021.


 - An average return that shows right skewness.


 - Microsoft stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.


 - Microsoft also shows a positive expected return at 1.75% risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 2.6% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Microsoft stock you purchase you are putting about 2.34 dollars at risk of investment of $59 99% of the time.


 - We trained a model to predict Microsoft stock using linear regression (LR)model.


 - The Mean Absolute Error was 0.6 indicating that our error from the forcast on average is really small


 - Mean Squared Error was 0.8 telling us how close we are to finding the line of best fit


 - Root Mean Squared Error was 0.9 which is standard deviation of the unexplained variance


 - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.

 - The Cross Validation. score was 99.98% showing the extent of our model performance



**Square**


 - Square closing price started in november, 2016 at 12.22 dollars and grew above $225.139999 in November 2021.


 - An average return that shows right skewness.


 - Square stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.


 - Square also shows a positive expected return at 3.5 % risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 4.7% using bootsrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Square stock you purchase you are putting about 0.48 dollars at risk of investment of $12.12 99% of the time.


- We trained a model to predict Square stock using linear regression (LR)model.


 - The Mean Absolute Error was 0.9 indicating that our error from the forcast on average is really small


 - Mean Squared Error was 1.9 telling us how close we are to finding the line of best fit


 - Root Mean Squared Error was 1.4 which is standard deviation of the unexplained variance


 - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.97%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.

 - The Cross Validation. score was 99.97% showing the extent of our model performance.



**Amazon**


 - Amazon closing price started in November,2016 at 743.239990 dollars and grew above $3549.935059 in November 2021.


 - An average return that was normally distributed.
Amazon stock correlated well with itself and other stocks in this project. This is necessary when making investment on different stocks.


 - Amazon also shows a positive expected return at 1.5 % risk of investment. There is also quantile daily return that with 95% confidence, our worst daily loss will not exceed 2.8% using bootstrap method to value the risk of investment. A Monte Carlo method was also used to run risk analysis on the returns and turns out that for every initial Amazon stock you purchase you are putting about 28.96 dollars at risk of investment of $745.51 99% of the time.


- The Mean Absolute Error was 1.5 indicating that our error from the forecast on average is really small


 - Mean Squared Error was 219.47 telling us how close we are to finding the line of best fit


 - Root Mean Squared Error was 2.1 which is standard deviation of the unexplained variance


 - The R-Squared shows if the model is a good fit for predicted values and how good of a “fit” it is.The higher the better and our algorithm shows 99.98%.This means that 99.98% of the data fits the regression line which is a fantastic fit for the model.

 - The Cross Validation. score was 99.97% showing the extent of our model performance
## Recommendations
Based on the series of analysis and evaluations we conducted, we recommend the following:


 - All stock has an upward trend showing a consistent rise in closing price( which forms a major consideration investors) with little fluctuations. Value at risk is low on all stocks for risk averse client as well as clients with high level of risk tolerance. Returns on investments though varies across stocks, there seems to be a decent correlation between stocks which means a combination of investment in the stocks we investigated will return a good yeild.We recommend  for our clients to invest at least 365 days without any interferance with the investment for our recommendations to be fully utilized.

 - On the part of our model, we were able to show that there is a strong relationship between our predictions and actual price. This means that our trained model can generalize well with unseen but similar data.

 - As part of our principles on "growth" and to improve our services to our clients, we planned a good control system were can build other models such as the Autoregressive Integrated moving avereage(ARIMA) to try to predict closing price in the future.
