# 📊 The Basics of NumPy & Arithmetic Universal Functions (ufuncs)

<p align="center">
  <img src="https://img.shields.io/badge/Python-NumPy-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Module-Data%20Analysis-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=for-the-badge" />
</p>

---

# 🎯 Learning Objectives

এই অধ্যায় শেষে আপনি জানতে পারবেন—

* NumPy কী এবং কেন ব্যবহার করা হয়
* NumPy Array কী
* Python List vs NumPy Array
* Array Creation Techniques
* Array Attributes
* Indexing & Slicing
* Vectorization
* Universal Functions (ufuncs)
* Arithmetic Operations
* Real World Data Analysis Examples

---

# 📚 Table of Contents

1. Introduction to NumPy
2. Why NumPy?
3. Creating Arrays
4. Array Dimensions
5. Array Attributes
6. Indexing & Slicing
7. Special Array Creation Functions
8. Vectorization
9. Universal Functions (ufuncs)
10. Arithmetic Operations
11. Real World Examples
12. Interview Questions
13. Summary

---

# 📖 What is NumPy?

**NumPy (Numerical Python)** হলো Python-এর সবচেয়ে জনপ্রিয় Numerical Computing Library।

এটি ব্যবহার করা হয়—

* Data Science
* Data Analysis
* Machine Learning
* Artificial Intelligence
* Scientific Computing
* Statistics

এবং অন্যান্য Mathematical Computation-এর জন্য।

---

# 🤔 Why NumPy?

Python List দিয়ে Numerical Computation করা সম্ভব হলেও বড় Dataset-এর ক্ষেত্রে NumPy অনেক বেশি Fast এবং Memory Efficient।

## Python List

```python
numbers = [1, 2, 3, 4, 5]
```

## NumPy Array

```python
import numpy as np

numbers = np.array([1, 2, 3, 4, 5])
```

---

# 📦 Installation

```bash
pip install numpy
```

Import:

```python
import numpy as np
```

---

# 🔹 Creating Arrays

## From List

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

print(arr)
```

Output:

```python
[1 2 3 4 5]
```

---

# 📏 Array Dimensions

## 1D Array

```python
arr = np.array([1, 2, 3])
```

---

## 2D Array

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6]
])
```

---

## 3D Array

```python
arr = np.array([
    [
        [1, 2],
        [3, 4]
    ],
    [
        [5, 6],
        [7, 8]
    ]
])
```

---

# 📊 Array Attributes

## ndim

Dimension Count

```python
print(arr.ndim)
```

---

## shape

Rows এবং Columns

```python
print(arr.shape)
```

---

## size

Total Elements

```python
print(arr.size)
```

---

## dtype

Data Type

```python
print(arr.dtype)
```

---

# 🔍 Indexing

```python
arr = np.array([10, 20, 30, 40])

print(arr[0])
```

Output:

```python
10
```

---

## Negative Indexing

```python
print(arr[-1])
```

Output:

```python
40
```

---

# 🔪 Slicing

```python
arr = np.array([10, 20, 30, 40, 50])

print(arr[1:4])
```

Output:

```python
[20 30 40]
```

---

# 🏗 Special Array Creation Functions

## zeros()

```python
np.zeros((3,3))
```

---

## ones()

```python
np.ones((2,2))
```

---

## full()

```python
np.full((2,3), 7)
```

---

## arange()

```python
np.arange(1,11)
```

Output:

```python
[1 2 3 4 5 6 7 8 9 10]
```

---

## linspace()

```python
np.linspace(0,10,5)
```

Output:

```python
[0. 2.5 5. 7.5 10.]
```

---

# ⚡ Vectorization

NumPy-এর সবচেয়ে শক্তিশালী Feature।

## Traditional Python

```python
numbers = [1,2,3,4]

result = []

for n in numbers:
    result.append(n * 2)
```

---

## NumPy

```python
arr = np.array([1,2,3,4])

result = arr * 2

print(result)
```

Output:

```python
[2 4 6 8]
```

---

# 🔥 Universal Functions (ufuncs)

