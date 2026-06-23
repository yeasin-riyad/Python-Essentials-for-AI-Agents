# 🐍 Python Variables & Data Types (বাংলা)

<p align="center">
  <img src="https://img.shields.io/badge/Python-Variables%20%26%20Data%20Types-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Level-Beginner-success?style=for-the-badge" alt="Level">
  <img src="https://img.shields.io/badge/Language-Bangla-red?style=for-the-badge" alt="Language">
</p>

> **এই নোটে যা শিখবেন**
>
> * Variable কী?
> * Data Type কী?
> * Dynamic Typing
> * Python-এর Built-in Data Types
> * Type Conversion
> * Real-world Examples
> * Interview Questions

---

# 📚 Table of Contents

* [Variable কী?](#-variable-কী)
* [Dynamic Typing](#-dynamic-typing)
* [Variable Naming Rules](#-variable-naming-rules)
* [Multiple Assignment](#-multiple-assignment)
* [Python Data Types](#-python-data-types)
* [Type Conversion](#-type-conversion)
* [Real World Example](#-real-world-example)
* [Interview Questions](#-interview-questions)
* [Summary](#-summary)

---

# 📦 Variable কী?

Variable হলো একটি **named container** যেখানে আমরা data সংরক্ষণ করি।

সহজভাবে,

> **Variable = একটি Box যার একটি নাম আছে এবং যার ভিতরে Data রাখা হয়।**

## Example

```python
name = "Yeasin"
age = 25
```

এখানে,

| Variable | Value      |
| -------- | ---------- |
| `name`   | `"Yeasin"` |
| `age`    | `25`       |

---

# 🌍 Real Life Example

ধরুন আপনার একটি আলমারি আছে।

| Label | Value  |
| ----- | ------ |
| Name  | Yeasin |
| Age   | 25     |
| City  | Dhaka  |

Python এ,

```python
name = "Yeasin"
age = 25
city = "Dhaka"
```

---

# ⚡ Dynamic Typing

Python একটি **Dynamically Typed Language**।

অর্থাৎ Variable তৈরি করার সময় Data Type লিখতে হয় না।

```python
x = 100

print(type(x))
```

Output

```text
<class 'int'>
```

একই Variable পরে অন্য Type ধারণ করতে পারে।

```python
x = 100

x = "Python"

x = 3.14
```

সবগুলোই Valid।

---

# ✍️ Variable Naming Rules

## ✅ Valid

```python
student_name = "Rahim"

user123 = "Admin"

_total = 100
```

---

## ❌ Invalid

```python
1name = "Rahim"

student-name = "Rahim"

class = "Python"
```

কারণ

* সংখ্যা দিয়ে শুরু করা যাবে না
* Hyphen ব্যবহার করা যাবে না
* Reserved Keyword ব্যবহার করা যাবে না

---

# 🔑 Multiple Assignment

## এক লাইনে একাধিক Variable

```python
x, y, z = 10, 20, 30

print(x)
print(y)
print(z)
```

---

## একই Value একাধিক Variable এ

```python
a = b = c = 100

print(a)
print(b)
print(c)
```

---

# 🔄 Swapping Variables

Python-এর অন্যতম সুন্দর Feature।

```python
x = 10
y = 20

x, y = y, x

print(x)
print(y)
```

Output

```text
20
10
```

---

# 🏷️ Python Data Types

Python-এর প্রধান Built-in Data Types হলো:

| Data Type | Example             |
| --------- | ------------------- |
| int       | `100`               |
| float     | `3.14`              |
| str       | `"Python"`          |
| bool      | `True`              |
| list      | `[1,2,3]`           |
| tuple     | `(1,2,3)`           |
| set       | `{1,2,3}`           |
| dict      | `{"name":"Yeasin"}` |
| NoneType  | `None`              |

---

# 🔢 Integer (int)

পূর্ণ সংখ্যা সংরক্ষণ করতে ব্যবহৃত হয়।

```python
age = 25

temperature = -5

salary = 50000
```

---

# 🔹 Float

Decimal Number সংরক্ষণ করে।

```python
price = 99.99

pi = 3.1416
```

---

# 🔤 String (str)

Text Data সংরক্ষণ করতে ব্যবহৃত হয়।

```python
name = "Python"

language = 'Bangla'
```

## String Index

```python
word = "Python"

print(word[0])
print(word[-1])
```

Output

```text
P
n
```

---

# 🔗 String Concatenation

```python
first = "Hello"
second = "World"

print(first + " " + second)
```

Output

```text
Hello World
```

---

# 🔁 String Repetition

```python
print("Hi " * 3)
```

Output

```text
Hi Hi Hi
```

---

# ✅ Boolean (bool)

Boolean-এর মাত্র দুইটি Value আছে।

```python
True

False
```

Example

```python
is_admin = False

is_logged_in = True
```

Comparison

```python
print(10 > 5)

print(10 < 5)
```

Output

```text
True

False
```

---

# 📋 List

Ordered এবং Mutable Collection।

```python
fruits = ["Apple", "Banana", "Orange"]
```

Access

```python
print(fruits[0])
```

Output

```text
Apple
```

Add Item

```python
fruits.append("Mango")
```

---

# 📦 Tuple

Ordered কিন্তু Immutable Collection।

```python
colors = ("Red", "Green", "Blue")
```

```python
print(colors[1])
```

Output

```text
Green
```

---

# 🎯 Set

Unique Value Store করে।

Duplicate Automatically Remove করে।

```python
numbers = {1, 2, 3, 2, 1}

print(numbers)
```

Output

```text
{1, 2, 3}
```

---

# 🗂 Dictionary

Key এবং Value Pair আকারে Data Store করে।

```python
student = {
    "name": "Yeasin",
    "age": 25,
    "city": "Dhaka"
}
```

Access

```python
print(student["name"])
```

Output

```text
Yeasin
```

---

# 🚫 NoneType

যখন কোনো Value নেই তখন None ব্যবহার করা হয়।

```python
result = None

print(result)
```

Output

```text
None
```

---

# 🔄 Type Conversion

## Integer → Float

```python
age = 25

print(float(age))
```

Output

```text
25.0
```

---

## Float → Integer

```python
price = 99.99

print(int(price))
```

Output

```text
99
```

---

## Integer → String

```python
age = 25

print(str(age))
```

Output

```text
'25'
```

---

## String → Integer

```python
number = "100"

print(int(number))
```

Output

```text
100
```

---

# 🔍 type() Function

Variable-এর Data Type জানার জন্য ব্যবহার করা হয়।

```python
name = "Python"
age = 25
price = 99.99
active = True

print(type(name))
print(type(age))
print(type(price))
print(type(active))
```

Output

```text
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

---

# 🎓 Real World Example

একটি Student Information System

```python
student_name = "Yeasin Mazumder"
student_age = 24
student_gpa = 3.85
is_graduated = False

courses = [
    "Python",
    "Database",
    "AI"
]

student = {
    "name": student_name,
    "age": student_age,
    "gpa": student_gpa,
    "graduated": is_graduated,
    "courses": courses
}

print(student)
```

---

# 💼 Interview Questions

## ১. Variable কী?

Memory-তে Data সংরক্ষণের জন্য একটি Named Reference।

---

## ২. Python Dynamic Typing কী?

Python Variable-এর Data Type Runtime-এ Automatically নির্ধারণ করে।

---

## ৩. Mutable এবং Immutable-এর পার্থক্য

| Mutable          | Immutable           |
| ---------------- | ------------------- |
| পরিবর্তন করা যায় | পরিবর্তন করা যায় না |
| List             | String              |
| Dictionary       | Tuple               |
| Set              | Integer             |
|                  | Float               |
|                  | Boolean             |

---

## ৪. `=` এবং `==` এর পার্থক্য

```python
x = 10      # Assignment

print(x == 10)   # Comparison
```

---

# 📝 Summary

| Data Type  | Example             |
| ---------- | ------------------- |
| Integer    | `100`               |
| Float      | `3.14`              |
| String     | `"Python"`          |
| Boolean    | `True`              |
| List       | `[1,2,3]`           |
| Tuple      | `(1,2,3)`           |
| Set        | `{1,2,3}`           |
| Dictionary | `{"name":"Yeasin"}` |
| NoneType   | `None`              |

---

# 🎯 Key Takeaways

* ✅ Variable হলো Data রাখার একটি Named Container।
* ✅ Python একটি Dynamically Typed Language।
* ✅ Variable তৈরি করতে Data Type লিখতে হয় না।
* ✅ Python-এর Built-in Data Types শেখা Programming-এর Foundation।
* ✅ `type()` Function দিয়ে যেকোনো Variable-এর Type জানা যায়।
* ✅ Mutable এবং Immutable Objects-এর পার্থক্য জানা খুবই গুরুত্বপূর্ণ।

---

<p align="center">

### ⭐ Happy Coding! 🐍

**Python Fundamentals → Variables & Data Types**

</p>
