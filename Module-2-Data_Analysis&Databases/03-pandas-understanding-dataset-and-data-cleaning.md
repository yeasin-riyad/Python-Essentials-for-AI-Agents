# 🐼 Pandas: Understanding the Dataset, Handling Missing Values & Modifying Dataset

<p align="center">
  <img src="https://img.shields.io/badge/Python-Pandas-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Data%20Analysis-Essential-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=for-the-badge" />
</p>

---

# 🎯 Learning Objectives

এই অধ্যায় শেষে আপনি জানতে পারবেন—

* Pandas কী
* Dataset কী
* DataFrame কী
* Dataset Load করা
* Dataset Explore করা
* Dataset Summary দেখা
* Missing Values কী
* Missing Values Detect করা
* Missing Values Handle করা
* Row ও Column Modify করা
* Rename করা
* Add/Delete Column
* Update Values
* Data Cleaning Techniques

---

# 📚 Table of Contents

1. Introduction to Pandas
2. Understanding Dataset
3. Loading Dataset
4. Exploring Dataset
5. Selecting Data
6. Missing Values
7. Handling Missing Values
8. Modifying Dataset
9. Filtering & Sorting
10. Real World Example
11. Data Cleaning Workflow
12. Interview Questions
13. Summary

---

# 📖 What is Pandas?

**Pandas** হলো Python-এর সবচেয়ে জনপ্রিয় Data Analysis এবং Data Manipulation Library।

এটি ব্যবহার করে—

* CSV File Analysis
* Excel File Processing
* Data Cleaning
* Data Transformation
* Data Analysis
* Machine Learning Data Preparation

করা হয়।

---

# 🤔 What is a Dataset?

Dataset হলো Structured Data-এর Collection।

উদাহরণ:

| Student ID | Name  | Department | GPA  |
| ---------- | ----- | ---------- | ---- |
| 101        | Rahim | CSE        | 3.75 |
| 102        | Karim | EEE        | 3.50 |
| 103        | Sakib | CSE        | 3.90 |

এটি একটি Dataset।

---

# 📦 Installation

```bash
pip install pandas
```

Import:

```python
import pandas as pd
```

---

# 📁 Loading Dataset

CSV File Load করা:

```python
import pandas as pd

df = pd.read_csv("students.csv")
```

---

# 👀 Viewing Dataset

## First 5 Rows

```python
df.head()
```

---

## Last 5 Rows

```python
df.tail()
```

---

# 📊 Understanding the Dataset

## Shape

Dataset-এ কত Rows এবং Columns আছে তা দেখায়।

```python
df.shape
```

Example Output:

```python
(1000, 5)
```

Meaning:

* 1000 Rows
* 5 Columns

---

## Column Names

```python
df.columns
```

---

## Data Types

```python
df.dtypes
```

Example:

```python
student_id     int64
name          object
department    object
gpa          float64
```

---

## Dataset Information

```python
df.info()
```

এটি দেখায়:

* Total Rows
* Total Columns
* Data Types
* Missing Values

---

## Statistical Summary

```python
df.describe()
```

Output:

```text
count
mean
std
min
25%
50%
75%
max
```

---

# 🔍 Selecting Data

## Single Column

```python
df["name"]
```

---

## Multiple Columns

```python
df[["name", "gpa"]]
```

---

## Select First Row

```python
df.iloc[0]
```

---

## Select First Five Rows

```python
df.iloc[0:5]
```

---

# ⚠ Understanding Missing Values

Dataset-এ কোনো Value অনুপস্থিত থাকলে তাকে Missing Value বলে।

Example:

| Name  | GPA  |
| ----- | ---- |
| Rahim | 3.75 |
| Karim | NaN  |
| Sakib | 3.90 |

এখানে Karim-এর GPA Missing।

---

# 🔎 Detecting Missing Values

## isnull()

```python
df.isnull()
```

---

## Count Missing Values

```python
df.isnull().sum()
```

Example Output:

```python
name          0
department    2
gpa           5
```

Meaning:

* department → 2 Missing Values
* gpa → 5 Missing Values

---

## notnull()

```python
df.notnull()
```

---

## Missing Value Percentage

```python
(df.isnull().sum() / len(df)) * 100
```

---

# 🗑 Removing Missing Values

## Remove Rows with Missing Values

```python
df.dropna()
```

---

## Remove Columns with Missing Values

```python
df.dropna(axis=1)
```

---

# 🎯 Filling Missing Values

## Fill with Zero

```python
df.fillna(0)
```

---

## Fill with Mean

```python
df["gpa"].fillna(
    df["gpa"].mean()
)
```

---

## Fill with Median

```python
df["salary"].fillna(
    df["salary"].median()
)
```

---

## Fill with Mode

```python
df["department"].fillna(
    df["department"].mode()[0]
)
```

---

## Forward Fill

```python
df.fillna(method="ffill")
```

