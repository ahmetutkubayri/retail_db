# Retail Data Analysis with PySpark

This project aims to solve several business needs using retail data from multiple CSV files, available in the [dataset repository](https://github.com/erkansirin78/datasets/tree/master/retail_db). The analysis leverages Spark DataFrames to efficiently process data and extract insights relevant to sales trends, order cancellations, and customer purchasing patterns.

## Objectives

1. **Count Distinct Orders**: Calculate the unique `orderItemOrderId` values in the `order_items` table to determine the total number of distinct orders.
2. **Row Counts**: Retrieve the row counts for both `orders` and `order_items` tables to understand the size and structure of the data.
3. **Top Canceled Products**: Identify the most frequently canceled products based on total sales amount and save the results in Parquet format.
4. **Top Canceled Categories**: Identify the most frequently canceled product categories by total sales amount and save the results in Parquet format.
5. **Peak Sales Month and Year**: Find the month and year with the highest total sales to determine peak sales periods.
6. **Peak Sales Day of the Week**: Determine the day of the week with the highest sales, providing insight into customer purchasing patterns.
7. **Comprehensive Retail Table**: Join all datasets to create a large unified dataset (`retail_all`) and store it in a PostgreSQL database, facilitating deeper analysis.

## Dataset Descriptions

- **orders.csv**: Contains customer orders, including order details and statuses (e.g., canceled, pending payment).
- **order_items.csv**: Provides item-level details for each order, including product IDs and prices.
- **products.csv**: Lists products available in the store, including descriptions and prices.
- **customers.csv**: Contains customer data, such as names and addresses.
- **categories.csv**: Contains categories for each product.
- **departments.csv**: Includes department data for organizing product categories.

## Requirements

- **Python** and **PySpark**: Required for data processing in this notebook.
- **PostgreSQL**: The `retail_all` table will be stored in a PostgreSQL database named `test1` for easy access and further analysis.
- **Parquet**: The output for canceled products and categories is saved in Parquet format, which provides efficient storage and quick access.

## Project Structure

1. **Data Loading**: Reads CSV files into PySpark DataFrames and explores the dataset.
2. **Data Processing and Analysis**: 
   - Counts distinct orders and retrieves row counts for key tables.
   - Identifies the most canceled products and categories based on total sales value.
   - Analyzes monthly and daily sales patterns.
3. **Data Storage**: Saves analytical results in Parquet format and stores the final `retail_all` table in a PostgreSQL database.

## How to Run

1. Clone this repository.
2. Ensure Python, PySpark, and PostgreSQL are installed and configured.
3. Place all data files (`orders.csv`, `order_items.csv`, etc.) in the specified directory.
4. Run the Jupyter notebook to execute the analysis and save results.

## Conclusion

This project provides valuable insights into retail data:
- **Order and Sales Analysis**: Gained insights into transaction volumes, frequently canceled products, and categories.
- **Sales Trends**: Analyzed peak sales periods by month, year, and day of the week.
- **Unified Data Table**: Created a consolidated dataset in PostgreSQL for deeper, relational analysis.

These findings help retailers optimize inventory, improve customer satisfaction, and identify key sales trends.
