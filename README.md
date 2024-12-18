# Car Price Prediction Using Machine Learning

## Overview

This project aims to build a machine learning model that predicts the price of used cars based on various features such as the car's age, number of kilometers driven, fuel type, transmission type, and other related factors. The model is developed using **PySpark** and **Random Forest Regressor**. It also includes feature preprocessing, model evaluation, and performance optimization.

## Objective

- To predict the price of a car based on features like fuel type, transmission type, number of kilometers driven, and other factors.
- To provide a reliable car price prediction system for businesses involved in buying and selling used cars.

## Dataset

The dataset used in this project contains used car listings with features such as:

- **Seller_Type**: Type of seller (e.g., individual, dealership)
- **Transmission**: Type of transmission (manual/automatic)
- **Owner**: Number of previous owners
- **Fuel_Type**: Type of fuel used (e.g., petrol, diesel)
- **Present_Price**: Current price of the car
- **Kms_Driven**: Number of kilometers driven by the car
- **No_of_years**: Age of the car (in years)
- **Price**: Target variable (Price of the car)

## Steps Taken

### 1. **Data Preprocessing:**
   - **Handling Missing Values:** Missing data was handled by removing or filling in missing values.
   - **Feature Engineering:** Categorical features were encoded using **One-Hot Encoding** to convert them into a format suitable for machine learning models.
   - **Log Transformation:** The target variable `Price` was log-transformed to make the distribution more normal.

### 2. **Model Building:**
   - **Pipeline Construction:** A pipeline was used to streamline the entire process, including preprocessing (One-Hot Encoding, Scaling) and the model itself.
   - **Cross-Validation:** Cross-validation was used to optimize hyperparameters and evaluate model performance.
   - **Random Forest Regressor:** This model was chosen due to its ability to handle non-linear relationships and its robustness.

### 3. **Model Evaluation:**
   - The model was evaluated using the following metrics:
     - **Root Mean Squared Error (RMSE):** Measures the average magnitude of the errors between predicted and actual values.
     - **Mean Absolute Error (MAE):** Measures the average of the absolute errors.
     - **R-squared (R2):** Measures how well the model explains the variance in the target variable.
   - Evaluation Results:
     - **RMSE:** 0.0948
     - **MAE:** 0.0621
     - **R2:** 0.9947
