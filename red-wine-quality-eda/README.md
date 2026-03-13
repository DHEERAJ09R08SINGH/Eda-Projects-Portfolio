# 🍷 Red Wine Quality Dataset — Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the Red Wine Quality dataset to understand the relationships between different physicochemical properties of wine and the resulting wine quality score.

EDA helps uncover patterns, detect anomalies, and identify relationships between variables before applying machine learning models.

---

# 📂 Dataset Information

Source:
UCI Machine Learning Repository
Wine Quality Dataset

The dataset contains **chemical properties of red wine samples** and a **quality rating** between **0 and 10**.

### Features in Dataset

* Fixed Acidity
* Volatile Acidity
* Citric Acid
* Residual Sugar
* Chlorides
* Free Sulfur Dioxide
* Total Sulfur Dioxide
* Density
* pH
* Sulphates
* Alcohol
* Quality (Target Variable)

---

# 🎯 Objectives

The goals of this EDA project are:

* Understand dataset structure
* Analyze feature distributions
* Detect missing values and duplicates
* Explore relationships between features
* Identify correlations affecting wine quality

---

# 🔍 EDA Steps Performed

### 1️⃣ Data Loading

The dataset was loaded using **Pandas**.

```python
import pandas as pd
df = pd.read_csv("winequality-red.csv")
```

---

### 2️⃣ Dataset Overview

Basic dataset exploration was performed using:

* `df.info()`
* `df.describe()`
* `df.shape`
* `df.columns`

These functions help understand:

* Number of rows and columns
* Data types
* Statistical summary

---

### 3️⃣ Target Variable Analysis

Unique values in the **quality column** were examined.

```python
df['quality'].unique()
```

Class distribution was analyzed using:

```python
df['quality'].value_counts()
```

This helps determine if the dataset is **balanced or imbalanced**.

---

### 4️⃣ Missing Values Check

Missing values were checked using:

```python
df.isnull().sum()
```

✅ Result:

No missing values were found in the dataset.

---

### 5️⃣ Duplicate Records

Duplicate rows were identified.

```python
df[df.duplicated()]
```

Approximately **240 duplicate records** were found.

Duplicates were removed:

```python
df.drop_duplicates(inplace=True)
```

---

### 6️⃣ Correlation Analysis

Feature relationships were analyzed using a **correlation matrix**.

```python
df.corr()
```

A **heatmap visualization** helps identify strong correlations between variables.

Example insight:

* Alcohol tends to have a **positive relationship with wine quality**.

---

# 📊 Data Visualization

Several visualizations were created to understand feature distributions and relationships.

---

### 📈 Target Variable Distribution

Bar chart showing distribution of wine quality ratings.

```python
df['quality'].value_counts().plot(kind='bar')
```

---

### 📉 Feature Distribution

Histograms and KDE plots were used to analyze distributions.

Examples:

* Fixed Acidity distribution
* Alcohol distribution
* Residual Sugar distribution

```python
sns.histplot(df['fixed acidity'], kde=True)
```

---

### 📦 Box Plot Analysis

Boxplot used to study relationship between **alcohol and quality**.

```python
sns.catplot(x='quality', y='alcohol', data=df, kind='box')
```

Insight:

Higher alcohol content tends to be associated with higher wine quality.

---

### 🔗 Feature Relationship Visualization

Scatter plots were used to examine relationships between variables.

Example:

```python
sns.scatterplot(x='alcohol', y='pH', hue='quality', data=df)
```

This helps visualize how **feature interactions affect wine quality**.

---

# 🔑 Key Insights

Some important observations from the analysis:

* Alcohol content shows a **positive relationship with wine quality**.
* Some features have **skewed distributions**.
* The dataset contained **duplicate records which were removed**.
* Several variables show **moderate correlations with the target variable**.

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

* Data Cleaning
* Duplicate Handling
* Exploratory Data Analysis
* Data Visualization
* Correlation Analysis
* Insight Generation

---

# 🚀 Future Work

Possible next steps:

* Feature engineering
* Feature scaling
* Machine Learning model building
* Wine quality prediction models

---

# 👨‍💻 Author

**Dheeraj R Singh**

Aspiring Data Scientist | Machine Learning Enthusiast



