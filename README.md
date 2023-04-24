# Time-Series-Analysis-of-Inside-Airbnb-Zurich-data

![Inside Airbnb Zurich](./images/Screenshot%202023-04-25%20at%2000.34.17.png)


This repository contains data used in a study on Airbnb listings in Zurich, Switzerland. The data were obtained from InsideAirbnb.com, an independent, non-commercial website that provides data and tools to explore how Airbnb is used in cities around the world.

## Data
The data used in this study are a time snapshot compiled on January 01, 2023, and contain publicly available information about Airbnb listings in Zurich. The data set chosen for this study is reviews.csv, which includes summary review data and Listing IDs. This file was selected to facilitate time-based analytics and visualizations linked to a specific listing.

## Usage

I perform the Dickey-Fuller test on the time series to test for stationarity . The Dickey-Fuller test is a statistical test used to determine if a time series is stationary or not. A stationary time series is one whose statistical properties such as mean and variance do not change over time. Stationarity is an important property for time series analysis and forecasting.In the context of analysis, the rolling mean and rolling standard deviation are statistical measures calculated for the given time series. The rolling mean is the average of the time series values within a specified window, calculated for each point in time. Similarly, the rolling standard deviation is the standard deviation of the time series values within a specified window, calculated for each point in time. In this case, the window size is 12.

These measures are used to smooth out short-term fluctuations and highlight longer-term trends or cycles in the data. By plotting them along with the original time series, it is possible to visually assess if the time series is stationary or not.

The test statistic is the result of the test, and the p-value is the probability of observing a test statistic as extreme as the one calculated if the null hypothesis (that the time series has a unit root and is therefore non-stationary) is true. When the p-value > 0.05, it means that there is not enough evidence to reject the null hypothesis at significance level of 5%.

To deal with non stationarity,a series of transformations applied to a time series stored in a DataFrame `df_example`. The original time series is stored in the `ts` column of the DataFrame. The following transformations are applied to the time series:

1. Log transformation: The natural logarithm of the time series values is calculated and stored in a new column `ts_log`.
2. 7-day moving average of the log-transformed time series: The 7-day moving average of the `ts_log` column is calculated and stored in a new column `ts_log_moving_avg`.
3. 7-day moving average of the original time series: The 7-day moving average of the `ts` column is calculated and stored in a new column `ts_moving_avg`.
4. Difference between the log-transformed time series and its first lag: The difference between the `ts_log` column and its first lag is calculated and stored in a new column `ts_log_diff`.
5. Difference between the original time series and its 7-day moving average: The difference between the `ts` column and the `ts_moving_avg` column is calculated and stored in a new column `ts_moving_avg_diff`.
6. Difference between the log-transformed time series and its 7-day moving average: The difference between the `ts_log` column and the `ts_log_moving_avg` column is calculated and stored in a new column `ts_log_moving_avg_diff`.
7. Exponentially weighted moving average (EWMA) of the log-transformed time series: The EWMA of the `ts_log` column with a half-life of 7 is calculated and stored in a new column `ts_log_ewma`.
8. Difference between the log-transformed time series and its EWMA: The difference between the `ts_log` column and the `ts_log_ewma` column is calculated and stored in a new column `ts_log_ewma_diff`.

After applying these transformations, several plots are created using the `plot_transformed_data` function to visualize the original time series and its transformed versions.




## Source
All data were obtained from InsideAirbnb.com, and are provided under a Creative Commons CC0 1.0 Universal (CC0 1.0) Public Domain Dedication.

## License
The data used in this repository are licensed under a Creative Commons CC0 1.0 Universal (CC0 1.0) Public Domain Dedication.
