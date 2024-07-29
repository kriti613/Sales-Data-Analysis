# Sales Data Analysis

## Overview

This project involves analyzing a sales dataset to extract meaningful insights and trends. The analysis covers various aspects, including identifying the best month for sales, the city with the maximum orders, the most sold product, understanding trends, and identifying products often sold together.

## Packages Used

The following Python packages were used for this analysis:

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical computations.
- `matplotlib`: For creating static, animated, and interactive visualizations.
- `seaborn`: For statistical data visualization.
- `pyarrow`: To enable the use of the Feather file format.

## Feather Data Format

Feather is a fast, lightweight, and easy-to-use binary columnar data storage format for use in data frames. It is designed to make reading and writing data frames efficient and fast, leveraging Apache Arrow to provide a standardized language-independent columnar memory format.

### How to Read Feather Data

To read data from a Feather file, you can use the `read_feather` function from the `pandas` library:

```python
import pandas as pd

# Read data from a Feather file
df = pd.read_feather('my_ftr_file_path.ftr')
```

## Data Cleaning

The dataset underwent several cleaning steps to ensure the integrity and quality of the data:

1. **Dropping Null Rows**: All rows with null values were dropped using `how='all'` to ensure we only remove rows where all columns are null.

    ```python
    df.dropna(how='all', inplace=True)
    ```

2. **Checking for Duplicates**: Duplicate entries were identified and removed to avoid redundant data points.

    ```python
    df.drop_duplicates(inplace=True)
    ```

## Analysis

### 1. Which is the Best Month for Sales?

This analysis identifies the month with the highest sales by aggregating the total sales per month and comparing the results.

### 2. Which City has the Maximum Orders?

This analysis determines which city has the highest number of orders by grouping the data by city and counting the number of orders.

### 3. What Product Sold the Most and Why?

This analysis identifies the most sold product and explores the reasons behind its popularity, considering factors such as price, demand, and any seasonal trends.

### 4. Understanding Trend of the Most Sold Product

This analysis investigates the sales trend of the most sold product over time, looking for patterns and changes in demand.

### 5. What Products are Most Often Sold Together?

This analysis examines the dataset to find combinations of products that are frequently purchased together, helping to identify potential bundling opportunities.


## Results

The results of the analysis provide valuable insights into sales patterns and trends, helping to inform business decisions and strategies. Key findings include the best month for sales, the city with the maximum orders, the most popular products, and products that are often sold together.
