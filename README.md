# Customer Segmentation Analysis

## Overview
This project focuses on customer segmentation for a banking dataset. It processes transaction data to group customers into distinct clusters based on their financial behaviors, demographics, and product preferences. The segmentation is performed using K-Means clustering algorithm with visualizations to illustrate the resulting customer groups.

## Features
- Data cleaning and preprocessing of banking transaction data
- Feature engineering from transaction history
- Dimensionality reduction for product ownership data using PCA
- Customer segmentation using K-Means clustering
- 2D and 3D visualizations of customer clusters

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn
- seaborn

## Dataset
The project uses a bank customer transaction dataset (`bank_customer_transactions.csv`) containing information about:
- Customer demographics (ID, gender, date of birth, location)
- Account details (balance)
- Transaction information (amount, date, time)
- Products owned by customers

## Code Structure
The code performs the following steps:

1. **Data Cleaning**
   - Fixes encoding issues in the raw data
   - Converts date and time columns to proper datetime format
   - Handles missing values

2. **Feature Engineering**
   - Transforms product ownership data using MultiLabelBinarizer and PCA
   - Encodes categorical features (gender, location)
   - Creates derived features (age, recency, frequency, transaction statistics)
   - Applies logarithmic transformation to skewed numeric features

3. **Customer Aggregation**
   - Groups transaction data by customer to create customer-level features
   - Calculates statistics per customer (mean, median, min, max for various metrics)

4. **Data Preprocessing**
   - Removes outliers using IQR method
   - Scales features using MinMaxScaler
   - Selects relevant features based on correlation analysis

5. **Clustering**
   - Applies K-Means algorithm to segment customers
   - Visualizes clusters using PCA in both 2D and 3D plots

## Usage
1. Place the raw data file (`bank_customer_transactions.csv`) in the appropriate directory
2. Run the notebook to perform the complete analysis:
   ```
   python customer_seg.ipynb
   ```
3. Review the generated visualizations and clusters

## Results
The analysis identifies 4 distinct customer segments based on:
- Account balance
- Transaction amount
- Product ownership patterns
- Demographics (age, gender)
- Location frequency
- Recency of transactions

