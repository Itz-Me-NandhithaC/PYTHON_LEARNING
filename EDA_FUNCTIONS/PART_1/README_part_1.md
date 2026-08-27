# 📊 Exploratory Data Analysis with Pandas — Part 1

Welcome to **Learn Functions – Part 1**! 🚀  
This Jupyter Notebook introduces the fundamentals of **Exploratory Data Analysis (EDA)** using Python and **Pandas**. The notebook uses a Superstore-style sales dataset to demonstrate how to load and inspect tabular data.

## 🗂️ Dataset

The notebook works with `samplesuperstore.csv`.

The dataset contains:

- **10,194 rows**
- **21 columns**
- Sales and order information
- Customer and geographical information
- Product and category information
- Quantity, discount, sales, and profit values

### Main Columns

| Column | Description |
|---|---|
| `Row ID` | Unique row identifier |
| `Order ID` | Order identifier |
| `Order Date` | Date the order was placed |
| `Ship Date` | Date the order was shipped |
| `Ship Mode` | Shipping method |
| `Customer ID` | Customer identifier |
| `Customer Name` | Customer name |
| `Segment` | Customer segment |
| `Country/Region` | Country or region |
| `City` | City |
| `State/Province` | State or province |
| `Postal Code` | Postal code |
| `Region` | Sales region |
| `Product ID` | Product identifier |
| `Category` | Product category |
| `Sub-Category` | Product sub-category |
| `Product Name` | Product name |
| `Sales` | Sales amount |
| `Quantity` | Quantity purchased |
| `Discount` | Discount applied |
| `Profit` | Profit amount |

## 🐼 Pandas Concepts Covered

### 1. Import Pandas and Load CSV Data

```python
import pandas as pd

store_details = pd.read_csv("samplesuperstore.csv")
```

### 2. View the First Rows

```python
store_details.head(10)
```

The notebook demonstrates how `head()` can be used to inspect the beginning of a DataFrame.

### 3. View the Last Rows

```python
store_details.tail(5)
```

`tail()` helps inspect the last records in the dataset.

### 4. Find Dataset Dimensions

```python
store_details.shape
```

Output:

```text
(10194, 21)
```

You can also separately retrieve the number of rows and columns:

```python
store_details.shape[0]  # Number of rows
store_details.shape[1]  # Number of columns
```

### 5. Display Column Names

```python
store_details.columns
```

The notebook also demonstrates looping through the columns:

```python
for column in store_details.columns:
    print(column)
```

### 6. Understand Dataset Information

```python
store_details.info()
```

`info()` provides useful information such as:

- Column names
- Non-null counts
- Data types
- Memory usage

### 7. Check Data Types

```python
store_details.dtypes
```

The notebook also shows how to inspect each column's data type:

```python
for column in store_details.columns:
    print(column, ":", store_details[column].dtype)
```

## 🔎 Data Type Overview

The dataset contains:

- `int64` columns for integer values
- `float64` columns for numerical decimal values
- `object` columns for text and currently stored date values

The notebook highlights why understanding data types is important. For example, date calculations require proper date/datetime values, while mathematical operations require numerical columns.

## 🛠️ Technologies Used

- 🐍 **Python 3.10**
- 🐼 **Pandas**
- 📓 **Jupyter Notebook**
- 📄 **CSV**

Install Pandas if required:

```bash
pip install pandas
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

## 🎯 Learning Objectives

By completing this notebook, you will learn how to:

- Load CSV data using Pandas
- Create and work with a DataFrame
- Inspect the first and last records
- Find the number of rows and columns
- Display column names
- Understand DataFrame information
- Identify column data types
- Use loops to inspect DataFrame columns
- Build a foundation for further EDA

## 🚀 What's Next?

This notebook is marked as **Part 1** and introduces the basic techniques required to explore a dataset. Future parts can continue with data cleaning, missing-value analysis, duplicate detection, date conversion, statistical summaries, filtering, grouping, and visualization.

---

### 👩‍💻 Learning Project

This repository is part of a hands-on journey into **Python, Pandas, and Data Analysis**.

> 😎 Keep learning, keep experimenting, and keep building! 🚀📊
