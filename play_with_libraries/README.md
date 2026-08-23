# Introduction to Visualization Libraries

A beginner-friendly Jupyter Notebook introducing the core Python libraries commonly used for **data analysis, numerical computing, and data visualization**.

The notebook is named `Intro_libraries.ipynb` and uses a **Python 3.10.11** kernel. It introduces Pandas and NumPy, then moves into Matplotlib, Seaborn, and Plotly, with examples based on a Superstore-style dataset.
*DATASET from KAGGLE:*https://www.kaggle.com/datasets/himanshuuike/superstore-sales-dataset?utm_source=chatgpt.com

## 📌 Overview

This notebook covers:

- Python terminology: **functions, modules, methods, libraries, and packages**
- **Pandas** for data analysis and DataFrame operations
- File paths: **absolute paths vs relative paths**
- **NumPy** for numerical and array operations
- Function parameters and arguments
- NumPy `repeat()` and the meaning of `axis`
- **Matplotlib** for visualization
- **Seaborn** installation/setup
- **Plotly** for interactive visualization
- Basic Jupyter Notebook productivity tips

## 🧰 Libraries Covered

| Library | Main Purpose | Covered In Notebook |
|---|---|---|
| **Pandas** | Data manipulation and analysis | ✅ |
| **NumPy** | Numerical and array operations | ✅ |
| **Matplotlib** | Static and customizable visualization | ✅ |
| **Seaborn** | Statistical/data visualization | Setup only |
| **Plotly** | Interactive visualization | Conceptual introduction |

## 📊 Dataset:https://www.kaggle.com/datasets/himanshuuike/superstore-sales-dataset?utm_source=chatgpt.com

The notebook loads a file named:

```text
samplesuperstore.csv
```

The dataset is loaded into a Pandas DataFrame named `super_store`.

The displayed dataset contains **10,194 rows and 21 columns**. Example columns include:

- `Row ID`
- `Order ID`
- `Order Date`
- `Ship Date`
- `Ship Mode`
- `Customer ID`
- `Customer Name`
- `Segment`
- `Country/Region`
- `City`
- `Postal Code`
- `Region`
- `Product ID`
- `Category`
- `Sub-Category`
- `Product Name`
- `Sales`
- `Quantity`
- `Discount`
- `Profit`

The notebook demonstrates how a tabular business dataset can be loaded and inspected with Pandas.

## 🐼 Pandas

Pandas is introduced as a Python library/package used for **data analysis and manipulation**.

The notebook highlights common use cases such as:

- Working with DataFrames
- Working with rows and columns
- Reading CSV files
- Working with Excel/table-like data
- Filtering
- Sorting
- Grouping
- Handling missing values
- Data cleaning

### Example

```python
import pandas as pd

super_store = pd.read_csv("samplesuperstore.csv")

print(super_store.head())
```

A simple aggregation example shown in the notebook is:

```python
print(df["marks"].mean())
```

## 📁 Absolute Path vs Relative Path

The notebook explains the difference between:

### Absolute Path

An absolute path specifies the complete location of a file.

Example:

```text
C:/...
```

This is useful when an exact file location is required.

### Relative Path

A relative path references a file relative to the current working directory.

Example:

```text
sample.csv
```

Relative paths are generally more portable when sharing projects or moving them between environments.

The notebook also demonstrates the use of a raw string for Windows paths:

```python
filepath_or_buffer = r"C:\..."
```

> Note: In Python, the `r` prefix creates a raw string; it does not mean "read the current directory."

## 🔢 NumPy

NumPy is introduced as **Numerical Python**, a library for numerical computing.

The notebook discusses:

- Array operations
- Mathematical operations
- Linear algebra
- Numerical computations
- Fast mathematical operations

Basic usage:

```python
import numpy as np
```

### `np.repeat()`

The notebook demonstrates repeating rows using:

```python
np.repeat(a=super_store, repeats=2, axis=0)
```

This produces an array with twice as many rows.

The notebook explains:

- `a` → parameter receiving the data
- `super_store` → argument/value passed to the parameter
- `repeats=2` → repeat the data two times
- `axis=0` → operate along rows
- `axis=1` → operate along columns

