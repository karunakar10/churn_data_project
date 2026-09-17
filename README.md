# churn_data_project
# Customer Churn Analysis Project

## Project Overview

This project analyzes customer churn data to understand why customers leave a company and which customer groups have higher churn risk.

The project starts with customer data stored in a SQLite database. The data is loaded into Python, cleaned, transformed, and analyzed using Pandas. Different churn metrics are calculated and visualizations are created to understand customer behavior.

## Objectives

- Calculate the overall customer churn rate
- Calculate the customer retention rate
- Analyze churn based on plan type
- Analyze churn across different states
- Analyze churn based on subscription type
- Calculate revenue loss from churned customers
- Create a churn score and classify customers into different risk levels
- Analyze monthly churn trends
- Create visualizations to understand churn patterns

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SQLite
- Jupyter Notebook
- Excel/CSV

## Project Workflow

1. Connect to the SQLite database
2. Extract tables and customer data
3. Explore the dataset
4. Clean and prepare the data
5. Handle missing values
6. Rename and remove unnecessary columns
7. Fix categorical values
8. Perform feature engineering
9. Create a customer churn flag
10. Calculate churn and retention metrics
11. Analyze churn by different customer segments
12. Calculate revenue loss due to churn
13. Create churn risk categories
14. Visualize churn patterns
15. Export the final dataset to CSV

## Data Cleaning

The following data-cleaning operations were performed:

- Renamed the `name` column to `customer_name`
- Removed unnecessary columns such as `pincode` and `interests`
- Converted the `dob` column into datetime format
- Standardized gender values such as `Men` to `Male` and `Women` to `Female`
- Filled missing country values using state-country mapping
- Checked the structure and information of the datasets

## Feature Engineering

A new column called `customer_churn` was created.

- `1` = Customer cancelled the service
- `0` = Customer did not cancel the service

The churn flag was created using the customer's cancellation date.

A `churn_risk` column was also created based on the churn score:

- Low Risk: Churn score <= 40
- Medium Risk: Churn score between 41 and 60
- High Risk: Churn score > 60

## Analysis Performed

### 1. Overall Churn Rate

The percentage of customers who cancelled their service was calculated using the `customer_churn` column.

### 2. Retention Rate

The retention rate was calculated as:

Retention Rate = 100 - Churn Rate

### 3. Churn by Plan Type

Customer churn was analyzed for different plan types such as:

- Basic
- Standard
- Premium

### 4. Churn by State

Churn rate, total monthly revenue, and number of customers were analyzed for different states.

### 5. Churn by Subscription Type

Customer churn was analyzed based on subscription type.

### 6. Revenue Loss

The total monthly charges associated with churned customers were calculated to understand the revenue affected by customer churn.

### 7. Churn Risk Analysis

Customers were classified into low, medium, and high churn-risk groups using their churn scores.

## Data Visualization

The project includes several visualizations:

- Monthly churn trend
- Churn by plan type
- Churn by state
- Correlation heatmap
- Pair plot
- Churn risk and monthly charge comparison

These visualizations help identify patterns and relationships in customer churn.

## Project Files

```text
Restaurant-Analytics-Project/
│
├── churn_data_project.ipynb
├── customer_churn.db
├── churn_data_excel_csv.csv
└── README.md
