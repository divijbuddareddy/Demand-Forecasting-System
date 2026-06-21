# Demand Forecasting Using Machine Learning

## Project Overview

This project predicts future weekly sales using Machine Learning techniques. The model analyzes historical sales data, economic indicators, seasonal patterns, and store-related information to forecast future demand.

The objective is to help businesses improve inventory management, production planning, workforce allocation, and decision-making.

---

## Problem Statement

Businesses often struggle with:

* Overstocking inventory
* Stock shortages
* Poor production planning
* Increased operational costs
* Inaccurate sales predictions

This project addresses these challenges by forecasting future demand using historical sales data.

---

## Dataset

Dataset Used: Walmart Weekly Sales Dataset

### Features

| Feature      | Description                                   |
| ------------ | --------------------------------------------- |
| Store        | Store ID                                      |
| Date         | Weekly sales date                             |
| Weekly_Sales | Weekly sales amount (Target Variable)         |
| Holiday_Flag | Indicates whether the week contains a holiday |
| Temperature  | Average temperature during the week           |
| Fuel_Price   | Fuel price during the week                    |
| CPI          | Consumer Price Index                          |
| Unemployment | Regional unemployment rate                    |

Dataset Size:

* 6435 Records
* 8 Original Features

---

## Feature Engineering

Additional features were created from the Date column:

* Year
* Month
* Day
* Weekday

Historical sales features:

### Lag Features

Lag features help the model learn from previous sales patterns.

* Lag_1 → Previous week's sales
* Lag_2 → Sales from two weeks ago

### Rolling Average

Rolling_4 → Average sales of the previous four weeks

---

## Machine Learning Model

### Random Forest Regressor

The Random Forest algorithm was used because:

* Handles non-linear relationships
* Works well on tabular business data
* Requires minimal preprocessing
* Produces highly accurate predictions

---

## Model Training Pipeline

1. Data Loading
2. Data Cleaning
3. Date Conversion
4. Feature Engineering
5. Lag Feature Creation
6. Rolling Average Calculation
7. Train-Test Split
8. Random Forest Training
9. Prediction
10. Model Evaluation

---

## Model Performance

Evaluation Metrics:

### Mean Absolute Error (MAE)

48,036.68

### R² Score

0.9775

The model explains approximately 97.75% of the variance in weekly sales.

---

## User Inputs

The deployed application accepts the following inputs:

| Input        | Description                          |
| ------------ | ------------------------------------ |
| Store        | Store Number                         |
| Holiday_Flag | Holiday Indicator (0 or 1)           |
| Temperature  | Weekly Temperature                   |
| Fuel_Price   | Fuel Price                           |
| CPI          | Consumer Price Index                 |
| Unemployment | Unemployment Rate                    |
| Year         | Forecast Year                        |
| Month        | Forecast Month                       |
| Day          | Forecast Day                         |
| Weekday      | Day of Week                          |
| Lag_1        | Previous Week Sales                  |
| Lag_2        | Sales Two Weeks Ago                  |
| Rolling_4    | Average Sales of Previous Four Weeks |

---

## Prediction Output

The application returns:

### Predicted Weekly Sales

Example:

Predicted Weekly Sales: 1,745,320.45

This value represents the estimated demand for the selected week.

---

## Business Applications

This project can be used in:

### Retail Stores

* Inventory Management
* Sales Forecasting
* Demand Planning

### E-Commerce

* Product Demand Prediction
* Stock Optimization
* Seasonal Planning

### Restaurants

* Ingredient Planning
* Food Demand Forecasting

### Manufacturing

* Production Planning
* Raw Material Forecasting
* Capacity Management

---

## Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Scikit-Learn
* Joblib
* Matplotlib

### Machine Learning

* Random Forest Regressor

### Deployment

* Gradio
* Hugging Face Spaces

---

## Project Structure

```text
Demand-Forecasting/
│
├── app.py
├── demand_forecasting_model.pkl
├── requirements.txt
├── Walmart.csv
├── README.md
```

## Conclusion

This project demonstrates how Machine Learning can be used to forecast future demand using historical sales and economic indicators. The model achieved an R² Score of 0.9775, indicating strong predictive performance and practical applicability in real-world business environments.

