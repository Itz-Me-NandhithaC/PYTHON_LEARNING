# 🐍 Python Data Structures

A beginner-friendly Jupyter Notebook covering the fundamental **Python data structures**: Lists, Sets, Tuples, and Dictionaries. The notebook demonstrates how to create, access, modify, and use these structures with simple Python examples.

## 📌 Topics Covered

The notebook focuses on four major Python data structures:

1. 📋 **List**
2. 🔹 **Set**
3. 📦 **Tuple**
4. 🗂️ **Dictionary**

It also includes a practical example of converting a dictionary into a **Pandas DataFrame**.

---

## 📋 1. List

Lists are used to store multiple values in an organized structure.

### Key Characteristics
- One-dimensional
- Heterogeneous — can contain different data types
- Allows duplicate values
- Mutable
- Supports multiple elements
- Supports indexing, negative indexing, and slicing

### Examples Covered
- Creating a list
- Checking the data type
- Accessing elements using positive indexing
- Accessing elements using negative indexing
- List slicing
- Updating list elements
- Understanding mutability

### List Methods Demonstrated
| Method | Purpose |
|---|---|
| `append()` | Adds an element to the end |
| `clear()` | Removes all elements |
| `copy()` | Creates a copy of the list |
| `count()` | Counts occurrences of a value |
| `extend()` | Adds elements from another iterable |
| `index()` | Returns the index of a value |
| `insert()` | Inserts an element at a specific position |
| `pop()` | Removes an element by position |
| `remove()` | Removes the first matching value |
| `reverse()` | Reverses the list |
| `sort()` | Sorts the list |

---

## 🔹 2. Set

Sets are collections that store **unique values**.

### Key Characteristics
- One-dimensional
- Heterogeneous
- Does not allow duplicate values
- Mutable
- Does not support positional indexing or slicing

### Operations Covered
- Creating an empty set
- Checking the type of a set
- Creating a set with different data types
- Understanding why positional updating is not supported
- Adding elements using `add()`
- Removing elements using `discard()`

---

## 📦 3. Tuple

Tuples are ordered collections that are **immutable**.

### Key Characteristics
- One-dimensional
- Heterogeneous
- Allows duplicate values
- Immutable
- Supports indexing
- Supports slicing

### Examples Covered
- Creating a tuple
- Checking the tuple type
- Accessing tuple elements
- Tuple slicing
- Understanding tuple immutability

---

## 🗂️ 4. Dictionary

Dictionaries store data as **key-value pairs**.

### Key Characteristics
- Stores data in `key:value` pairs
- Keys should be unique
- Values can be duplicated
- Mutable
- Does not support positional indexing or slicing

### Examples Covered
- Creating an empty dictionary
- Checking the dictionary type
- Creating dictionaries with different values
- Accessing dictionary keys and values
- Using `keys()`
- Using `values()`
- Clearing dictionary contents with `clear()`
- Understanding dictionary mutability

---

## 📊 Dictionary to Pandas DataFrame

The notebook also demonstrates how dictionaries can be used to create Pandas DataFrames.

### ❌ Single-value dictionary

A dictionary such as:

```python
c_dict = {"anu": 5, "banu": 3, "subz": 7}
```

does not directly provide multiple rows for a DataFrame.

### ✅ Dictionary with lists

The notebook then uses lists as dictionary values:

```python
student_mark = {
    "Student": ["Nandhitha", "Ria", "Yathra"],
    "Maths": [68, 85, 95],
    "Computer": [100, 100, 100],
    "Tamil": [85, 85, 86]
}
```

This structure can be converted into a Pandas DataFrame:

```python
import pandas as pd

pd.DataFrame(data=student_mark)
```

This demonstrates an important practical connection between **Python dictionaries and tabular data analysis with Pandas**.

---

## 🛠️ Technologies Used

- 🐍 Python
- 📓 Jupyter Notebook
- 🐼 Pandas

---

## 📁 Project Structure

```text
Python-Data-Structures/
│
├── Python Data Structure(2).ipynb
└── README.md
```

---

## 🎯 Learning Objectives

By working through this notebook, you can understand:

- The difference between Python's major built-in data structures
- Mutable vs. immutable data structures
- Indexing and negative indexing
- Slicing
- Handling duplicate values
- Basic methods used with Lists and Sets
- Key-value pairs in Dictionaries
- How dictionaries can be structured for DataFrame creation
- Basic use of Pandas for tabular data

---

## 🚀 How to Run

1. Install Python.
2. Install Jupyter Notebook or use JupyterLab/Google Colab.
3. Open `Python Data Structure(2).ipynb`.
4. Run the cells sequentially to explore the examples.

If Pandas is not installed, run:

```bash
pip install pandas
```

---

## 📚 Conclusion

This notebook provides a simple introduction to Python data structures through hands-on examples. It covers the basic properties and operations of **Lists, Sets, Tuples, and Dictionaries**, followed by a practical example of using dictionaries with **Pandas DataFrames**.

⭐ A useful beginner project for building a strong foundation in Python and preparing for further learning in **Data Analysis and Data Science**.
