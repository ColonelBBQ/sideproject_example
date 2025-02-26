# Customer Segmentation for Bank Users

## Project Overview

This project applies machine learning techniques to segment bank customers based on their transaction behaviors and account balances. By leveraging clustering methods, we identify distinct customer groups that could provide insights for financial institutions.

Code is found in main.ipynb

## Dataset

The original dataset was sourced from [Kaggle](https://www.kaggle.com/datasets/shivamb/bank-customer-segmentation/data) and contains over 1 million transactions with the following columns:

- **TransactionID**: Unique identifier for each transaction  
- **CustomerID**: Unique identifier for each customer  
- **CustomerDOB**: Customer date of birth  
- **CustGender**: Gender of the customer  
- **CustLocation**: Customer's location  
- **CustAccountBalance**: Account balance at the time of transaction  
- **TransactionDate**: Date of transaction  
- **TransactionTime**: Time of transaction  
- **TransactionAmount (INR)**: Amount transacted  

### Data Engineering

To create meaningful customer segments, we processed the raw data into a structured format with the following features:

- **Age**: Customer's age  
- **TransactionCount**: Number of transactions made  
- **TransactionAmountMean**: Average transaction amount  
- **TransactionAmountSum**: Total transaction amount  
- **AccountBalanceMax**: Maximum recorded account balance  
- **AccountBalanceMin**: Minimum recorded account balance  
- **AccountBalanceMean**: Average account balance  
- **Recency**: Days since the last transaction  

## Methodology

1. **Data Preprocessing**:  
   - Cleaned missing values  
   - Converted date fields to age and recency metrics  
   - Aggregated transactions at the customer level  

2. **Feature Scaling**:  
   - Standardized numerical features using `StandardScaler` to ensure uniform influence across clustering  

3. **Clustering (K-Means Algorithm)**:  
   - Used the **Elbow Method** to determine the optimal number of clusters  
   - Applied **K-Means** to segment customers based on transaction behaviors and account balances  

4. **Visualization with PCA**:  
   - Reduced dimensionality to 2 components for visualization  
   - Plotted customer segments to analyze grouping patterns  

## Results

The clustering process resulted in highly distinct customer groups, including:

- **High-net-worth individuals with infrequent but large transactions**  
- **Frequent low-value transaction users with lower account balances**  
- **Users who maintain high balances but conduct fewer transactions**  
- **Customers with sporadic usage patterns**  

These insights can help financial institutions tailor their services based on customer behaviors.

