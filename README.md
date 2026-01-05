Flight Price Prediction Project

Project Overview

This project focuses on predicting flight prices using a dataset containing various flight-related features. The goal is to build and evaluate machine learning models to accurately forecast flight fares, providing insights into the factors influencing pricing.

Dataset

The project utilizes the Flight_Booking.csv dataset, which includes information such as airline, flight number, source/destination cities, departure/arrival times, number of stops, flight duration, days left until departure, and the price.

Methodology

1. Data Loading and Initial Exploration

The dataset was loaded into a pandas DataFrame.
Initial checks were performed using df.head(), df.info(), and df.isnull().sum() to understand the data structure and identify missing values. No missing values were found.
2. Data Preprocessing

The 'Unnamed: 0' column, which appeared to be an index, was dropped.
Label Encoding was applied to all categorical features to convert them into numerical representations suitable for machine learning models. The encoded features include: airline, source_city, departure_time, stops, arrival_time, destination_city, and class.
3. Exploratory Data Analysis (EDA)

Airline vs. Price: A line plot was generated to visualize the average price for each airline.
Days Left vs. Price: A line plot showed the relationship between the number of days left until departure and flight prices, indicating that prices tend to increase as the departure date approaches.
Correlation Heatmap: A heatmap was created to visualize the correlation matrix of the numerical features, helping to understand relationships between variables.
4. Feature Selection (VIF Analysis)

Variance Inflation Factor (VIF): VIF was calculated for all independent variables to detect multicollinearity. All VIF values were found to be low (below 5), suggesting no significant multicollinearity among the features. This indicates that all selected features can be used in the models without causing stability issues.
5. Model Training and Evaluation

Three different regression models were trained and evaluated on the dataset. The data was split into training (80%) and testing (20%) sets. The models were evaluated using the following metrics:

Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)
R-squared (R2)
Mean Absolute Error (MAE)
Mean Absolute Percentage Error (MAPE)
a. Linear Regression

R2: 0.9046
RMSE: 7014.31
MAE: 4624.99
MAPE: 43.54%
b. Decision Tree Regressor

R2: 0.9757
RMSE: 3540.01
MAE: 1171.29
MAPE: 7.39%
c. Random Forest Regressor

R2: 0.9849
RMSE: 2786.50
MAE: 1091.44
MAPE: 7.04%
Results and Conclusion

The Random Forest Regressor demonstrated the best performance among the three models, achieving the highest R-squared value (0.9849) and the lowest error metrics (RMSE, MAE, MAPE). This indicates that the Random Forest model is highly effective in capturing the complex relationships within the flight booking data and provides the most accurate predictions for flight prices.

The project successfully built and evaluated machine learning models for flight price prediction, with Random Forest emerging as the top-performing model. The analysis also provided insights into key factors influencing flight prices, such as 'class' and 'days_left'.

How to Run

This project was developed in a Google Colab environment. To run the notebook:

Upload the Flight_Booking.csv file to your Colab environment (e.g., to the /content/ directory).
Execute the cells sequentially.
