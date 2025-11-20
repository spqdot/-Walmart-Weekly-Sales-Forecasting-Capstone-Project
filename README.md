# -Walmart-Weekly-Sales-Forecasting-Capstone-Project
 Walmart Weekly Sales Forecasting Capstone Project 
 📈 This project involves a comprehensive Time Series Analysis and Forecasting of Walmart's weekly sales data to predict future sales and identify key factors influencing performance across different store locations.
🌟 Project Overview
The primary objective of this capstone project is to develop an accurate forecasting model for Walmart's Weekly Sales using historical data and various external factors like holidays, temperature, fuel price, and economic indicators.The analysis is structured around data cleaning, exploratory data analysis (EDA), time series decomposition, and the application of various forecasting models to both the aggregated company-wide sales and individual high/low-performing stores.
💾 DataThe project utilizes the Walmart Weekly Sales Dataset, which contains 6,435 weekly records.Column NameDescriptionStoreThe store number (1 to 45).DateThe week of sales.Weekly_SalesTarget variable: Sales for the given week.Holiday_Flag1 if the week includes a major holiday, 0 otherwise.TemperatureAverage temperature in the region.Fuel_PriceCost of fuel in the region.CPIConsumer Price Index.UnemploymentUnemployment rate.

🛠️ Methodology and Analysis Tasks
The project followed a standard data science and time series workflow:

1. Data Cleaning and Preprocessing
Loaded the dataset and examined its structure.

Checked for missing and duplicate values (none were found).

Converted the Date column to the appropriate datetime format.

2. Exploratory Data Analysis (EDA)
Calculated summary statistics for all numerical columns.

Identified the Top Performing Store (Store 20) and the Worst Performing Store (Store 39) based on average weekly sales.

Analyzed correlations between Weekly_Sales and other features.

3. Time Series Analysis
Performed a Dickey-Fuller Test to check for stationarity, concluding the data is stationary.

Executed Seasonal Decomposition to visualize the trend, seasonality (period=52 weeks), and residual components of the sales data.

4. Sales Forecasting
Forecasting was conducted using three primary Time Series models:

AR (Autoregressive)

ARIMA (Autoregressive Integrated Moving Average)

SARIMA (Seasonal Autoregressive Integrated Moving Average) - selected as the best model.

Key Results and Observations Model Performance
The models were evaluated using Root Mean Squared Error (RMSE).ModelRMSE (Overall Sales)SARIMA 1,287,024.58, AR 1,799,834.98, ARIMA1,849,550.37
The SARIMA model demonstrated the lowest RMSE, confirming its superior ability to capture the inherent seasonality and provide the most accurate forecasts for the overall time series data.
Store-Specific Forecasting 
Best-performing Store (Store 20): The model was highly effective, accurately predicting sales trends and the seasonal spikes that occur, particularly in December.
Worst-performing Store (Store 39): In contrast, the model's forecasts for this store were highly inconsistent and unreliable, struggling to capture any meaningful pattern, likely due to low sales volume and higher data variability.
🚀 Technologies and LibrariesLanguage: PythonLibraries:pandas and numpy for data manipulationmatplotlib.pyplot and seaborn for data visualizationstatsmodels for time series modeling (AR, ARIMA, SARIMA)
