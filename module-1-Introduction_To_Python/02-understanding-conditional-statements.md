# 🔀 Understanding Conditional Statements & Implementing Conditional Statements (বাংলা)

<p align="center">
  <img src="https://img.shields.io/badge/Python-Conditional%20Statements-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Topic-if%20else%20elif-success?style=for-the-badge" alt="Topic">
  <img src="https://img.shields.io/badge/Language-Bangla-red?style=for-the-badge" alt="Language">
</p>

> **এই অধ্যায়ে যা শিখবেন**
>
> * Conditional Statement কী?
> * Why Conditional Statements?
> * if Statement
> * if...else Statement
> * if...elif...else Statement
> * Nested if
> * Logical Operators
> * Comparison Operators
> * Ternary Operator
> * Real World Examples
> * Interview Questions

---

# 📚 Table of Contents

* What is Conditional Statement?
* Why We Need Conditional Statements?
* Comparison Operators
* if Statement
* if...else Statement
* if...elif...else Statement
* Nested if
* Logical Operators
* Ternary Operator
* Real World Examples
* Interview Questions
* Summary

---

# 🤔 Conditional Statement কী?

Programming-এ অনেক সময় আমাদের সিদ্ধান্ত (Decision) নিতে হয়।

যেমন,

* যদি বৃষ্টি হয় → ছাতা নিয়ে বের হবো।
* যদি বয়স ১৮ বা তার বেশি হয় → ভোট দিতে পারবে।
* যদি পরীক্ষায় ৮০-এর বেশি নম্বর হয় → Grade A।

এই ধরনের Decision নেওয়ার জন্য Python-এ **Conditional Statements** ব্যবহার করা হয়।

---

# 🌍 Real Life Example

```
যদি আজ শুক্রবার হয়
    তাহলে জুমার নামাজে যাবো
অন্যথায়
    স্বাভাবিক কাজ করবো
```

Programming-এ একই ধারণা ব্যবহার করা হয়।

---

# 🔄 Flow Diagram

```
          Condition
              │
      ┌───────┴────────┐
      │                │
   True              False
      │                │
 Execute A        Execute B
```

---

# ⚖️ Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal                 |
| !=       | Not Equal             |
| >        | Greater Than          |
| <        | Less Than             |
| >=       | Greater Than or Equal |
| <=       | Less Than or Equal    |

---

## Example

```python
age = 20

print(age >= 18)
```

Output

```
True
```

---

# ✅ if Statement

Syntax

```python
if condition:
    statement
```

---

## Example 1

```python
age = 20

if age >= 18:
    print("You are eligible for voting.")
```

Output

```
You are eligible for voting.
```

---

## Example 2

```python
temperature = 35

if temperature > 30:
    print("It's a hot day.")
```

---

# 🔹 if...else Statement

যখন Condition True অথবা False দুই ক্ষেত্রেই আলাদা কাজ করতে হবে তখন if...else ব্যবহার করা হয়।

Syntax

```python
if condition:
    statement
else:
    statement
```

---

## Example

```python
age = 15

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

Output

```
Minor
```

---

# 🎓 Student Pass/Fail Example

```python
marks = 75

if marks >= 40:
    print("Pass")
else:
    print("Fail")
```

Output

```
Pass
```

---

# 🚦 if...elif...else Statement

যখন একাধিক Condition Check করতে হয় তখন elif ব্যবহার করা হয়।

Syntax

```python
if condition1:
    statement

elif condition2:
    statement

elif condition3:
    statement

else:
    statement
```

---

# 📝 Grade Calculator

```python
marks = 82

if marks >= 80:
    print("Grade A")

elif marks >= 70:
    print("Grade B")

elif marks >= 60:
    print("Grade C")

elif marks >= 40:
    print("Grade D")

else:
    print("Fail")
```

Output

```
Grade A
```

---

# 🔍 Execution Flow

Python উপরের Condition থেকে নিচে Check করে।

```
marks = 82

marks >= 80 ?  ✅ True

↓

Grade A

↓

Program Stops
```

নিচের Condition আর Check করা হয় না।

---

# 🪆 Nested if Statement

একটি if-এর ভিতরে আরেকটি if ব্যবহার করা হলে তাকে Nested if বলে।

---

## Example

```python
age = 22
has_nid = True

if age >= 18:

    if has_nid:
        print("Eligible for voting")

    else:
        print("Need NID")

else:
    print("Not eligible")
