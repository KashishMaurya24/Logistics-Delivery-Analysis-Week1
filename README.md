# Food Delivery Logistics Performance Analysis

## 📌 Project Overview

This project analyzes food delivery logistics data to understand the factors affecting delivery time and identify opportunities for improving last-mile delivery efficiency.

The project uses Python and data science techniques including Exploratory Data Analysis (EDA), Key Performance Indicators (KPIs), Linear Regression, K-Means Clustering, and an optimization framework.

The analysis was developed as part of a **Logistics Data Analyst internship project**.

---

## 🎯 Problem Statement

Food delivery operations involve multiple factors such as delivery distance, traffic conditions, weather, vehicle condition, rider workload, and customer ratings.

The objective of this project is to analyze historical delivery data and answer:

> **What factors influence food delivery time, and how can data-driven analysis improve last-mile delivery efficiency?**

---

## 🎯 Objectives

* Analyze historical food delivery data.
* Identify important logistics KPIs.
* Understand factors affecting delivery time.
* Build a regression model for delivery-time prediction.
* Segment deliveries using K-Means clustering.
* Identify high-delay and high-risk delivery segments.
* Develop an optimization framework for resource allocation.
* Provide actionable logistics recommendations.

---

## 📊 Dataset

The project uses a publicly available food delivery dataset containing **38,964 delivery records**.

Important variables include:

* Delivery distance
* Delivery time
* Delivery-person age
* Delivery-person rating
* Weather conditions
* Road traffic density
* Vehicle condition
* Type of vehicle
* Multiple deliveries
* Festival conditions
* City

### Source

[Zomato Delivery EDA Dataset – Hugging Face](https://huggingface.co/datasets/allenborochin/zomato_delivery_EDA)

---

## 📈 Key Performance Indicators

The following KPIs were calculated:

| KPI                       |            Result |
| ------------------------- | ----------------: |
| Average Delivery Time     | **26.58 minutes** |
| Average Delivery Distance |       **9.77 km** |
| Average Delivery Rating   |      **4.63 / 5** |

These KPIs provide a high-level view of delivery performance.

---

## 🔍 Exploratory Data Analysis

EDA was performed to investigate relationships between:

* Delivery distance and delivery time
* Traffic density and delivery time
* Weather conditions and delivery time
* Vehicle type and delivery performance
* City and delivery time
* Multiple deliveries and delivery time

The analysis showed that delivery performance depends on multiple operational factors rather than distance alone.

---

## 🤖 Predictive Modeling

### Simple Linear Regression

The first model used only delivery distance to predict delivery time.

| Metric |           Result |
| ------ | ---------------: |
| R²     |       **0.1084** |
| MAE    | **7.07 minutes** |
| RMSE   | **8.71 minutes** |

The low R² showed that distance alone was not sufficient for reliable delivery-time prediction.

### Multiple Linear Regression

The second model incorporated multiple operational and environmental variables.

| Metric |           Result |
| ------ | ---------------: |
| R²     |       **0.5903** |
| MAE    | **4.69 minutes** |
| RMSE   | **5.90 minutes** |

The multiple regression model performed substantially better than the simple distance-based model.

### Key Insight

Delivery time is influenced by a combination of factors including traffic, weather, workload, vehicle condition, distance, and other operational variables.

---

## 🔵 K-Means Clustering

K-Means clustering was applied using:

* Distance
* Delivery time
* Delivery-person rating

The Elbow Method was used to determine the appropriate number of clusters, resulting in **5 clusters**.

| Cluster | Distance | Delivery Time | Rating |
| ------- | -------: | ------------: | -----: |
| 0       |  6.14 km |     28.03 min |   4.72 |
| 1       | 14.82 km |     40.89 min |   4.69 |
| 2       |  5.07 km |     16.80 min |   4.74 |
| 3       | 15.42 km |     22.51 min |   4.75 |
| 4       | 11.43 km |     36.22 min |   4.01 |

### Important Findings

**Cluster 1** represents the highest-delay segment, with an average delivery time of **40.89 minutes**.

**Cluster 2** represents the fastest segment, averaging **16.80 minutes**.

**Cluster 4** has a relatively high delivery time and the lowest average rating of **4.01**.

An important observation is that Cluster 3 has the longest average distance (**15.42 km**) but a relatively low delivery time (**22.51 minutes**). This demonstrates that distance alone does not determine delivery performance.

---

## ⚙️ Optimization Framework

An optimization framework was proposed with the following objectives:

* Minimize delivery time
* Reduce transportation cost
* Improve rider/resource utilization
* Prioritize high-delay delivery segments

Possible constraints include:

* Limited delivery riders
* Vehicle availability
* Delivery distance
* Traffic conditions
* Delivery capacity

The analysis can support future route optimization and resource-allocation systems.

---

## 💡 Business Recommendations

Based on the analysis:

1. **Prioritize high-delay segments** such as Cluster 1 for improved resource allocation.
2. **Investigate low-rating/high-time deliveries** represented by Cluster 4.
3. **Study high-performing deliveries** in Cluster 2 to identify efficient operational practices.
4. Avoid making resource decisions based only on distance.
5. Consider traffic, weather, workload, vehicle condition, and other operational factors during delivery planning.
6. Use predictive analytics as a decision-support tool for delivery-time estimation.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab
* GitHub

---

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
KPI Calculation
      ↓
Feature Engineering
      ↓
Regression Modeling
      ↓
K-Means Clustering
      ↓
Optimization Framework
      ↓
Business Recommendations
```

---

## 📁 Project Structure

```text
food-delivery-logistics-analysis/
│
├── Logistics_Delivery_Analysis.ipynb
├── README.md
├── data/
├── images/
├── report/
└── requirements.txt
```

---

## 📌 Expected Impact

This project provides a data-driven framework that can help logistics organizations:

* identify delivery bottlenecks
* improve delivery-time prediction
* identify high-risk delivery segments
* improve rider and vehicle allocation
* support route and resource planning
* improve operational efficiency
* enhance customer service

---

## 🚀 Future Improvements

Future versions of the project could include:

* Real-time traffic data
* GPS-based route optimization
* Advanced machine-learning models such as Random Forest and XGBoost
* Real-time delivery-time prediction
* Interactive Streamlit dashboard
* Automated monitoring of logistics KPIs
* Integration with live delivery data

---

## 👩‍💻 Author

**Kashish Maurya**
B.Tech – Artificial Intelligence & Machine Learning
IIMT University, Meerut

---

## 📄 Project Context

This project was developed as part of a **Logistics Data Analyst internship project with Yuva Intern**, with the objective of applying data science techniques to a practical logistics problem.
