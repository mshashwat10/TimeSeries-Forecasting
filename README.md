# TimeSeries-Forecasting - Case studies

# 1. Paperback vs Hardcover

The data set used here is "Books", it has Sales data of the paperback and hardcover books. In general hardcover books are 
published first so as part of the data analysis I am building a linear regression model to identify the effect of hardcover book sales on paperback book sales.This is useful in terms of estimating the sales for paperback books and the information can be used for identifying the optimal no of books to be published.


![Paperback vs Hardcover](https://user-images.githubusercontent.com/38140470/82738326-65b0d200-9cfc-11ea-9f9f-242126961db3.png)

![Regression Fit](https://user-images.githubusercontent.com/38140470/82739033-0d7cce80-9d02-11ea-9989-e8df27156795.png)

After seeing the results, we can see Hardcover(x) is not significant(p-value < 0.05) in predicting sales for Hardcover(y)

# 2. Simple Exponential Smoothing

Exponential Smoothing is one of the most popular forecasting techniques, best fit for short-term forecasts without trend
or seasonality. Values of alpha(smoothing constant) is chosen based on the value that gives the lowest RMS value,
another point is that it gives more weight to the current data than the past.Bigger Alpha means you are giving more weight to the recent data.

Beer dataset is used to perform SES forecasting technique, running the SES keeping alpha as 0.1, h=25( no of periods for forecast) and CI as 80,95 we observe the value of RMS as 19.96
![Simple Exp Smoothing , Alpha = 0 1](https://user-images.githubusercontent.com/38140470/82739101-82e89f00-9d02-11ea-998f-b266cffd8392.png)

Running the SES second time keeping alpha as 0.5, we observe the value of RMS as 20.155
![SES Alpha = 0 5](https://user-images.githubusercontent.com/38140470/82739105-8714bc80-9d02-11ea-99cd-a1969a9a68d3.png)

Since keeping Alpha as 0.5 gives us the lesser RMS value so we will use this value of alpha for our final forecasting model
