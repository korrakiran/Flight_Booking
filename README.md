# Flight Price Prediction Project

## Project Overview

This project focuses on predicting flight prices using a dataset containing various flight-related features. The objective is to build and evaluate machine learning models that can accurately forecast flight fares and provide insights into the factors influencing flight pricing.

---

## Dataset

The project uses the **Flight_Booking.csv** dataset, which includes the following features:

- Airline  
- Flight number  
- Source city  
- Destination city  
- Departure time  
- Arrival time  
- Number of stops  
- Flight duration  
- Days left until departure  
- Ticket price  

---

## Methodology

### 1. Data Loading and Initial Exploration

- The dataset was loaded into a pandas DataFrame.
- Initial exploration was carried out using:
  - `df.head()`
  - `df.info()`
  - `df.isnull().sum()`
- No missing values were found in the dataset.

---

### 2. Data Preprocessing

- The column **`Unnamed: 0`**, which acted as an index, was removed.
- Label Encoding was applied to categorical features to convert them into numerical form.
- Encoded features include:
  - `airline`
  - `source_city`
  - `departure_time`
  - `stops`
  - `arrival_time`
  - `destination_city`
  - `class`

---

### 3. Exploratory Data Analysis (EDA)

- **Airline vs Price**  
  A line plot was used to visualize the average ticket price for each airline.

- **Days Left vs Price**  
  A line plot showed that flight prices generally increase as the departure date approaches.

- **Correlation Heatmap**  
  A heatmap was generated to analyze correlations between numerical features and understand their relationships.

---

### 4. Feature Selection (VIF Analysis)

- **Variance Inflation Factor (VIF)** was calculated to detect multicollinearity among independent variables.
- All VIF values were below 5.
- This indicates no significant multicollinearity, so all features were retained for modeling.

---

### 5. Model Training and Evaluation

- The dataset was split into:
  - 80% training data
  - 20% testing data
- The following evaluation metrics were used:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R-squared (R²)
  - Mean Absolute Error (MAE)
  - Mean Absolute Percentage Error (MAPE)

#### a. Linear Regression

- R²: **0.9046**
- RMSE: **7014.31**
- MAE: **4624.99**
- MAPE: **43.54%**

#### b. Decision Tree Regressor

- R²: **0.9757**
- RMSE: **3540.01**
- MAE: **1171.29**
- MAPE: **7.39%**

#### c. Random Forest Regressor

- R²: **0.9849**
- RMSE: **2786.50**
- MAE: **1091.44**
- MAPE: **7.04%**

---

## Results and Conclusion

- The **Random Forest Regressor** achieved the best overall performance.
- It recorded the highest R² value and the lowest error metrics among all models.
- This indicates its strong ability to capture complex, non-linear relationships in flight pricing data.
- Key influencing factors identified include:
  - `class`
  - `days_left`

The project successfully demonstrates how machine learning can be applied to flight price prediction, with Random Forest emerging as the most effective model.

---

## How to Run

This project was developed using **Google Colab**.

Steps to execute:

1. Upload the `Flight_Booking.csv` file to the Colab environment (for example, `/content/`).
2. Run all notebook cells sequentially.
