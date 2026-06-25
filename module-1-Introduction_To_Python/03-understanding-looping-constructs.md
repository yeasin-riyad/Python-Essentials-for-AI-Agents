# 🔄 Understanding Looping Constructs in Python (বাংলা Deep Dive)

<p align="center">
  <img src="https://img.shields.io/badge/Python-Looping%20Constructs-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Level-Beginner-success?style=for-the-badge" alt="Level">
  <img src="https://img.shields.io/badge/Language-Bangla-red?style=for-the-badge" alt="Language">
</p>

> ## 🎯 এই অধ্যায়ে যা শিখবেন
>
> * Loop কী?
> * কেন Loop ব্যবহার করা হয়?
> * while Loop
> * for Loop
> * range() Function
> * Nested Loop
> * break, continue, pass
> * else with Loop
> * Infinite Loop
> * Real World Examples
> * Time Complexity ধারণা
> * Interview Questions

---

# 📚 Table of Contents

* Introduction
* What is Loop?
* Why Loop?
* while Loop
* for Loop
* range() Function
* Nested Loop
* Loop Control Statements
* else with Loop
* Infinite Loop
* Real World Examples
* Common Mistakes
* Interview Questions
* Summary

---

# 🔄 Loop কী?

Loop হলো এমন একটি Programming Construct যা একই Code বারবার Execute করতে সাহায্য করে যতক্ষণ পর্যন্ত একটি Condition সত্য থাকে অথবা কোনো Collection-এর সব Element শেষ না হয়।

সহজ ভাষায়,

> **Loop = Repeat Until Done**

---

# 🌍 Real Life Example

ধরুন একজন শিক্ষক ৫০ জন শিক্ষার্থীকে একই কথা বলছেন।

❌ Loop ছাড়া

```
Hello Student 1
Hello Student 2
Hello Student 3
...
Hello Student 50
```

এভাবে ৫০ বার লিখতে হবে।

---

✅ Loop ব্যবহার করলে

```python
for i in range(50):
    print("Hello Student")
```

একবার Code লিখেই ৫০ বার Execute হবে।

---

# 🤔 কেন Loop ব্যবহার করা হয়?

Loop ব্যবহার করলে—

* ✅ একই Code বারবার লিখতে হয় না
* ✅ Code ছোট হয়
* ✅ Maintain করা সহজ হয়
* ✅ Performance ভালো হয়
* ✅ Automation সম্ভব হয়

---

# 🔁 while Loop

while Loop Condition True থাকা পর্যন্ত Execute হয়।

---

## Syntax

```python
while condition:
    statement
```

---

# Example 1

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Output

```
1
2
3
4
5
```

---

# Execution Flow

```
count = 1

↓

count <= 5 ?

↓

True

↓

Print

↓

count += 1

↓

Repeat
```

---

# Example 2

Countdown Timer

```python
seconds = 5

while seconds > 0:
    print(seconds)
    seconds -= 1

print("Time Up!")
```

Output

```
5
4
3
2
1
Time Up!
```

---

# ⚠️ Infinite Loop

```python
while True:
    print("Hello")
```

এটি কখনো Stop হবে না।

---

Infinite Loop বন্ধ করতে

```
Ctrl + C
```

অথবা

```
break
```

ব্যবহার করা হয়।

---

# 🔂 for Loop

Python-এর সবচেয়ে বেশি ব্যবহৃত Loop।

এটি Collection-এর প্রতিটি Element-এর উপর Iterate করে।

---

## Syntax

```python
for variable in iterable:
    statement
```

---

# Example

```python
fruits = ["Apple", "Banana", "Orange"]

for fruit in fruits:
    print(fruit)
```

Output

```
Apple
Banana
Orange
```

---

# String Iterate করা

```python
name = "Python"

for letter in name:
    print(letter)
```

Output

```
P
y
t
h
o
n
```

---

# 🔢 range() Function

range() Number Generate করে।

---

## range(stop)

```python
for i in range(5):
    print(i)
```

Output

```
0
1
2
3
4
```

---

## range(start, stop)

```python
for i in range(1,6):
    print(i)
```

Output

```
1
2
3
4
5
```

---

## range(start, stop, step)

```python
for i in range(2,11,2):
    print(i)
```

Output

```
2
4
6
8
10
```

---

# Reverse Loop

```python
for i in range(10,0,-1):
    print(i)
```

Output

```
10
9
8
7
6
5
4
3
2
1
```

---

# 🪆 Nested Loop

একটি Loop-এর ভিতরে আরেকটি Loop থাকলে তাকে Nested Loop বলে।

---

# Example

```python
for row in range(3):

    for col in range(3):

        print("*", end=" ")

    print()
```

Output

```
* * *

* * *

* * *
```

---

# Multiplication Table

```python
for i in range(1,6):

    for j in range(1,6):

        print(i*j, end="\t")

    print()
```

Output

```
1 2 3 4 5

2 4 6 8 10

3 6 9 12 15

4 8 12 16 20

5 10 15 20 25
```

---

# 🛑 break Statement

break Loop সম্পূর্ণ Stop করে দেয়।

---

Example

```python
for i in range(10):

    if i == 5:
        break

    print(i)
```

Output

```
0
1
2
3
4
```

---

# ⏭ continue Statement

বর্তমান Iteration Skip করে পরের Iteration-এ যায়।

---

