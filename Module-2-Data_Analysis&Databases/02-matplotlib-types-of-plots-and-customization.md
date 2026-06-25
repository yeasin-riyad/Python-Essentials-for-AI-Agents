# 📊 Matplotlib: Types of Plots & Customizing Plots

<p align="center">
  <img src="https://img.shields.io/badge/Python-Matplotlib-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Data%20Visualization-Essential-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=for-the-badge" />
</p>

---

# 🎯 Learning Objectives

এই অধ্যায় শেষে আপনি জানতে পারবেন—

* Matplotlib কী
* কেন Matplotlib ব্যবহার করা হয়
* Figure এবং Axes কী
* Line Plot
* Bar Chart
* Scatter Plot
* Histogram
* Pie Chart
* Box Plot
* Subplots
* Plot Customization
* Title, Labels, Legends
* Colors & Styles
* Markers
* Grid
* Figure Size
* Save Figure

---

# 📚 Table of Contents

1. Introduction to Matplotlib
2. Figure & Axes
3. Line Plot
4. Bar Chart
5. Scatter Plot
6. Histogram
7. Pie Chart
8. Box Plot
9. Subplots
10. Plot Customization
11. Save Figure
12. Real World Examples
13. Interview Questions
14. Summary

---

# 📖 What is Matplotlib?

**Matplotlib** হলো Python-এর সবচেয়ে জনপ্রিয় Data Visualization Library।

এটি ব্যবহার করে Data-কে Graph, Chart এবং Plot-এর মাধ্যমে Visualize করা যায়।

---

# 🤔 Why Matplotlib?

ধরুন আপনার কাছে Sales Data আছে।

| Month | Sales |
| ----- | ----- |
| Jan   | 100   |
| Feb   | 120   |
| Mar   | 180   |
| Apr   | 150   |

Table দেখে Trend বোঝা কঠিন।

কিন্তু Graph ব্যবহার করলে—

✅ Trend বোঝা সহজ

✅ Comparison করা সহজ

✅ Pattern Detect করা সহজ

---

# 📦 Installation

```bash
pip install matplotlib
```

Import:

```python
import matplotlib.pyplot as plt
```

---

# 🏗 Figure & Axes

Matplotlib-এর Core Components।

## Figure

পুরো Canvas।

```python
plt.figure()
```

---

## Axes

যেখানে Plot Draw হয়।

```python
fig, ax = plt.subplots()
```

---

# 📈 Line Plot

Trend Analysis-এর জন্য সবচেয়ে জনপ্রিয় Plot।

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

plt.plot(x, y)

plt.show()
```

---

## Use Cases

* Sales Trend
* Temperature Change
* Growth Analysis
* Stock Prices

---

# 📊 Bar Chart

Category Comparison-এর জন্য।

```python
students = ["A", "B", "C", "D"]
marks = [80, 90, 70, 85]

plt.bar(students, marks)

plt.show()
```

---

## Horizontal Bar Chart

```python
plt.barh(students, marks)
```

---

## Use Cases

* Product Sales
* Survey Results
* Student Marks

---

# 🎯 Scatter Plot

দুই Variable-এর Relationship দেখায়।

```python
height = [150, 160, 170, 180]
weight = [50, 55, 70, 80]

plt.scatter(height, weight)

plt.show()
```

---

## Use Cases

* Machine Learning
* Correlation Analysis
* Data Exploration

---

# 📊 Histogram

Data Distribution দেখানোর জন্য।

```python
ages = [18,20,21,22,18,19,25,24,21]

plt.hist(ages)

plt.show()
```

---

## Use Cases

* Salary Distribution
* Age Distribution
* Marks Distribution

---

# 🥧 Pie Chart

Percentage বা Proportion দেখানোর জন্য।

```python
sizes = [40, 30, 20, 10]

labels = [
    "Python",
    "JavaScript",
    "Java",
    "C++"
]

plt.pie(
    sizes,
    labels=labels
)

plt.show()
```

---

## Use Cases

* Market Share
* Budget Allocation
* Survey Results

---

# 📦 Box Plot

Outlier Detection এবং Distribution Analysis-এর জন্য।

```python
data = [10,20,25,30,35,40,100]

plt.boxplot(data)