Universal Functions হলো এমন Functions যা Array-এর প্রতিটি Element-এর উপর Automatically Apply হয়।

---

# ➕ Addition

```python
arr = np.array([1,2,3])

print(arr + 10)
```

Output:

```python
[11 12 13]
```

---

# ➖ Subtraction

```python
print(arr - 2)
```

Output:

```python
[-1 0 1]
```

---

# ✖ Multiplication

```python
print(arr * 3)
```

Output:

```python
[3 6 9]
```

---

# ➗ Division

```python
print(arr / 2)
```

Output:

```python
[0.5 1.0 1.5]
```

---

# 🔢 Power

```python
print(arr ** 2)
```

Output:

```python
[1 4 9]
```

---

# 🔄 Modulus

```python
print(arr % 2)
```

Output:

```python
[1 0 1]
```

---

# 📐 Square Root

```python
np.sqrt([4,9,16])
```

Output:

```python
[2. 3. 4.]
```

---

# 📈 Exponential

```python
np.exp([1,2,3])
```

---

# 📊 Logarithm

```python
np.log([1,10,100])
```

---

# 📐 Trigonometric Functions

```python
np.sin(arr)

np.cos(arr)

np.tan(arr)
```

---

# 🔄 Array-to-Array Operations

```python
a = np.array([1,2,3])

b = np.array([4,5,6])
```

Addition:

```python
a + b
```

Output:

```python
[5 7 9]
```

---

Multiplication:

```python
a * b
```

Output:

```python
[ 4 10 18 ]
```

---

Division:

```python
a / b
```

Output:

```python
[0.25 0.4 0.5]
```

---

# 🎯 Real World Example

## GPA Analysis

```python
import numpy as np

gpa = np.array([
    3.0,
    3.2,
    3.5,
    3.8,
    4.0
])

new_gpa = gpa + 0.2

print(new_gpa)
```

Output:

```python
[3.2 3.4 3.7 4.0 4.2]
```

---

# 📈 Sales Analysis

```python
sales = np.array([
    1000,
    1200,
    1500,
    1800
])

sales_with_vat = sales * 1.15

print(sales_with_vat)
```

Output:

```python
[1150 1380 1725 2070]
```

---

# 💼 Interview Questions

### 1. What is NumPy?

NumPy হলো Python-এর Numerical Computing Library।

---

### 2. What is ndarray?

NumPy-এর Core N-Dimensional Array Object।

---

### 3. Why is NumPy faster than Python Lists?

কারণ NumPy Vectorized Operations এবং Optimized C Implementation ব্যবহার করে।

---

### 4. What is Vectorization?

Loop ছাড়াই পুরো Array-এর উপর Operation চালানো।

---

### 5. What is a Universal Function (ufunc)?

এমন Function যা Array-এর প্রতিটি Element-এর উপর Automatically Apply হয়।

---

# 📋 Summary

| Concept       | Description              |
| ------------- | ------------------------ |
| NumPy         | Numerical Python Library |
| ndarray       | N-Dimensional Array      |
| ndim          | Number of Dimensions     |
| shape         | Array Shape              |
| size          | Total Elements           |
| dtype         | Data Type                |
| Vectorization | Loop-free Operations     |
| ufunc         | Universal Functions      |
| zeros()       | Zero Array               |
| ones()        | One Array                |
| arange()      | Range Array              |
| linspace()    | Evenly Spaced Numbers    |

---

# 🎯 Key Takeaways

✅ NumPy হলো Data Science এবং AI-এর Foundation Library।

✅ ndarray হলো NumPy-এর Core Data Structure।

✅ Vectorization NumPy-এর অন্যতম Powerful Feature।

✅ Universal Functions (ufuncs) Mathematical Operations সহজ এবং দ্রুত করে।

✅ NumPy Python List-এর তুলনায় Faster এবং Memory Efficient।

---

# 🚀 Next Topic

## NumPy Arrays, Indexing, Slicing, Reshaping & Broadcasting

* Fancy Indexing
* Boolean Masking
* Reshape
* Flatten
* Broadcasting
* Aggregation Functions
* Statistical Operations

⭐ Happy Learning NumPy! 🐍📊
