# 🐍 Modules, Packages & Python Best Practices (বাংলা Deep Dive)

<p align="center">
  <img src="https://img.shields.io/badge/Python-Modules%20%26%20Packages-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-success?style=for-the-badge" alt="Level">
  <img src="https://img.shields.io/badge/Language-Bangla-red?style=for-the-badge" alt="Language">
</p>

> ## 🎯 এই অধ্যায়ে যা শিখবেন
>
> * Module কী?
> * Package কী?
> * Module vs Package
> * Import Statement
> * Built-in Modules
> * Custom Modules
> * Creating Packages
> * Absolute & Relative Imports
> * `__name__ == "__main__"`
> * Python Project Structure
> * Python Best Practices
> * Real World Examples
> * Interview Questions

---

# 📚 Table of Contents

* Introduction
* Modules
* Packages
* Import Statements
* Built-in Modules
* Custom Modules
* Creating Packages
* Project Structure
* Python Best Practices
* Real World Examples
* Interview Questions
* Summary

---

# 📖 Introduction

ছোট Project-এ সব Code একটি File-এ লেখা সম্ভব।

কিন্তু Project বড় হলে হাজার হাজার Line Code একটি File-এ রাখা অসম্ভব হয়ে যায়।

তাই Code-কে ছোট ছোট অংশে ভাগ করা হয়।

Python-এ এই অংশগুলোকে বলা হয়

* Module
* Package

---

# 📦 Module কী?

Module হলো একটি Python File (`.py`) যেখানে Function, Class, Variable এবং অন্যান্য Code থাকে।

সহজভাবে,

> **One Python File = One Module**

---

# 🌍 Real Life Example

ধরুন একটি Library আছে।

```
Library
│
├── Math Book
├── English Book
├── Physics Book
└── History Book
```

এখানে প্রতিটি Book একটি Module-এর মতো।

---

# প্রথম Module

## calculator.py

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

---

## main.py

```python
import calculator

print(calculator.add(10, 20))

print(calculator.subtract(30, 10))
```

Output

```
30

20
```

---

# Import Statement

Module ব্যবহার করার জন্য import করতে হয়।

```
import module_name
```

Example

```python
import math
```

---

# নির্দিষ্ট Function Import

```python
from math import sqrt

print(sqrt(25))
```

Output

```
5.0
```

---

# Multiple Import

```python
from math import sqrt, pi

print(pi)

print(sqrt(64))
```

---

# Alias ব্যবহার

```python
import math as m

print(m.sqrt(81))
```

Output

```
9
```

---

# ⭐ Built-in Modules

Python-এর সাথে অনেক Module আগে থেকেই থাকে।

---

## math

```python
import math

print(math.pi)

print(math.sqrt(100))

print(math.factorial(5))
```

Output

```
3.1415926535

10

120
```

---

## random

```python
import random

print(random.randint(1, 10))
```

Random Number Generate করবে।

---

## datetime

```python
from datetime import datetime

print(datetime.now())
```

বর্তমান Date & Time দেখাবে।

---

## os

```python
import os

print(os.getcwd())
```

বর্তমান Working Directory দেখাবে।

---

# 🏗 Custom Module

ধরুন

```
project/

calculator.py

main.py
```

---

calculator.py

```python
def multiply(a, b):

    return a * b
```

---

main.py

```python
import calculator

print(calculator.multiply(5, 10))
```

Output

```
50
```

---

# 📦 Package কী?

Package হলো একাধিক Module-এর Collection।

অর্থাৎ,

```
Package

↓

Module

↓

Function/Class
```

---

# Real Life Example

```
Shopping Mall

↓

Clothing Section

↓

Shirt
Pant

↓

Electronics Section

↓

Laptop
Mobile
```

---

# Package Structure

```
my_app/

│

├── main.py

│

├── utils/

│     ├── __init__.py
│     ├── math_utils.py
│     └── string_utils.py

│

└── services/

      ├── __init__.py
      └── user_service.py
```

---

# **init**.py

এই File Python-কে বলে যে Folder-টি একটি Package।

Python 3.3+ এ Optional হলেও Best Practice হিসেবে রাখা হয়।

---

# Package Import

```
utils

│

└── math_utils.py
```

math_utils.py

```python
def add(a, b):

    return a + b
```

---

main.py

```python
from utils.math_utils import add

print(add(10, 20))
```

Output

```
30
```

---

# Absolute Import

```python
from utils.math_utils import add
```

Project Root থেকে Import করা হয়।

---

# Relative Import

```python
from .math_utils import add
```

Package-এর ভিতরে Import করার জন্য ব্যবহার করা হয়।

---

# **name** == "**main**"

Python File Run হলে

```
__name__

↓

"__main__"
```

হয়ে যায়।

---

Example

```python
def greet():

    print("Hello")

if __name__ == "__main__":

    greet()
```

