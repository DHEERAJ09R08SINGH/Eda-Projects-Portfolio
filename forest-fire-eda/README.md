# 🌲 Forest Fire Dataset — Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the **Forest Fire dataset** to understand how environmental and meteorological conditions influence the occurrence and spread of forest fires.

The goal of this analysis is to identify patterns, relationships, and factors that contribute to forest fire activity using statistical summaries and visualizations.

---

# 📂 Dataset Description

The dataset contains **meteorological and environmental data collected from a forest region**, along with the **burned area caused by fires**.

### Features in Dataset

* **X, Y** — Spatial coordinates within the forest map
* **Month** — Month of the year
* **Day** — Day of the week
* **FFMC** — Fine Fuel Moisture Code
* **DMC** — Duff Moisture Code
* **DC** — Drought Code
* **ISI** — Initial Spread Index
* **Temperature** — Temperature in °C
* **RH** — Relative Humidity (%)
* **Wind** — Wind speed
* **Rain** — Rainfall amount
* **Area** — Burned area of the forest (Target Variable)

---

# 🎯 Objectives

The main objectives of this EDA project are:

* Understand dataset structure
* Analyze environmental conditions influencing forest fires
* Explore distribution of burned areas
* Identify relationships between weather conditions and fire spread
* Visualize patterns using data visualization techniques

---

# 🔎 EDA Steps Performed

### 1️⃣ Data Loading

The dataset was loaded using **Pandas**.

```python
import pandas as pd
df = pd.read_csv("forestfires.csv")
```

---

### 2️⃣ Dataset Overview

Initial exploration was performed using:

* `df.shape`
* `df.info()`
* `df.describe()`

These methods help understand:

* Dataset size
* Data types
* Statistical summary

---

### 3️⃣ Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

Result:

The dataset contains **no significant missing values**.

---

### 4️⃣ Distribution Analysis

Feature distributions were analyzed using:

* Histograms
* KDE plots

Key variables analyzed:

* Temperature
* Relative humidity
* Wind speed
* Burned area

---

### 5️⃣ Burned Area Analysis

The **Area feature** represents the burned forest area.

Observations:

* Burned area distribution is **highly skewed**
* Most fires result in **small burned areas**

---

### 6️⃣ Environmental Factor Analysis

Relationships between environmental variables and burned area were explored.

Examples:

* Temperature vs burned area
* Wind speed vs fire spread
* Humidity vs burned area

Scatter plots and visualizations were used to analyze these relationships.

---

### 7️⃣ Correlation Analysis

A **correlation matrix** was generated to understand relationships between numerical variables.

```python
df.corr()
```

A **heatmap** visualization was used to highlight correlations between environmental factors.

---

# 📊 Data Visualizations

The following visualizations were used in the analysis:

* Feature distribution histograms
* Scatter plots
* Box plots
* Correlation heatmap

These visualizations help reveal hidden relationships within the dataset.

---

# 🔑 Key Insights

Important observations from the analysis include:

* Most forest fires result in **very small burned areas**
* Temperature and wind may contribute to fire spread
* Burned area distribution is **highly skewed**
* Several environmental factors interact to influence fire intensity

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

This project demonstrates the following skills:

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Environmental Data Analysis
* Insight Generation

---

# 🚀 Future Work

Possible future improvements:

* Feature engineering
* Log transformation for skewed variables
* Machine learning models to predict burned area
* Predictive modeling for forest fire risk

---

# 👨‍💻 Author

**Dheeraj R Singh**

Aspiring Data Scientist | Machine Learning Enthusiast



