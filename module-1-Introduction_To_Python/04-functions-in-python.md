# 🐍 Functions in Python (বাংলা Deep Dive)

<p align="center">
  <img src="https://img.shields.io/badge/Python-Functions-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-success?style=for-the-badge" alt="Level">
  <img src="https://img.shields.io/badge/Language-Bangla-red?style=for-the-badge" alt="Language">
</p>

> ## 🎯 এই অধ্যায়ে যা শিখবেন
>
> * Function কী?
> * কেন Function ব্যবহার করা হয়?
> * Function Declaration & Calling
> * User Defined Functions
> * Parameters vs Arguments
> * Types of Arguments
> * Return Values
> * Local & Global Scope
> * Lambda Function (Introduction)
> * Real World Examples
> * Best Practices
> * Interview Questions

---

# 📚 Table of Contents

* Introduction
* What is a Function?
* Why Use Functions?
* Function Syntax
* User Defined Functions
* Parameters and Arguments
* Types of Arguments
* Return Values
* Scope
* Lambda Functions
* Real World Examples
* Best Practices
* Interview Questions
* Summary

---

# 🤔 Function কী?

Function হলো এমন একটি **Reusable Block of Code** যা একটি নির্দিষ্ট কাজ সম্পন্ন করে।

একবার Function তৈরি করলে প্রয়োজন অনুযায়ী যতবার ইচ্ছা ব্যবহার করা যায়।

---

# 🌍 Real Life Example

ধরুন আপনার বাসায় একটি Coffee Machine আছে।

আপনি যখনই Coffee চান,

```
Coffee Machine

↓

Coffee তৈরি করে

↓

আপনার হাতে দেয়
```

আপনাকে প্রতিবার Coffee বানানোর পুরো Process লিখতে হয় না।

Programming-এ Function একই কাজ করে।

---

# ❓ কেন Function ব্যবহার করা হয়?

Function ব্যবহারের সুবিধা:

✅ Code Reuse করা যায়

✅ Code ছোট হয়

✅ Debug করা সহজ হয়

✅ Maintenance সহজ হয়

✅ Large Project Manage করা সহজ হয়

---

# 🔨 Function Syntax

```python
def function_name():
    # code
```

---

# প্রথম Function

```python
def greet():
    print("Hello Python")
```

Function তৈরি করলেই Execute হবে না।

Call করতে হবে।

```python
greet()
```

Output

```
Hello Python
```

---

# 🔄 Execution Flow

```
Program Start

↓

Function Define

↓

Function Call

↓

Execute Function Body

↓

Return Control
```

---

# 👨‍💻 User Defined Function

যে Function Programmer নিজে তৈরি করে তাকে User Defined Function বলে।

---

Example

```python
def welcome():

    print("Welcome")

welcome()
```

Output

```
Welcome
```

---

# 📥 Parameters কী?

Parameter হলো Function Definition-এর ভিতরে থাকা Variable।

```python
def greet(name):

    print("Hello", name)
```

এখানে

```
name

↓

Parameter
```

---

# 📤 Arguments কী?

Function Call করার সময় যে Value পাঠানো হয় তাকে Argument বলে।

```python
greet("Yeasin")
```

এখানে

```
"Yeasin"

↓

Argument
```

---

# 🎯 Parameter vs Argument

| Parameter                     | Argument                    |
| ----------------------------- | --------------------------- |
| Function Define করার সময় থাকে | Function Call করার সময় থাকে |
| Variable                      | Actual Value                |

---

# Example

```python
def add(a, b):

    print(a + b)

add(10, 20)
```

Output

```
30
```

---

# 📌 Positional Arguments

Position অনুযায়ী Value Assign হয়।

```python
def student(name, age):

    print(name)
    print(age)

student("Rahim", 20)
```

Output

```
Rahim

20
```

---

# 🔖 Keyword Arguments

Variable Name ব্যবহার করে Value পাঠানো হয়।

```python
def student(name, age):

    print(name)
    print(age)

student(age=20, name="Rahim")
```

Output

```
Rahim

20
```

---

# ⚙️ Default Arguments

Default Value দেওয়া যায়।

```python
def country(name="Bangladesh"):

    print(name)

country()

country("Japan")
```

Output

```
Bangladesh

Japan
```

---

# 📦 Variable Length Arguments (*args)

Unlimited Positional Arguments নেওয়া যায়।

```python
def total(*numbers):

    print(numbers)

total(1,2,3,4,5)
```

Output

```
(1,2,3,4,5)
```

---

# 🗂 Variable Length Keyword Arguments (**kwargs)

Unlimited Keyword Arguments নেওয়া যায়।

```python
def student(**info):

    print(info)

student(name="Yeasin", age=24)
```

Output

```
{
'name':'Yeasin',
'age':24
}
```

---

# 🔙 Return Statement

Function Result Return করার জন্য return ব্যবহার করা হয়।

---

Example

```python
def add(a,b):

    return a+b

result = add(10,20)

print(result)
```

Output

```
30
```

---

# Without Return

```python
def add(a,b):

    print(a+b)

result = add(10,20)

print(result)
```

Output

```
30

None
```

কারণ Function কোনো Value Return করেনি।

---

# Multiple Return Values

```python
def calculation(a,b):

    return a+b,a-b,a*b

result = calculation(10,5)

print(result)
```

Output

```
(15,5,50)
```

---

# Unpacking Return Values

```python
def calculation(a,b):

    return a+b,a-b

sum_result,diff_result=calculation(20,10)

print(sum_result)

print(diff_result)
```

Output

```
30

10
```