plt.show()
```

---

## Use Cases

* Statistics
* Data Cleaning
* Outlier Detection

---

# 🔲 Subplots

এক Figure-এর মধ্যে একাধিক Plot।

```python
fig, ax = plt.subplots(2, 2)
```

---

Visual Layout

```text
+---------+---------+
| Plot 1  | Plot 2  |
+---------+---------+
| Plot 3  | Plot 4  |
+---------+---------+
```

---

# 🎨 Plot Customization

Professional Visualization-এর জন্য অত্যন্ত গুরুত্বপূর্ণ।

---

# 📝 Title

```python
plt.title("Monthly Sales Report")
```

---

# 🏷 X Label

```python
plt.xlabel("Month")
```

---

# 🏷 Y Label

```python
plt.ylabel("Sales")
```

---

# 🎨 Colors

```python
plt.plot(
    x,
    y,
    color="red"
)
```

Popular Colors

```text
red
blue
green
yellow
orange
purple
black
```

---

# 📏 Line Width

```python
plt.plot(
    x,
    y,
    linewidth=3
)
```

---

# 〰 Line Styles

Solid

```python
linestyle="-"
```

Dashed

```python
linestyle="--"
```

Dotted

```python
linestyle=":"
```

Dash-Dot

```python
linestyle="-."
```

---

Example

```python
plt.plot(
    x,
    y,
    linestyle="--"
)
```

---

# 🔘 Markers

Data Points Highlight করার জন্য।

```python
plt.plot(
    x,
    y,
    marker="o"
)
```

---

Popular Markers

| Marker | Shape    |
| ------ | -------- |
| o      | Circle   |
| s      | Square   |
| ^      | Triangle |
| *      | Star     |
| x      | Cross    |

---

# 📋 Legend

Multiple Dataset আলাদা করার জন্য।

```python
plt.plot(
    x,
    y,
    label="Sales"
)

plt.legend()
```

---

Multiple Lines Example

```python
plt.plot(
    x,
    y,
    label="2024"
)

plt.plot(
    x,
    z,
    label="2025"
)

plt.legend()
```

---

# 🔲 Grid

Graph আরও Readable করার জন্য।

```python
plt.grid(True)
```

---

# 📐 Figure Size

```python
plt.figure(
    figsize=(10,5)
)
```

---

Meaning

```text
Width  = 10
Height = 5
```

---

# 📸 Save Figure

PNG

```python
plt.savefig(
    "report.png"
)
```

---

PDF

```python
plt.savefig(
    "report.pdf"
)
```

---

# 🎯 Complete Example

```python
import matplotlib.pyplot as plt

months = [
    "Jan",
    "Feb",
    "Mar",
    "Apr"
]

sales = [
    100,
    150,
    120,
    200
]

plt.figure(figsize=(8,5))

plt.plot(
    months,
    sales,
    marker="o",
    linewidth=2,
    label="Sales"
)

plt.title(
    "Monthly Sales Report"
)

plt.xlabel("Month")

plt.ylabel("Sales")

plt.grid(True)

plt.legend()

plt.show()
```

---

# 🌍 Real World Example

Student GPA Analysis

```python
students = [
    "A",
    "B",
    "C",
    "D"
]

gpa = [
    3.2,
    3.8,
    3.5,
    3.9
]

plt.bar(
    students,
    gpa
)

plt.title(
    "Student GPA Analysis"
)

plt.show()
```

---

# 📊 Choosing the Right Plot

| Plot Type    | Best Use Case         |
| ------------ | --------------------- |
| Line Plot    | Trend Analysis        |
| Bar Chart    | Category Comparison   |
| Scatter Plot | Relationship Analysis |
| Histogram    | Distribution Analysis |
| Pie Chart    | Percentage Analysis   |
| Box Plot     | Outlier Detection     |

---

# 💼 Interview Questions

### What is Matplotlib?

Python-এর সবচেয়ে জনপ্রিয় Data Visualization Library।

---

### Difference Between Figure and Axes?

| Figure        | Axes      |
| ------------- | --------- |
| Entire Canvas | Plot Area |

---

### When to Use Scatter Plot?

দুই Variable-এর Relationship দেখানোর জন্য।

---

### What is Histogram?

Data Distribution দেখানোর Graph।

---

### Why Use Legend?

Multiple Dataset Identify করার জন্য।

---

### How to Save a Plot?

```python
plt.savefig("plot.png")
```

---

# 📋 Summary

| Function  | Purpose              |
| --------- | -------------------- |
| plot()    | Line Plot            |
| bar()     | Vertical Bar Chart   |
| barh()    | Horizontal Bar Chart |
| scatter() | Scatter Plot         |
| hist()    | Histogram            |
| pie()     | Pie Chart            |
| boxplot() | Box Plot             |
| title()   | Add Title            |
| xlabel()  | X-axis Label         |
| ylabel()  | Y-axis Label         |
| legend()  | Show Legend          |
| grid()    | Show Grid            |
| savefig() | Save Plot            |

---

# 🎯 Key Takeaways

✅ Matplotlib হলো Python-এর সবচেয়ে জনপ্রিয় Visualization Library।

✅ বিভিন্ন ধরনের Plot বিভিন্ন ধরনের Analysis-এর জন্য ব্যবহার করা হয়।

✅ Professional Visualization-এর জন্য Plot Customization অত্যন্ত গুরুত্বপূর্ণ।

✅ Title, Labels, Legend, Grid এবং Figure Size ব্যবহার করলে Graph অনেক বেশি Readable হয়।

✅ Data Science, Machine Learning, Analytics এবং AI Project-এ Matplotlib একটি Essential Skill।

---

# 🚀 Next Topic

## 📊 Pandas Fundamentals: Series & DataFrame

পরবর্তী অধ্যায়ে শিখবো—

* Pandas Introduction
* Series
* DataFrame
* Reading CSV Files
* Data Exploration
* Filtering & Sorting
* Missing Values Handling

⭐ Happy Data Visualization! 📈🐍🚀