---

এখন

```
python app.py
```

Run করলে greet() Execute হবে।

কিন্তু অন্য Module থেকে Import করলে Execute হবে না।

---

# 🎯 কেন এটি ব্যবহার করা হয়?

✅ Testing

✅ Demo Code

✅ Script হিসেবে Run করার জন্য

---

# Project Structure Best Practice

```
my_project/

│

├── app/

│    ├── __init__.py

│    ├── models/

│    ├── services/

│    ├── routes/

│    ├── utils/

│    └── config/

│

├── tests/

├── requirements.txt

├── README.md

└── main.py
```

---

# 🏆 Python Best Practices

---

# ১. Meaningful Variable Names

❌

```python
a = 100

b = 20
```

---

✅

```python
student_age = 20

total_price = 100
```

---

# ২. Function ছোট রাখুন

❌

এক Function-এ 500 Line Code

---

✅

এক Function একটিমাত্র কাজ করবে।

---

# ৩. DRY Principle

> Don't Repeat Yourself

❌

একই Code বারবার Copy করবেন না।

---

✅

Function বা Module তৈরি করুন।

---

# ৪. PEP 8 Follow করুন

Variable

```python
student_name
```

Function

```python
calculate_total()
```

Class

```python
StudentManager
```

Constant

```python
MAX_USERS = 100
```

---

# ৫. Comments ব্যবহার করুন

```python
# Calculate total price

total = price * quantity
```

---

# ৬. Docstring ব্যবহার করুন

```python
def add(a, b):
    """
    Returns the sum of two numbers.
    """

    return a + b
```

---

# ৭. Exception Handle করুন

❌

```python
number = int(input())
```

---

✅

```python
try:

    number = int(input())

except ValueError:

    print("Invalid Input")
```

---

# ৮. Magic Number Avoid করুন

❌

```python
price = quantity * 0.15
```

---

✅

```python
VAT_RATE = 0.15

price = quantity * VAT_RATE
```

---

# ৯. Virtual Environment ব্যবহার করুন

```
python -m venv venv
```

Activate

Windows

```
venv\Scripts\activate
```

Linux / macOS

```
source venv/bin/activate
```

---

# ১০. requirements.txt ব্যবহার করুন

Generate

```
pip freeze > requirements.txt
```

Install

```
pip install -r requirements.txt
```

---

# 💼 Real World Example

```
student_management/

│

├── main.py

├── students.py

├── courses.py

├── utils.py

└── config.py
```

---

students.py

```python
def get_students():

    return ["Rahim", "Karim", "Sakib"]
```

---

main.py

```python
from students import get_students

students = get_students()

for student in students:

    print(student)
```

Output

```
Rahim

Karim

Sakib
```

---

# 🎯 Interview Questions

## ১. Module কী?

একটি `.py` File যেখানে Function, Class এবং Variable থাকে।

---

## ২. Package কী?

একাধিক Related Module-এর Collection।

---

## ৩. Module এবং Package-এর পার্থক্য কী?

| Module             | Package                        |
| ------------------ | ------------------------------ |
| Single Python File | Multiple Modules-এর Collection |
| `.py` File         | Folder                         |

---

## ৪. import এবং from...import-এর পার্থক্য কী?

```
import math

math.sqrt(25)
```

vs

```
from math import sqrt

sqrt(25)
```

---

## ৫. **name** == "**main**" কেন ব্যবহার করা হয়?

কোনো File Direct Run করা হয়েছে নাকি Import করা হয়েছে তা নির্ধারণ করার জন্য।

---

# 📋 Summary

| Topic       | Description              |
| ----------- | ------------------------ |
| Module      | Single Python File       |
| Package     | Collection of Modules    |
| import      | Module Import করে        |
| from import | Specific Item Import করে |
| alias       | Short Name দেয়           |
| **init**.py | Package Initialize করে   |
| **name**    | Module-এর Name ধরে রাখে  |
| PEP 8       | Python Coding Standard   |

---

# 🎯 Key Takeaways

✅ Module Code Reusability বাড়ায়।

✅ Package Large Project Organize করতে সাহায্য করে।

✅ Built-in Module ব্যবহার করে অনেক কাজ সহজ করা যায়।

✅ `__name__ == "__main__"` Professional Python Development-এর গুরুত্বপূর্ণ Concept।

✅ PEP 8 এবং Best Practices Follow করলে Code Clean, Readable এবং Maintainable হয়।

---

<p align="center">

# 🐍 Python Essentials

## Chapter 05 Complete ✅

### 🚀 Next Topic

# 📂 File Handling & Exception Handling in Python

* Reading Files
* Writing Files
* Context Manager (`with`)
* try / except / finally
* Custom Exceptions
* Best Practices

⭐ Happy Coding! 🚀

</p>
