# Time-Series-Analysis-of-Inside-Airbnb-Zurich-data

![Inside Airbnb Zurich](./images/Screenshot%202023-04-25%20at%2000.34.17.png)


This repository contains data used in a study on Airbnb listings in Zurich, Switzerland. The data were obtained from InsideAirbnb.com, an independent, non-commercial website that provides data and tools to explore how Airbnb is used in cities around the world.

## Data
The data used in this study are a time snapshot compiled on January 01, 2023, and contain publicly available information about Airbnb listings in Zurich. The data set chosen for this study is reviews.csv, which includes summary review data and Listing IDs. This file was selected to facilitate time-based analytics and visualizations linked to a specific listing.

## Usage

I perform the Dickey-Fuller test on the time series to test for stationarity . The Dickey-Fuller test is a statistical test used to determine if a time series is stationary or not. A stationary time series is one whose statistical properties such as mean and variance do not change over time. Stationarity is an important property for time series analysis and forecasting.In the context of analysis, the rolling mean and rolling standard deviation are statistical measures calculated for the given time series. The rolling mean is the average of the time series values within a specified window, calculated for each point in time. Similarly, the rolling standard deviation is the standard deviation of the time series values within a specified window, calculated for each point in time. In this case, the window size is 12.

These measures are used to smooth out short-term fluctuations and highlight longer-term trends or cycles in the data. By plotting them along with the original time series, it is possible to visually assess if the time series is stationary or not.

The test statistic is the result of the test, and the p-value is the probability of observing a test statistic as extreme as the one calculated if the null hypothesis (that the time series has a unit root and is therefore non-stationary) is true. When the p-value > 0.05, it means that there is not enough evidence to reject the null hypothesis at significance level of 5%.


## Source
All data were obtained from InsideAirbnb.com, and are provided under a Creative Commons CC0 1.0 Universal (CC0 1.0) Public Domain Dedication.

## License
The data used in this repository are licensed under a Creative Commons CC0 1.0 Universal (CC0 1.0) Public Domain Dedication.