---

# 🌐 Variable Scope

Scope নির্ধারণ করে Variable কোথা থেকে Access করা যাবে।

---

# Local Scope

Function-এর ভিতরে তৈরি Variable শুধুমাত্র Function-এর ভিতরে থাকে।

```python
def demo():

    message="Hello"

    print(message)

demo()
```

---

Outside Access করলে

```python
print(message)
```

Output

```
NameError
```

---

# Global Scope

Function-এর বাইরে তৈরি Variable পুরো Program-এ ব্যবহার করা যায়।

```python
language="Python"

def show():

    print(language)

show()

print(language)
```

Output

```
Python

Python
```

---

# global Keyword

Function-এর ভিতরে Global Variable Modify করতে।

```python
count=0

def increase():

    global count

    count+=1

increase()

print(count)
```

Output

```
1
```

---

# 🔥 Lambda Function

এক লাইনের Anonymous Function।

Syntax

```python
lambda parameters : expression
```

---

Example

```python
square=lambda x:x*x

print(square(5))
```

Output

```
25
```

---

# 🎯 Real World Example 1

Student Grade

```python
def grade(mark):

    if mark>=80:

        return "A"

    elif mark>=70:

        return "B"

    elif mark>=60:

        return "C"

    else:

        return "Fail"

print(grade(85))
```

Output

```
A
```

---

# 🎯 Real World Example 2

Simple Calculator

```python
def calculator(a,b,operation):

    if operation=="add":

        return a+b

    elif operation=="sub":

        return a-b

print(calculator(20,10,"add"))
```

Output

```
30
```

---

# 🎯 Real World Example 3

Login Check

```python
def login(username,password):

    if username=="admin" and password=="1234":

        return True

    return False

print(login("admin","1234"))
```

Output

```
True
```

---

# 📊 Call Stack (Basic Idea)

```
main()

↓

login()

↓

check_password()

↓

Return

↓

Return

↓

Program End
```

Python Function Call Stack অনুসরণ করে।

---

# ⚠️ Common Mistakes

## Mistake 1

```python
def greet()

    print("Hello")
```

❌ Colon নেই

---

Correct

```python
def greet():

    print("Hello")
```

---

## Mistake 2

```python
def add(a,b):

    return

    a+b
```

return-এর পরে Code Execute হবে না।

---

## Mistake 3

```python
def show():

    name="Python"

print(name)
```

Output

```
NameError
```

কারণ Variable Local Scope-এর মধ্যে আছে।

---

# 🚀 Best Practices

✅ Function Name Verb দিয়ে শুরু করুন

```
calculate_total()

send_email()

create_user()
```

---

✅ এক Function একটিমাত্র কাজ করুক

---

✅ ছোট ছোট Function লিখুন

---

✅ প্রয়োজন ছাড়া global Variable ব্যবহার করবেন না

---

✅ Meaningful Parameter Name ব্যবহার করুন

---

# 💼 Interview Questions

## ১. Function কী?

Reusable Code Block যা নির্দিষ্ট একটি কাজ সম্পন্ন করে।

---

## ২. Parameter এবং Argument-এর পার্থক্য কী?

| Parameter         | Argument     |
| ----------------- | ------------ |
| Definition-এর সময় | Call-এর সময়  |
| Variable          | Actual Value |

---

## ৩. return এবং print-এর মধ্যে পার্থক্য কী?

| return                       | print               |
| ---------------------------- | ------------------- |
| Value Function Caller-কে দেয় | শুধু Screen-এ দেখায় |
| Function শেষ করে             | Function শেষ করে না |

---

## ৪. Local Scope কী?

Function-এর ভিতরের Variable যা বাইরে Access করা যায় না।

---

## ৫. Global Scope কী?

Function-এর বাইরে থাকা Variable যা Program-এর যেকোনো জায়গা থেকে Access করা যায়।

---

## ৬. Lambda Function কী?

এক লাইনের Anonymous Function যা ছোট Expression-এর জন্য ব্যবহার করা হয়।

---

# 📝 Summary

| Topic        | Description                    |
| ------------ | ------------------------------ |
| def          | Function তৈরি করে              |
| Parameter    | Function Variable              |
| Argument     | Passed Value                   |
| return       | Result Return করে              |
| Local Scope  | Function-এর ভিতরে সীমাবদ্ধ     |
| Global Scope | পুরো Program-এ Accessible      |
| *args        | Unlimited Positional Arguments |
| **kwargs     | Unlimited Keyword Arguments    |
| lambda       | Anonymous Function             |

---

# 🎯 Key Takeaways

✅ Function হলো Python-এর অন্যতম গুরুত্বপূর্ণ Building Block।

✅ Code Reusability এবং Maintainability বাড়ানোর জন্য Function ব্যবহার করা হয়।

✅ Parameter এবং Argument-এর পার্থক্য Interview-এর জন্য খুবই গুরুত্বপূর্ণ।

✅ `return` ব্যবহার করলে Function Result অন্য জায়গায় ব্যবহার করা যায়।

✅ Local এবং Global Scope বুঝতে পারলে Variable সম্পর্কিত অনেক Bug এড়ানো যায়।

✅ `*args` এবং `**kwargs` Flexible Function তৈরিতে সাহায্য করে।

---

<p align="center">

# 🐍 Python Essentials

## Chapter 04 Complete ✅

### 🚀 Next Topic

# 📦 Python Data Structures Deep Dive

* Lists
* Tuples
* Sets
* Dictionaries
* Comprehensions
* Built-in Methods

⭐ Happy Coding!

</p>
