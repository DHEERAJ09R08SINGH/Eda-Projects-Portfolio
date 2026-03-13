# 📱 Google Playstore Dataset — Exploratory Data Analysis & Feature Engineering

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** and **Feature Engineering (FE)** on the **Google Playstore dataset** to understand trends in mobile applications available on the Play Store.

The analysis focuses on exploring app categories, ratings, installs, pricing models, and other factors that influence app popularity.

The dataset was cleaned and transformed to make it suitable for further machine learning analysis.

---

# 📂 Dataset Description

The dataset contains information about applications available on the Google Play Store.

### Key Features

* **App** — Application name
* **Category** — App category (e.g., Games, Education, Business)
* **Rating** — User rating of the app
* **Reviews** — Number of user reviews
* **Size** — Application size
* **Installs** — Number of installs
* **Type** — Free or Paid app
* **Price** — Price of the application
* **Content Rating** — Age suitability of the app
* **Genres** — App genre
* **Last Updated** — Last update date
* **Current Version** — Current version of the app
* **Android Version** — Minimum Android version required

---

# 🎯 Objectives

The main objectives of this project are:

* Explore distribution of apps across categories
* Analyze relationship between ratings and installs
* Compare free and paid applications
* Perform data cleaning and feature engineering
* Identify trends affecting app popularity

---

# 🔎 EDA Steps Performed

### 1️⃣ Data Loading

The dataset was loaded using **Pandas**.

```python
import pandas as pd
df = pd.read_csv("googleplaystore.csv")
```

---

### 2️⃣ Dataset Overview

Basic dataset inspection was performed using:

* `df.shape`
* `df.info()`
* `df.describe()`

This step helps understand dataset structure and statistics.

---

### 3️⃣ Data Cleaning

Several columns required cleaning and conversion:

* **Installs column**

  * Removed `+` and `,`
  * Converted to numeric values

* **Price column**

  * Removed `$` symbol
  * Converted to numeric format

Example transformation:

```python
df['Installs'] = df['Installs'].str.replace('+','').str.replace(',','')
df['Installs'] = df['Installs'].astype(int)
```

---

### 4️⃣ Missing Value Handling

Missing values were identified and handled appropriately.

```python
df.isnull().sum()
```

Rows with significant missing values were cleaned or removed.

---

### 5️⃣ Feature Engineering

New useful features were derived from existing columns such as:

* Updated date features
* Cleaned numerical variables
* Converted categorical variables

These transformations help prepare the dataset for modeling.

---

### 6️⃣ Category Analysis

The distribution of apps across categories was analyzed.

Observations help identify **most popular app categories**.

---

### 7️⃣ Rating vs Installs Analysis

Scatter plots were used to analyze the relationship between:

* App rating
* Number of installs

This helps identify patterns in **user engagement and popularity**.

---

### 8️⃣ Free vs Paid Apps Analysis

Apps were compared based on **pricing models**.

Key analysis included:

* Free vs Paid app distribution
* Price vs installs relationship

---

### 9️⃣ Correlation Analysis

A correlation matrix was used to identify relationships between numerical features.

Heatmaps were used for visualization.

---

# 📊 Data Visualizations

The following visualizations were used during analysis:

* Category distribution charts
* Rating distribution plots
* Rating vs installs scatter plots
* Free vs paid apps comparison
* Correlation heatmap

These visualizations help reveal important patterns in the dataset.

---

# 🔑 Key Insights

Important findings from the analysis include:

* **Free apps dominate the Playstore** and have significantly higher installs.
* Certain categories such as **Games and Tools** have the highest number of apps.
* Higher rated apps often receive **more installs**.
* Paid apps generally have **lower install counts compared to free apps**.

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

This project demonstrates the following data science skills:

* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis
* Data Visualization
* Handling messy real-world datasets
* Insight extraction

---

# 🚀 Future Work

Potential next steps include:

* Predicting app success using machine learning
* Recommendation systems for apps
* Advanced feature engineering
* Interactive dashboards for Playstore analytics

---

# 👨‍💻 Author

**Dheeraj R Singh**

Aspiring Data Scientist | Machine Learning Enthusiast