Example

```python
for i in range(6):

    if i == 3:
        continue

    print(i)
```

Output

```
0
1
2
4
5
```

---

# 🚧 pass Statement

pass কিছুই করে না।

Placeholder হিসেবে ব্যবহার করা হয়।

```python
for i in range(5):

    if i == 3:
        pass

    print(i)
```

Output

```
0
1
2
3
4
```

---

# 🎁 else with Loop

Loop স্বাভাবিকভাবে শেষ হলে else Execute হয়।

---

Example

```python
for i in range(5):

    print(i)

else:

    print("Loop Finished")
```

Output

```
0
1
2
3
4
Loop Finished
```

---

break ব্যবহার করলে

```python
for i in range(5):

    if i == 2:
        break

else:

    print("Finished")
```

Output

```
Nothing Printed
```

কারণ Loop break দিয়ে শেষ হয়েছে।

---

# 💡 Real World Example 1

Password Check

```python
password = "python123"

while True:

    user = input("Enter Password: ")

    if user == password:
        print("Login Success")
        break

    else:
        print("Wrong Password")
```

---

# 💡 Real World Example 2

Shopping Cart

```python
cart = ["Laptop", "Mouse", "Keyboard"]

for item in cart:

    print(item)
```

Output

```
Laptop
Mouse
Keyboard
```

---

# 💡 Real World Example 3

Even Numbers

```python
for number in range(2,21,2):

    print(number)
```

Output

```
2
4
6
8
10
12
14
16
18
20
```

---

# 💡 Real World Example 4

Sum of Numbers

```python
total = 0

for number in range(1,11):

    total += number

print(total)
```

Output

```
55
```

---

# 📊 Time Complexity

## while Loop

```
while i < n
```

Complexity

```
O(n)
```

---

## for Loop

```
for i in range(n)
```

Complexity

```
O(n)
```

---

## Nested Loop

```
for i in range(n):

    for j in range(n):
```

Complexity

```
O(n²)
```

---

# ⚠️ Common Mistakes

## Mistake 1

```python
while count <= 5:

    print(count)
```

❌ count Update করা হয়নি।

Result

```
Infinite Loop
```

---

Correct

```python
count = 1

while count <= 5:

    print(count)

    count += 1
```

---

## Mistake 2

```python
for i in range(5):

print(i)
```

❌ Indentation Error

---

Correct

```python
for i in range(5):

    print(i)
```

---

# 🎯 Interview Questions

## ১. Loop কী?

Loop হলো এমন একটি Control Structure যা একই Code বারবার Execute করে।

---

## ২. while এবং for Loop-এর মধ্যে পার্থক্য কী?

| while                                    | for                                |
| ---------------------------------------- | ---------------------------------- |
| Condition Based                          | Iterable Based                     |
| Iteration সংখ্যা আগে জানা নাও থাকতে পারে | Iteration সংখ্যা সাধারণত জানা থাকে |

---

## ৩. break কী করে?

Loop সম্পূর্ণ বন্ধ করে দেয়।

---

## ৪. continue কী করে?

বর্তমান Iteration Skip করে পরবর্তী Iteration-এ যায়।

---

## ৫. pass কেন ব্যবহার করা হয়?

Future Implementation-এর জন্য Placeholder হিসেবে।

---

## ৬. Nested Loop-এর Complexity কত?

```
O(n²)
```

---

# 📝 Summary

| Topic       | Purpose                                |
| ----------- | -------------------------------------- |
| while       | Condition True থাকা পর্যন্ত Execute    |
| for         | Iterable-এর প্রতিটি Element Iterate    |
| range()     | Number Sequence Generate               |
| break       | Loop Stop                              |
| continue    | Current Iteration Skip                 |
| pass        | Placeholder                            |
| Nested Loop | Loop-এর ভিতরে Loop                     |
| else        | Loop Successfully Complete হলে Execute |

---

# 🚀 Best Practices

✅ Infinite Loop এড়াতে Condition Update করুন।

✅ Unknown Iteration হলে while ব্যবহার করুন।

✅ List, Tuple, String Iterate করার জন্য for Loop ব্যবহার করুন।

✅ Nested Loop প্রয়োজন ছাড়া ব্যবহার করবেন না।

✅ Meaningful Variable Name ব্যবহার করুন।

✅ break এবং continue শুধুমাত্র প্রয়োজন হলে ব্যবহার করুন।

---

# 🎯 Key Takeaways

* 🔹 Loop Programming-এর অন্যতম গুরুত্বপূর্ণ Control Structure।
* 🔹 Python-এ মূলত `while` এবং `for` Loop ব্যবহৃত হয়।
* 🔹 `range()` Function সংখ্যা Generate করার জন্য ব্যবহৃত হয়।
* 🔹 `break`, `continue`, এবং `pass` Loop-এর Behaviour নিয়ন্ত্রণ করে।
* 🔹 Nested Loop দিয়ে Matrix, Pattern, এবং Table তৈরি করা যায়।
* 🔹 বাস্তব জীবনের প্রায় সব Automation Task-এ Loop ব্যবহৃত হয়।

---

<p align="center">

# 🐍 Python Essentials

### Chapter 03 Complete ✅

⭐ **Next Topic:** Functions in Python (User Defined Functions, Parameters, Arguments, Return Values & Scope)

**Happy Coding! 🚀**

</p>
