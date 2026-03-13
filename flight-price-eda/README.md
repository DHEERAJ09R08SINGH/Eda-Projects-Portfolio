# ✈️ Flight Price Dataset — Exploratory Data Analysis & Feature Engineering

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** and **Feature Engineering (FE)** on a flight price dataset to understand the factors influencing airline ticket prices.

Airline ticket prices vary depending on several factors such as airline, journey date, duration, stops, and departure time. Through EDA and visualization, this project identifies patterns and relationships that affect flight pricing.

The analysis also includes **feature engineering techniques** to prepare the dataset for machine learning models.

---

# 📂 Dataset Description

The dataset contains information about flights including airline details, journey information, and ticket prices.

### Key Features

* **Airline** — Name of the airline company
* **Date_of_Journey** — Date of travel
* **Source** — Departure city
* **Destination** — Arrival city
* **Route** — Flight route
* **Dep_Time** — Departure time
* **Arrival_Time** — Arrival time
* **Duration** — Total travel duration
* **Total_Stops** — Number of stops in the journey
* **Additional_Info** — Extra flight information
* **Price** — Ticket price (Target Variable)

---

# 🎯 Objectives

The main objectives of this project are:

* Explore flight price distribution
* Identify factors affecting airline ticket prices
* Perform data cleaning and preprocessing
* Extract new features from date and time columns
* Prepare dataset for machine learning models

---

# 🔎 EDA Steps Performed

### 1️⃣ Data Loading

The dataset was loaded using **Pandas**.

```python
import pandas as pd
df = pd.read_excel("flight_price.xlsx")
```

---

### 2️⃣ Dataset Overview

Initial exploration was performed using:

* `df.shape`
* `df.info()`
* `df.describe()`

These functions help understand dataset structure and statistics.

---

### 3️⃣ Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

Rows containing missing values were handled appropriately.

---

### 4️⃣ Feature Engineering

Several new features were extracted from date and time columns.

Examples include:

* **Journey Day**
* **Journey Month**
* **Departure Hour**
* **Departure Minute**
* **Arrival Hour**
* **Arrival Minute**

Example code:

```python
df["Journey_day"] = pd.to_datetime(df["Date_of_Journey"]).dt.day
df["Journey_month"] = pd.to_datetime(df["Date_of_Journey"]).dt.month
```

---

### 5️⃣ Duration Processing

Flight duration was split into:

* Duration hours
* Duration minutes

This helps machine learning models better interpret travel time.

---

### 6️⃣ Categorical Feature Analysis

Categorical variables such as:

* Airline
* Source
* Destination
* Total Stops

were analyzed using visualizations.

---

### 7️⃣ Price Distribution Analysis

Price distribution was visualized to understand the spread and identify possible outliers.

---

### 8️⃣ Correlation Analysis

Correlation analysis was performed to understand relationships between features.

Heatmaps were used to visualize correlations.

---

# 📊 Data Visualizations

Several visualizations were used during analysis:

* Airline vs Price boxplots
* Source vs Price analysis
* Stops vs Ticket Price
* Price distribution plots
* Correlation heatmap

These visualizations help reveal patterns affecting flight pricing.

---

# 🔑 Key Insights

Important findings from the analysis:

* Flights with **more stops tend to have lower prices**.
* **Airline choice significantly impacts ticket price**.
* **Flight duration influences ticket price**.
* Certain routes have consistently higher prices.

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
* Handling Date & Time Features
* Preparing data for Machine Learning

---

# 🚀 Future Work

Possible next steps:

* One-hot encoding categorical features
* Feature scaling
* Training machine learning models for flight price prediction
* Model evaluation and optimization

---

# 👨‍💻 Author

**Dheeraj R Singh**

Aspiring Data Scientist | Machine Learning Enthusiast