```

Output

```
Eligible for voting
```

---

# 🔗 Logical Operators

Python-এ তিনটি প্রধান Logical Operator আছে।

| Operator | Meaning                             |
| -------- | ----------------------------------- |
| and      | দুইটিই True হতে হবে                 |
| or       | যেকোনো একটি True হলেই হবে           |
| not      | True কে False এবং False কে True করে |

---

# AND Example

```python
age = 22
has_license = True

if age >= 18 and has_license:
    print("Can drive")
```

Output

```
Can drive
```

---

# OR Example

```python
is_student = False
has_coupon = True

if is_student or has_coupon:
    print("Discount Available")
```

Output

```
Discount Available
```

---

# NOT Example

```python
logged_in = False

if not logged_in:
    print("Please Login")
```

Output

```
Please Login
```

---

# 🎯 Ternary Operator

ছোট if...else এক লাইনে লেখার জন্য Ternary Operator ব্যবহার করা হয়।

Syntax

```python
value_if_true if condition else value_if_false
```

---

## Example

```python
age = 20

status = "Adult" if age >= 18 else "Minor"

print(status)
```

Output

```
Adult
```

---

# 💡 Real World Example 1

## ATM Withdrawal

```python
balance = 5000
withdraw = 3000

if withdraw <= balance:
    print("Transaction Successful")

else:
    print("Insufficient Balance")
```

---

# 💡 Real World Example 2

## Login System

```python
username = "admin"
password = "1234"

if username == "admin" and password == "1234":
    print("Login Successful")

else:
    print("Invalid Credentials")
```

---

# 💡 Real World Example 3

## Movie Ticket

```python
age = 12

if age < 5:
    print("Free Ticket")

elif age < 18:
    print("Child Ticket")

elif age < 60:
    print("Regular Ticket")

else:
    print("Senior Citizen Discount")
```

---

# ⚠️ Indentation

Python-এ Curly Brace `{}` ব্যবহার করা হয় না।

Indentation দিয়েই Block নির্ধারণ করা হয়।

✅ Correct

```python
if True:
    print("Hello")
```

❌ Wrong

```python
if True:
print("Hello")
```

Output

```
IndentationError
```

---

# 🚫 Common Mistakes

## Mistake 1

```python
if age = 18:
```

❌ Wrong

---

Correct

```python
if age == 18:
```

---

## Mistake 2

```python
if score > 80
    print(score)
```

❌ Colon (`:`) ভুলে যাওয়া

---

Correct

```python
if score > 80:
    print(score)
```

---

# 🎯 Interview Questions

## ১. Conditional Statement কী?

Conditional Statement এমন একটি Control Structure যা নির্দিষ্ট Condition অনুযায়ী Program-এর Flow নিয়ন্ত্রণ করে।

---

## ২. if এবং if...else-এর মধ্যে পার্থক্য কী?

| if                            | if...else                               |
| ----------------------------- | --------------------------------------- |
| শুধুমাত্র True হলে Execute হয় | True এবং False উভয় ক্ষেত্রেই Execute হয় |

---

## ৩. elif কেন ব্যবহার করা হয়?

একাধিক Condition Sequentially Check করার জন্য।

---

## ৪. Nested if কী?

একটি if Block-এর ভিতরে আরেকটি if ব্যবহার করাকে Nested if বলে।

---

## ৫. Python-এ Block কীভাবে নির্ধারণ করা হয়?

Indentation দিয়ে।

---

# 📝 Summary

| Statement        | Purpose                   |
| ---------------- | ------------------------- |
| if               | একটিমাত্র Condition Check |
| if...else        | দুইটি Decision            |
| if...elif...else | Multiple Decision         |
| Nested if        | ভিতরে আরও Decision        |
| Ternary          | One-line if...else        |

---

# 🎯 Key Takeaways

✅ Conditional Statement Program-কে Decision নিতে সাহায্য করে।

✅ `if`, `if...else`, `if...elif...else` হলো Python-এর প্রধান Conditional Structures।

✅ Multiple Condition Check করতে `elif` ব্যবহার করা হয়।

✅ Complex Logic তৈরির জন্য `and`, `or`, `not` ব্যবহার করা হয়।

✅ Python-এ Indentation অত্যন্ত গুরুত্বপূর্ণ।

---

<p align="center">

# 🚀 Next Topic

## 🔁 Loops in Python (for Loop & while Loop Deep Dive)

**"Condition থেকে এবার Iteration শেখার পালা!"**

⭐ Happy Coding! 🐍

</p>
