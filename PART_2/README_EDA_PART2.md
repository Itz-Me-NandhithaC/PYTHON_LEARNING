# 🐼 Learn Functions – Part 2

A beginner-friendly **Python Pandas practice notebook** focused on learning essential data inspection and data-cleaning functions through practical examples.

This notebook demonstrates commonly used Pandas functions for **Exploratory Data Analysis (EDA)** and basic data preprocessing.

---


The notebook uses datasets such as:

* 🛒 Sample Superstore Dataset
* 🎓 Student Details Dataset

The main goal is to learn how to **inspect, understand, clean, and summarize data using Pandas**.

---

## 🎯 Learning Objectives

By completing this notebook, you will learn how to:

* Understand the structure of a dataset
* Inspect column names and data types
* Identify numerical and categorical columns
* Generate statistical summaries
* Detect missing values
* Calculate missing-value percentages
* Handle missing values
* Detect duplicate records
* Explore unique values
* Count unique values
* Analyze frequency distributions
* Use Pandas functions in practical data-analysis workflows

---

---

# 📚 Topics Covered

## 1. 🔍 Understanding the Dataset with `info()`

The `info()` function is used to understand the basic structure of a DataFrame.

```python
store_details.info()
```

It helps identify:

* Column names
* Number of non-null values
* Data types
* Memory usage

---

## 2. 🔢 Identifying Numerical Columns

Using `select_dtypes()` to select numerical columns:

```python
numerical_col = store_details.select_dtypes(
    include=["int64", "float64"]
).columns
```

The notebook also demonstrates how to loop through and display the numerical columns.

---

## 3. 🏷️ Identifying Categorical Columns

Categorical/object columns can be selected using:

```python
categorical_col = store_details.select_dtypes(
    include=["object"]
).columns
```

This is useful for separating categorical information from numerical information during EDA.

---

# 4. 📊 Statistical Summary with `describe()`

The `describe()` function provides a statistical overview of numerical columns.

```python
store_details.describe()
```

It provides statistics such as:

| Statistic | Meaning                    |
| --------- | -------------------------- |
| `count`   | Number of available values |
| `mean`    | Average                    |
| `std`     | Standard deviation         |
| `min`     | Minimum                    |
| `25%`     | First quartile             |
| `50%`     | Median                     |
| `75%`     | Third quartile             |
| `max`     | Maximum                    |

The notebook also demonstrates using `describe()` on:

* Selected columns
* Specific data types

Example:

```python
store_details[["Product ID", "Customer ID"]].describe()
```

---

# 5. ❌ Checking Missing Values

Missing values are an important part of data cleaning.

The notebook introduces:

```python
df.isnull()
```

and:

```python
df.isnull().sum()
```

The `isnull()` function identifies missing values, while `sum()` can be used to count missing values in each column.

It also demonstrates calculating the percentage of missing values:

```python
missing_percentage = (
    df.isnull().sum() / len(df)
) * 100
```

The notebook also uses the equivalent `isna()` function:

```python
stu_details.isna().sum()
```

---

# 6. 🧹 Handling Missing Values

Several approaches to handling missing values are covered.

### Method 1 — `dropna()`

Used to remove records containing missing values.

```python
df.dropna()
```

The notebook emphasizes using this carefully because removing records can result in loss of information.

### Method 2 — Mean

Numerical missing values can be replaced with the mean:

```python
df["Sales"] = df["Sales"].fillna(
    df["Sales"].mean()
)
```

### Method 3 — Median

The median can be used when outliers are present:

```python
df["Profit"] = df["Profit"].fillna(
    df["Profit"].median()
)
```

### Method 4 — Mode

Categorical missing values can be replaced using the mode:

```python
df["Region"] = df["Region"].fillna(
    df["Region"].mode()[0]
)
```

The notebook explains why `[0]` is used: `mode()` returns the mode value(s), and `[0]` selects the first value.

### Method 5 — Custom Value

Missing categorical values can also be replaced with a custom value:

```python
df["Region"] = df["Region"].fillna("Unknown")
```

### Choosing a Method

The notebook introduces the following general approach:

* **Mean** → when values are normally distributed
* **Median** → when outliers are present
* **Mode** → for categorical values
* **Remove rows** → when missing records are very few and unimportant

---

# 7. 🔁 Checking Duplicate Records

Duplicate records can affect data analysis.

The notebook uses:

```python
df.duplicated()
```

To count duplicates:

```python
df.duplicated().sum()
```

The notebook also demonstrates checking the dataset after duplicate-related processing.

---

# 8. 🔢 Unique Values

The notebook introduces two important functions:

### `nunique()`

Returns the number of unique values.

```python
df["Category"].nunique()
```

### `unique()`

Returns the actual unique values.

```python
df["Category"].unique()
```

The notebook demonstrates these functions on individual columns and explores unique values across the student dataset.

It also demonstrates looping through all columns:

```python
for col in stu_details.columns:
    print(stu_details[col].unique())
```

and displaying both:

* Actual unique values
* Number of unique values

---

# 9. 📈 Frequency Distribution with `value_counts()`

The `value_counts()` function shows how frequently each value occurs.

Example:

```python
df["Category"].value_counts()
```

The notebook demonstrates frequency analysis using the student dataset:

```python
stu_details["Name"].value_counts()
```

It also connects frequency distribution with:

```python
nunique()
```

and:

```python
unique()
```

This helps understand how values are distributed within a column.

---

---

# 💻 Example Workflow

A basic Pandas EDA workflow from this notebook can be summarized as:

```python
import pandas as pd

df = pd.read_csv("dataset.csv")

# Understand dataset
df.info()

# Numerical columns
numerical_col = df.select_dtypes(
    include=["int64", "float64"]
).columns

# Categorical columns
categorical_col = df.select_dtypes(
    include=["object"]
).columns

# Statistical summary
df.describe()

# Missing values
df.isnull().sum()

# Missing percentage
missing_percentage = (
    df.isna().sum() / len(df)
) * 100

# Duplicate records
df.duplicated().sum()

# Unique values
df["Column"].unique()

# Number of unique values
df["Column"].nunique()

# Frequency distribution
df["Column"].value_counts()
```

---

# 📁 Files

```text
📦 Learn_Functions_Part2
 ├── 📓 Learn_Functions_part2.ipynb
 ├── 📄 samplesuperstore.csv
 └── 📄 students_.csv
```
---

# 🚀 Key Takeaways

Through this notebook, I practiced the fundamental Pandas functions required for the early stages of data analysis:

```text
info()
select_dtypes()
describe()
isnull()
isna()
sum()
fillna()
dropna()
mean()
median()
mode()
duplicated()
nunique()
unique()
value_counts()
```

These functions form an important foundation for **Exploratory Data Analysis and Data Cleaning** in Python.

---

## 🌱 Learning Journey

This notebook is part of my journey to build practical skills in **Python, Pandas, Data Analysis, and Exploratory Data Analysis**.

> **Be Confident 😎
> Be Consistent ⏩
> Be For Yourself 🔎
> Be Happy 😊**

---

---

### 📌 Project Status

**Status:** 🟢 Learning / Practice

**Level:** Beginner

**Focus:** Python Pandas & Exploratory Data Analysis