The resulting repeated dataset contains **20,388 rows and 21 columns**.

## 📈 Matplotlib

Matplotlib is introduced as a Python visualization library for creating:

- Line charts
- Bar charts
- Scatter plots
- Histograms
- Pie charts
- Other customizable visualizations

It is also described as supporting:

- Custom titles and labels
- Legends
- Grid lines
- Styling/customization
- Multiple output formats such as PNG, JPG, SVG, and PDF
- Jupyter Notebooks and Python scripts
- Integration with NumPy and Pandas

Import:

```python
import matplotlib.pyplot as plt
```

The notebook attempts to create a histogram using:

```python
plt.hist(super_store["Ship Date"])
```

However, that particular cell records a `NameError` because `super_store` was not defined in the active kernel state at the time the cell was executed.

## 🎨 Seaborn

The notebook installs Seaborn using:

```python
pip install seaborn
```

The recorded notebook output shows that **Seaborn 0.13.2** was successfully installed.

The notebook indicates that the difference between Matplotlib and Seaborn will be covered later, but no substantial Seaborn visualization example is included in the recorded notebook content.

## 📊 Plotly

Plotly is introduced as a library for creating **interactive, high-quality, web-based visualizations**.

The notebook highlights:

- Interactive charts
- Zooming
- Panning
- Hover tooltips
- Dynamic visualizations
- Line charts
- Bar charts
- Scatter plots
- Pie charts
- Histograms
- Heatmaps
- 3D plots
- Maps
- Integration with Dash
- Jupyter Notebook display
- HTML output
- Web application embedding

The notebook installs Plotly and records **Plotly 6.9.0** as successfully installed.

## 📝 Jupyter Notebook Tip

A shortcut note included in the notebook:

> Use `Shift + Tab` on a function to inspect what it does.
> Use `Tab` after `pd.` from view the functions,class,methods etc from the `PANDAS`
This is useful for quickly viewing function signatures and documentation while working in Jupyter.

## 🔍 Learning Outcomes

After going through this notebook, you should have a basic understanding of:

1. The difference between functions, modules, methods, libraries, and packages.
2. How to import and use Pandas.
3. How to load CSV data into a DataFrame.
4. Basic DataFrame-oriented data analysis concepts.
5. The difference between absolute and relative file paths.
6. How NumPy works with arrays.
7. How `np.repeat()` works with `axis`.
8. The role of Matplotlib in data visualization.
9. The purpose of Seaborn.
10. The purpose and interactive capabilities of Plotly.
11. How Pandas, NumPy, and visualization libraries fit together in a data-analysis workflow.

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
```

### 3. Make sure the dataset is available

Place:

```text
samplesuperstore.csv
```

in the location expected by the notebook, or update the file path in the Pandas `read_csv()` cell.

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Intro_libraries.ipynb
```

and run the cells from top to bottom.

## 📂 Suggested Repository Structure

```text
project/
│
├── Intro_libraries.ipynb
├── samplesuperstore.csv
├── README.md
└── requirements.txt
```

Suggested `requirements.txt`:

```text
pandas
numpy
matplotlib
seaborn
plotly
jupyter
```

## ⚠️ Notes

- The notebook is primarily a **learning/reference notebook**, rather than a complete end-to-end data analysis project.
- Some cells contain installation commands such as `pip install matplotlib`, `pip install seaborn`, and `pip install plotly`.
- The recorded Matplotlib histogram cell produced a `NameError` because `super_store` was unavailable in that execution state.
- Seaborn is installed, but the recorded notebook does not contain a substantial Seaborn visualization example.
- Plotly is installed and explained conceptually, but the recorded content does not show a completed Plotly chart.
- The notebook uses the file `samplesuperstore.csv`, which needs to be available when executing the data-loading cells.

## 🎯 Purpose of This Repository

This repository can serve as a **beginner's reference for Python data-analysis libraries**, especially for learning how Pandas and NumPy work together with visualization libraries such as Matplotlib, Seaborn, and Plotly.

It is also a useful starting point for progressing toward:

**Python → NumPy → Pandas → Data Cleaning → Data Analysis → Data Visualization → Exploratory Data Analysis (EDA)**

---

### Technologies

- Python 3.10+
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
