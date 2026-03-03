Student Performance Analysis & Data Analysis Foundations




Author: David Eniola

Course: Statistics
Goal: Build a strong foundation in Python and data analysis for real-world datasets

Project Overview

This project is part of my journey to become job-ready in Data Analysis.
It focuses on:

Python programming basics

Handling student datasets

Detecting and managing missing data

Transitioning to pandas for real-world data analysis

1️⃣ Python Basics
Variables and Data Types
name = "David"
course = "Statistics"
graduation_year = 2026
CGPA = 3.56
Whether_you_like_statistics = True
Printing Information
print(f"My name is {name}")
print(f"I am studying {course}")
print(f"I will graduate in {graduation_year}")
print(f"My CGPA is {CGPA + 0.25}")
print(f"Do I love statistics? {Whether_you_like_statistics}")
Conditional Statements
marks = 80
if marks >= 70:
    performance = "Excellent Performance"
elif marks >= 50:
    performance = "Good Performance"
else:
    performance = "Needs Improvement"

print(performance)
Loops
for i in range(1, 11):
    if i % 2 == 0:
        print(f"{i} is Even")
    else:
        print(f"{i} is Odd")
2️⃣ Student Data Project (Python)
Sample Dataset
students = [
    {"name": "John", "marks": 80, "hours": 12},
    {"name": "Mary", "marks": 65, "hours": 8},
    {"name": "Tom", "marks": 75}  # missing hours
]
Handling Missing Data
for student in students:
    marks = student.get("marks", 0)
    hours = student.get("hours", 0)

    if marks >= 70 and hours >= 10:
        print(f"{student['name']} is a High Performer")
    else:
        print(f"{student['name']} is not a High Performer")
Detecting Missing Values
missing_hours = 0
for student in students:
    if "hours" not in student:
        missing_hours += 1

print("Students missing hours:", missing_hours)
3️⃣ Introduction to Pandas
Create a DataFrame
import pandas as pd

data = {
    "name": ["John", "Mary", "Tom"],
    "marks": [80, 65, 75],
    "hours": [12, 8, None]  # None = missing
}

df = pd.DataFrame(data)
print(df)
Basic Analysis
# Average marks
print(df["marks"].mean())

# Average hours (ignores missing values)
print(df["hours"].mean())

# Count missing values
print(df.isnull().sum())

# Filter high performers
high_performers = df[(df["marks"] >= 70) & (df["hours"] >= 10)]
print(high_performers)
4️⃣ Missing Data Concepts
Type	Description	Safe to Delete?
MCAR	Missing completely at random	✅ Yes
MAR	Missing at random (depends on other variables)	⚠️ Often impute
MNAR	Missing not at random (depends on missing value itself)	❌ Do not delete
5️⃣ Key Takeaways

Python basics (variables, loops, conditions) are crucial for analysis

Handling missing data is critical to avoid bias

Pandas simplifies data cleaning and analysis

Understanding missing data types prevents biased conclusions

6️⃣ Next Steps

Load CSV datasets into pandas

Clean missing data with imputation

Explore data visualization (matplotlib / seaborn)

Apply statistical analysis on real datasets

7️⃣ Author

David Eniola
Final-Year Statistics Student
Building a strong foundation in Data Analysis 🚀# 📊 Student Performance Analysis (Python + Pandas)

## 📌 Project Overview

This project is part of my journey to build a strong foundation in **Data Analysis** as a final-year Statistics student.

The goal of this project is to:

* Practice core Python programming
* Understand data structures (lists, dictionaries)
* Handle missing data properly
* Transition from basic Python to **pandas**
* Think like a real data analyst

---

## 🚀 What This Project Covers

### 1️⃣ Basic Python Foundations

* Loops (`for`)
* Conditional statements (`if/else`)
* Dictionaries
* Error handling
* Using `.get()` to safely access dictionary values

### 2️⃣ Handling Missing Data

* Detecting missing keys in dictionaries
* Avoiding `KeyError`
* Understanding `None` values
* Counting missing values

### 3️⃣ Introduction to Pandas

* Creating a DataFrame
* Calculating averages using `.mean()`
* Detecting missing values using `.isnull()`
* Filtering data using conditions
* Understanding how pandas handles `NaN`

---

## 🧠 Example Dataset

```python
data = {
    "name": ["John", "Mary", "Tom"],
    "marks": [80, 65, 75],
    "hours": [12, 8, None]
}
```

This dataset includes:

* Student names
* Exam marks
* Study hours (with missing data)

---

## 📊 Key Analysis Performed

* Calculated average marks
* Identified high-performing students
* Counted missing values
* Explored how pandas treats `NaN`
* Compared different ways to handle missing data

---

## 🎯 What I Learned

* Python is case-sensitive (`DataFrame` ≠ `Dataframe`)
* Missing data is not the same as zero
* Pandas ignores `NaN` values in calculations by default
* Data quality directly affects statistical results
* Defensive coding prevents crashes

---

## 🛠 Technologies Used

* Python
* Pandas

---

## 📈 Next Steps

* Load data from CSV files
* Perform data cleaning
* Add visualizations
* Apply statistical analysis techniques
* Build more real-world datasets

---

## 👨‍🎓 Author

David Eniola
Final-Year Statistics Student
Building a strong fou
