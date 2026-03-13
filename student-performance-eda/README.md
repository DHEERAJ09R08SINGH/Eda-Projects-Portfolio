# 🎓 Student Performance Indicator — Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the Student Performance dataset to understand the factors that influence students' academic results.

The analysis focuses on exploring relationships between demographic factors, study-related variables, and students’ exam scores.

EDA helps identify patterns, correlations, and trends that may affect student performance.

---

# 📂 Dataset Description

The dataset contains information about students including demographic details, study habits, and exam scores.

### Key Features

* Gender
* Race/Ethnicity
* Parental Level of Education
* Lunch Type
* Test Preparation Course
* Math Score
* Reading Score
* Writing Score

Target variables are the **student scores in different subjects**.

---

# 🎯 Objectives

The main goals of this project are:

* Understand the dataset structure
* Analyze distribution of student scores
* Identify relationships between demographic features and performance
* Explore correlations between subjects
* Visualize patterns in student achievement

---

# 🔎 EDA Steps Performed

### 1️⃣ Data Loading

The dataset was loaded using **Pandas**.

```python
import pandas as pd
df = pd.read_csv("StudentsPerformance.csv")
```

---

### 2️⃣ Dataset Overview

Initial inspection of the dataset was performed using:

* `df.shape`
* `df.info()`
* `df.describe()`

This step helps understand:

* Number of records
* Data types
* Statistical summary

---

### 3️⃣ Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

Result:

No significant missing values were found in the dataset.

---

### 4️⃣ Score Distribution Analysis

The distribution of scores was analyzed using **histograms and density plots**.

Visualizations help understand:

* Score spread
* Skewness in distribution
* Average performance level

---

### 5️⃣ Feature Relationship Analysis

Relationships between variables were explored using visualizations such as:

* Box plots
* Bar charts
* Scatter plots

Examples:

* Gender vs student scores
* Parental education vs student performance
* Lunch type vs scores

---

### 6️⃣ Correlation Analysis

Correlation analysis was performed to examine relationships between numeric features.

```python
df.corr()
```

Key correlations were visualized using **heatmaps**.

---

# 📊 Data Visualizations

The following visualizations were used in the analysis:

* Score distribution plots
* Gender vs score boxplots
* Feature comparison charts
* Correlation heatmap

These visualizations help identify **patterns and relationships within the dataset**.

---

# 🔑 Key Insights

Important observations from the analysis include:

* Students who completed **test preparation courses tend to score higher**.
* **Parental education level** shows some influence on student performance.
* Scores in **math, reading, and writing are strongly correlated**.
* Performance distribution varies across demographic groups.

---

# 🛠 Tools & Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# 📊 Skills Demonstrated

* Data cleaning
* Exploratory Data Analysis
* Data visualization
* Correlation analysis
* Insight generation

---

# 🚀 Future Work

Potential next steps include:

* Feature engineering
* Predictive modeling
* Student performance prediction using machine learning

---

# 👨‍💻 Author

**Dheeraj R Singh**

Aspiring Data Scientist | Machine Learning Enthusiast

