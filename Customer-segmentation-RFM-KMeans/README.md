# 📊 Customer Segmentation Using RFM Analysis & K-Means Clustering

## 🧠 Project Summary

This project applies **RFM (Recency, Frequency, Monetary) analysis** combined with **K-Means clustering** to segment customers based on purchasing behavior. The goal is to identify meaningful customer groups to support targeted marketing strategies and improve customer retention.

---

## 🎯 Problem Statement

Businesses often struggle to understand:

* Who are their most valuable customers?
* Which customers are at risk of leaving?
* Which customers should be targeted for promotions or loyalty programs?

This project solves that by grouping customers based on their transaction behavior.

---

## 📦 Dataset

* Source: Online Retail dataset
* Contains transactional data including:

  * Invoice number
  * Customer ID
  * Quantity
  * Unit price
  * Invoice date

---

## 🧹 Data Cleaning Steps

* Removed missing `CustomerID` values
* Removed cancelled transactions (negative quantities)
* Removed invalid pricing (zero or negative unit price)
* Created a new feature:

  * `TotalPrice = Quantity × UnitPrice`

---

## 🧱 Feature Engineering (RFM)

Customers were aggregated into:

* **Recency** → Days since last purchase
* **Frequency** → Number of purchases
* **Monetary** → Total spending

---

## 🔄 Data Transformation

To prepare data for clustering:

* Applied log transformation:

  * `log1p(Frequency)`
  * `log1p(Monetary)`
* Standardized features using `StandardScaler`

Final clustering features:

* Recency
* LogFrequency
* LogMonetary

---

## 🤖 Model: K-Means Clustering

* Used K-Means algorithm to segment customers
* Optimal number of clusters determined using the **Elbow Method**
* Final chosen value: **k = 4**

---

## 📈 Elbow Method Result

* Tested k values from 1 to 10
* Plotted inertia vs number of clusters
* Selected point where improvement slowed significantly

---

## 🧩 Customer Segments

After clustering, customers were grouped and analyzed:

### 🔵 Cluster 0 — Low-Value / Occasional Customers

* High Recency (inactive for long)
* Low Frequency
* Low Monetary value

👉 Action: Low-priority marketing

---

### 🟢 Cluster 1 — Regular Customers

* Moderate Recency
* Moderate Frequency
* Moderate Monetary value

👉 Action: Engagement campaigns, upselling

---

### 🟡 Cluster 2 — Loyal Customers

* Low Recency
* High Frequency
* Good Monetary value

👉 Action: Loyalty programs, retention focus

---

### 🔴 Cluster 3 — VIP Customers (Champions)

* Very low Recency (recent buyers)
* High Frequency
* Very high Monetary value

👉 Action: Reward, retain, premium offers

---

## 📊 Visualization

Key plot used:

* **Recency vs Monetary scatter plot**
* Color-coded by cluster

This clearly shows:

* High-value active customers
* At-risk customers
* Low-value customers

---

## 💡 Key Insights

* A small group of customers contributes a large portion of revenue
* Many customers are inactive and may need re-engagement campaigns
* VIP customers are highly valuable and should be prioritized for retention

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📌 Project Workflow

Data Cleaning
→ RFM Feature Engineering
→ Log Transformation
→ Scaling
→ Elbow Method
→ K-Means Clustering
→ Cluster Profiling
→ Business Interpretation

---

## 🚀 How to Run the Project

clone the repository
cd Customer-segmentation-RFM-KMeans
pip install -r requirements.txt
jupyter notebook
