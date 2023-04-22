# Python_VaR_Calculation

The portfolio consists of 1) a long position (receiving float leg and paying fixed leg) in a USD 3M Libor fixed-to-floating swap with a notional of $100 millions; 2)$1 million in each of the four stocks: AAPL, MSFT, FORD, and BOA.

The Data file contains the infomation of 1) 1 year historical daily price of four stocks; 2) 1-year historical zero rates on the SOFR and 3M LIBOR curves; 3) the PV01s of the swap.

The purpose of this code is to calculate the 1-day 95% parametric/Monte Carlo/historical VaR for the portfolio.

Step1: calculate relative change for stock price and abosulte chnage for Libor and Sofr.

Step2: calculate the mean and standard deviation of the change to standardize the data

Step3:  generate correlation matrix and decomposed the correlation matrix by chloesky decomposition

Step4: calculate linear weights

Parametric VaR:
Calculate the mean and standard deviation of portfolio by combining standardized data with linear weights. And calculate VaR = mean + std * standard norm cdf (

