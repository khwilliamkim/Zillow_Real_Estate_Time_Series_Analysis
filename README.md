# Zillow Real Estate Time Series Analysis

Author: Kyunghwan William Kim
Track: Data Science Flex

## Time Series Model for Real Estate Investment Company

This project assumes to be an investment firm based in Long Island New York to provide detailed analysis and insights to investors who are interested in real estate for financial growth. Our target clients are mid-income families or individuals with initial budget under $1,000,000 and are looking to buy in 2023.

The scope of this project will be to conduct a time series analysis to predict the 5 best zipcodes to invest in based on ROI.

What we’ll be doing in this project is analyzing these features of a time series data set, and then seeing if we can use mathematical models to forecast into the future. We’ll also see how we can split our original time series data set to evaluate how well our model predicts the future.

### Our Data

This project will explore the Housing Prices in the United States, from the years 1996 - 2018, with our frequency being Monthly Production output.

Each row represents a unique zip code. Each record contains location info and median housing sales prices for each month.

There are 14,723 rows and 272 variables:
* RegionID: Unique index
* RegionName: Unique Zip Code
* City: City related to Zip Code
* State: State related to Zip Code
* Metro: Metropolitan Area related to Zip Code
* CountyName: County related to Zip Code
* SizeRank: Numerical rank of size of Zip Code
* 1996-04 through 2018-04: refers to the median housing sales values for April 1996 through April 2018

### Success Metrics

To solve the problems raised under business understanding, two columns will be created.

* Return on Investment (ROI) 

ROI is the measure of expected returns from investments
    
* Coefficient of Variation (CV)

CV is a measure of the dispersion of data points around the mean and represents the ratio of the standard deviation to the mean. It allows investors to determine how much volatility, or risk, is assumed in comparison to the amount of return expected from investments.

### Project Steps

#### 1. Load the Data/Filtering for Chosen Zipcodes
* Filter to Nassau County New York

#### 2. EDA and Data Cleaning
* Success Metrics
* Check for Null Values
* Filter with Clients Budget

#### 3. Data Preprocessing 
* Change from Wide to Long Format

#### 4. Data Visualization
* Cities with Highest Median House Value
* Zipcodes with Highest CV
* Zipcodes with Highest ROI
* Deeper look onto 2008 Housing Crisis
 
#### 5. Time Series Basics
Time Series data is experimental data that has been observed at different points in time.

Time series provide the opportunity to predict/forecast future values based on previous values. Such analyses can be used to forecast trends in economics, weather, and capacity planning etc.

* Forecasting with ARIMA
* Seasonality
* Stationarity
* ACF and PACF
* Detrending by Differencing

Prices seem to have peaked before the 2008 recession, only to see a dramatic fall immediately after. Since then, prices have been steadily on the rise since 2012 but have yet to reach their pre-recession peaks.

##### 6. Model #1. Autoregression
##### 7. Model #2. AR(2)
##### 8. Model #3. Moving Average
##### 9. Model #4. MA(2)
##### 10. Model #5. ARIMA
##### 11. Model #6. SARIMA
##### 12. Model #7. SARIMA with one zipcode
##### 13. Model #8. SARIMA with five zipcodes

#### 6. Model #9. (S)ARIMA Model with all zipcodes
We want to build a Time Series model to predict the future ROI for each zip code in Nassau County that would fit our client's budget. But first, we will select 5 specific zipcode to build our time series model on. For this purpose, we decided to use the highest growing zipcode since 2012.

* Initial Model using 5 Sample Zipcodes
* Final Model using All Zipcodes

##### 7. Dynamic Forecasting
* Train/Test
The train-test split for a time series is a little different from what we are used to. Because chronological order matters, we cannot randomly sample points in our data. Instead, we cut off a portion of our data at the end, and reserve it as our test set.
* Top 5 Zipcodes with highest 5yr ROI

#### 8. Interpret Results
Based on the 5 year ROI, below 5 zipcodes stand out to be the best to invest for real estate investors.

11735: Farmingdale, NY (-70% to 211%)
11803: Plainview, NY (-148% to 287%)
11598: Woodmere, NY (-11% to 133%)
11003: Elmont, NY (-33% to 154%)
11552: West Hempstead, NY (3% to 114%)
The zipcodes with the highest price volatility are:

11575: Roosevelt, NY
11096: Inwood, NY
11561: Long Beach, NY
11550: Hempstead, NY
11553: Uniondale, NY
Meaning that real estate investors should not invest in these areas

The methods we will employ in this project example will only take in data from a uni-variate time series. That means we really are only considering the relationship between the y-axis value the x-axis time points. We’re not considering outside factors that may be effecting the time series
