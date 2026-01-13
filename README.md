# 🚦 Accident Severity Detection using Big Data & Machine Learning

## 📌 Project Description
This project focuses on **predicting traffic accident severity** using large-scale real-world data and Big Data technologies. By leveraging **Apache Spark** and **machine learning**, the system analyzes millions of accident records to identify high-risk situations and support **road safety planning** and **emergency response systems**.

The project is implemented as an **end-to-end Big Data pipeline**, integrating data engineering, analytics, supervised learning, and anomaly detection in a scalable and reproducible manner.

---

## 📊 Dataset
- **Name:** US-Accidents Dataset  
- **Author:** Sobhan Moosavi  
- **Records:** ~4,036,713 traffic accidents  
- **Coverage:** 49 U.S. states  
- **Time Period:** February 2016 – March 2023  
- **Features:**  
  - 46 raw attributes  
  - 51 engineered features  

Due to the size of the dataset, traditional single-machine processing is not feasible. Therefore, **Apache Spark** is used for efficient distributed processing.

---

## ⚙️ Technologies & Tools
- **Apache Spark (PySpark)**
- **Spark SQL**
- **Spark MLlib**
- **Python**
- **Parquet (columnar storage format)**

---

## 🏗️ System Architecture
Raw CSV Data
↓
ETL Pipeline (Apache Spark)
↓
Cleaned & Curated Parquet Data
↓
Spark SQL Analysis
↓
Machine Learning Models
↓
Anomaly Detection
↓
Reports & Insights

---

## 🧹 Data Preprocessing & Feature Engineering
The following preprocessing steps were performed using Apache Spark:
- Dropped columns with high missing values
- Imputed missing numerical values using median
- Filled missing categorical values with `"Unknown"`
- Extracted temporal features (Hour, DayOfWeek, Month)
- Encoded categorical features using `StringIndexer` and `OneHotEncoder`
- Converted boolean road features into numerical format
- Combined all features using `VectorAssembler`

The final dataset was stored in **Parquet format** for scalable analytics and modeling.

---

## 📈 Exploratory Data Analysis (Spark SQL)
Using Spark SQL, large-scale exploratory analysis was conducted to identify:
- Accident distribution by U.S. state
- Temporal patterns by hour of day
- Relationship between weather conditions and accident severity

These insights helped guide feature selection and model design.

---

## 🤖 Machine Learning Models

### 1️⃣ Multi-Class Classification
- **Target Variable:** Accident Severity (1–4)
- **Model:** Logistic Regression (Spark MLlib)
- **Challenge:** Severe class imbalance
- **Solution:** Class-weighted loss function

This model provides **fine-grained severity prediction**, allowing deeper analysis of accident intensity.

---

### 2️⃣ Binary Classification (Extension)
- **Low-Risk:** Severity 1–2  
- **High-Risk:** Severity 3–4  

This formulation improves robustness under extreme class imbalance and is more suitable for **real-time emergency response systems**.

---

## 📊 Model Evaluation
The following metrics were used:
- Accuracy
- Weighted Precision
- Weighted Recall
- F1-Score
- AUC (Area Under Curve)

Weighted metrics were used to ensure fair evaluation across imbalanced severity classes.

---

## 🚨 Anomaly Detection
As an advanced extension, **Z-score based anomaly detection** was applied to numerical features such as:
- Distance
- Weather conditions
- Visibility
- Wind speed
- Precipitation

This step identifies **rare and extreme accident conditions**, which are valuable for risk monitoring and safety planning.

---

## ✅ Key Results
- Identified important **temporal, environmental, and road-related factors** affecting accident severity
- Demonstrated the trade-off between **multi-class detail** and **binary robustness**
- Built a scalable and reproducible **Big Data ETL + ML pipeline**
- Detected rare, high-risk accident events using anomaly detection

---

## 🎯 Applications
- Emergency response prioritization
- Road safety planning
- Traffic risk analysis
- Large-scale accident pattern discovery

---

## 📌 Conclusion
This project demonstrates how **Big Data analytics and machine learning** can be effectively combined to process millions of records and extract actionable insights. The system delivers both **detailed severity analysis** and **robust high-risk detection**, making it suitable for real-world traffic safety applications.

---

## 👨‍💻 Authors
- Mohammad Abu Hantash  
- Ahmad Al-Smadi  

---

## 📄 License
This project is for **academic and educational purposes**.