Example:

```text
100
NaN
NaN
200
```

After:

```text
100
100
100
200
```

---

## Backward Fill

```python
df.fillna(method="bfill")
```

---

# ✏ Modifying Dataset

## Rename Column

```python
df.rename(
    columns={
        "gpa": "cgpa"
    }
)
```

---

## Add New Column

```python
df["country"] = "Bangladesh"
```

---

## Add Calculated Column

```python
df["bonus"] = (
    df["salary"] * 0.10
)
```

---

## Update Existing Column

```python
df["salary"] = (
    df["salary"] * 1.20
)
```

---

## Update Specific Cell

```python
df.loc[
    0,
    "name"
] = "Yeasin"
```

---

## Delete Column

```python
df.drop(
    "bonus",
    axis=1
)
```

---

## Delete Multiple Columns

```python
df.drop(
    [
        "bonus",
        "country"
    ],
    axis=1
)
```

---

## Delete Row

```python
df.drop(0)
```

---

# 🔍 Filtering Data

## CSE Students

```python
df[
    df["department"] == "CSE"
]
```

---

## GPA Greater Than 3.5

```python
df[
    df["gpa"] > 3.5
]
```

---

## Multiple Conditions

```python
df[
    (df["department"] == "CSE")
    &
    (df["gpa"] > 3.5)
]
```

---

# 📈 Sorting Data

## Ascending Order

```python
df.sort_values(
    by="gpa"
)
```

---

## Descending Order

```python
df.sort_values(
    by="gpa",
    ascending=False
)
```

---

# 🌍 Real World Example

```python
import pandas as pd

df = pd.read_csv(
    "employees.csv"
)

# Check Missing Values
print(
    df.isnull().sum()
)

# Fill Missing Salary
df["salary"] = (
    df["salary"]
    .fillna(
        df["salary"].mean()
    )
)

# Add Bonus Column
df["bonus"] = (
    df["salary"] * 0.10
)

# Rename Column
df.rename(
    columns={
        "salary":
        "monthly_salary"
    }
)
```

---

# 🧹 Typical Data Cleaning Workflow

```text
Load Dataset
      ↓
Inspect Dataset
      ↓
Check Missing Values
      ↓
Handle Missing Values
      ↓
Remove Duplicates
      ↓
Rename Columns
      ↓
Convert Data Types
      ↓
Feature Engineering
      ↓
Ready for Analysis
```

---

# 💼 Interview Questions

### 1. What is Pandas?

Python-এর Data Analysis Library।

---

### 2. What is a DataFrame?

Pandas-এর Tabular Data Structure।

---

### 3. How to Detect Missing Values?

```python
df.isnull()
```

---

### 4. How to Count Missing Values?

```python
df.isnull().sum()
```

---

### 5. How to Fill Missing Values?

```python
df.fillna()
```

---

### 6. How to Delete Rows or Columns?

```python
df.drop()
```

---

### 7. How to View Dataset Summary?

```python
df.describe()
```

---

### 8. How to View Dataset Information?

```python
df.info()
```

---

# 📋 Summary

| Function      | Purpose               |
| ------------- | --------------------- |
| read_csv()    | Load Dataset          |
| head()        | First Rows            |
| tail()        | Last Rows             |
| shape         | Dataset Size          |
| columns       | Column Names          |
| info()        | Dataset Information   |
| describe()    | Statistical Summary   |
| isnull()      | Detect Missing Values |
| fillna()      | Fill Missing Values   |
| dropna()      | Remove Missing Values |
| rename()      | Rename Columns        |
| drop()        | Delete Rows/Columns   |
| sort_values() | Sorting               |
| loc           | Update Values         |
| iloc          | Row Selection         |

---

# 🎯 Key Takeaways

✅ Pandas হলো Data Analysis-এর সবচেয়ে গুরুত্বপূর্ণ Library।

✅ Dataset বুঝতে `shape`, `info()` এবং `describe()` অত্যন্ত গুরুত্বপূর্ণ।

✅ Missing Values হলো Real World Dataset-এর সবচেয়ে Common Problem।

✅ `fillna()` এবং `dropna()` ব্যবহার করে Missing Values Handle করা যায়।

✅ `rename()`, `drop()`, `loc()` এবং নতুন Column Creation Data Manipulation-এর জন্য অত্যন্ত গুরুত্বপূর্ণ।

✅ Data Cleaning Machine Learning Pipeline-এর অন্যতম গুরুত্বপূর্ণ ধাপ।

---

# 🚀 Next Topic

## 📊 Pandas GroupBy, Aggregation & Data Analysis

পরবর্তী অধ্যায়ে শিখবো—

* GroupBy
* Aggregation Functions
* Value Counts
* Pivot Tables
* Merge & Join
* Combining Datasets
* Advanced Data Analysis

⭐ Happy Learning Pandas! 🐼📊🚀
