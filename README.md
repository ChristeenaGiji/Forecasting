# Forecasting

This project aims to forecast monthly milk production for the next year (1976) using historical data and the Prophet forecasting model. The analysis involves cleaning the dataset, fitting the Prophet model with yearly seasonality, creating future dates for predictions, and evaluating the model's performance through cross-validation.

Dataset
The dataset used for this project is sourced from Kaggle, containing monthly milk production data from 1962 to 1975. The data is clean and structured with columns representing the date and the corresponding milk production values.
https://www.kaggle.com/datasets/pkmisra/monthly-milk-production-pounds

Steps and Methodology
Data Preparation:

Loaded the dataset and ensured it is in the required format with columns ds (datestamp) and y (milk production).
Converted the date column to datetime format and checked for any missing values or anomalies.
Model Fitting with Prophet:

Initialized the Prophet model, disabling weekly and daily seasonality to focus only on yearly seasonality (yearly_seasonality=True, weekly_seasonality=False, daily_seasonality=False).
Fitted the model to the historical data (1962-1975).
Creating Future Dates:

Generated future dates for the next 365 days, which translates to predicting monthly milk production for the year 1976.
Model Prediction:

Used the fitted model to predict milk production for the generated future dates.
Cross-Validation:

Implemented cross-validation to evaluate the model's performance. The data from 1962 to 1964 was used as the training set, and the data from 1965 onwards was used as the testing set.
Evaluated the model using various performance metrics like MAPE (Mean Absolute Percentage Error), RMSE (Root Mean Squared Error), and other relevant metrics.
Performance Metrics:

Calculated and analyzed the performance metrics to assess the model's accuracy and reliability in predicting future milk production.
Results
The Prophet model, configured with only yearly seasonality, successfully captured the trends in the historical milk production data.
The predictions for the year 1976 provided a reliable estimate of monthly milk production.
Cross-validation showed satisfactory performance metrics, with MAPE and RMSE values indicating the model's predictive power and accuracy.
