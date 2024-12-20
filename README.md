# Big Sales Data Prediction

This project uses machine learning techniques to predict sales data for a large retail dataset. The goal is to predict the sales of items based on several features such as item weight, item type, outlet size, and others. The model employs a Random Forest Regressor to make these predictions.

## Table of Contents

- [Overview](#overview)
- [Libraries Used](#libraries-used)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Results Visualization](#results-visualization)
- [How to Run](#how-to-run)

## Overview

The project involves the following steps:

1. **Data Loading**: Import the dataset from a CSV file.
2. **Data Exploration**: Perform initial exploration of the dataset to understand its structure, data types, and identify missing values.
3. **Data Preprocessing**: Handle missing values, clean and transform categorical data, and standardize numerical features.
4. **Modeling**: Use a Random Forest Regressor to train a predictive model on the processed data.
5. **Evaluation**: Evaluate the model using metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-Squared (R²).
6. **Visualization**: Visualize the performance of the model by comparing actual and predicted sales values.

## Libraries Used

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For plotting graphs and visualizing data.
- `seaborn`: For enhanced data visualization.
- `sklearn`: For machine learning and data preprocessing (StandardScaler, RandomForestRegressor, etc.).

## Dataset

The dataset contains sales data for 14,204 rows and 12 columns. The columns include details such as item identifier, weight, fat content, visibility, item type, outlet type, and sales information. The data is loaded from a CSV file hosted on GitHub.

The dataset includes the following columns:
- **Item_Identifier**: Unique identifier for each item.
- **Item_Weight**: Weight of the item (with some missing values).
- **Item_Fat_Content**: Fat content of the item (categorical).
- **Item_Visibility**: Visibility of the item (numeric).
- **Item_Type**: Type of item (categorical).
- **Item_MRP**: Maximum retail price of the item.
- **Outlet_Identifier**: Identifier for the outlet.
- **Outlet_Establishment_Year**: Year the outlet was established.
- **Outlet_Size**: Size of the outlet (categorical).
- **Outlet_Location_Type**: Type of location for the outlet (categorical).
- **Outlet_Type**: Type of outlet (categorical).
- **Item_Outlet_Sales**: Target variable representing the sales of the item.

## Data Preprocessing

### Handling Missing Values
The missing values in the **Item_Weight** column are filled with the mean weight of the respective item type.

### Encoding Categorical Variables
Several categorical variables are encoded into numerical values:
- **Item_Fat_Content**: "Low Fat" and "Regular" are mapped to 0 and 1.
- **Item_Type**: Different item types are mapped to integer values.
- **Outlet_Identifier**: Outlet identifiers are mapped to integers.
- **Outlet_Size, Outlet_Location_Type, Outlet_Type**: Categorical variables are replaced with numerical values representing the categories.

### Standardization
The numerical features like **Item_Weight**, **Item_Visibility**, **Item_MRP**, and **Outlet_Establishment_Year** are standardized to ensure that all variables have the same scale.

## Feature Engineering

- **Independent Variables**: A set of features such as item weight, fat content, item type, outlet size, and location type are selected as independent variables for the model.
- **Dependent Variable**: The target variable is the **Item_Outlet_Sales**.

## Model Training

### Train-Test Split
The dataset is split into a training set (90%) and a test set (10%) to evaluate the model's performance on unseen data.

### Random Forest Regressor
A Random Forest Regressor is used to train the model. This ensemble method helps improve prediction accuracy by combining multiple decision trees.

## Model Evaluation

The model is evaluated using the following metrics:
- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted sales.
- **Mean Absolute Error (MAE)**: Measures the average absolute difference between actual and predicted sales.
- **R-Squared (R²)**: Represents the proportion of variance in the dependent variable that is predictable from the independent variables.

### Results
- **MSE**: 1,839,497.71
- **MAE**: 797.34
- **R²**: 0.457

## Results Visualization

The predicted sales are compared against the actual sales using a scatter plot to visually assess the model's performance.

## How to Run

1. Clone the repository to your local machine or open it on Google Colab.
2. Install the necessary libraries using the appropriate package manager.
3. Run the Jupyter Notebook.
4. Follow the steps outlined in the notebook to load the dataset, preprocess the data, train the model, and evaluate the results.

---

This project demonstrates how machine learning can be applied to retail sales data to predict item sales, offering valuable insights into store and product performance.
