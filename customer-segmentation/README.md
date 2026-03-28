# Customer Segmentation Analysis

## Project Overview

This project analyzes mall customer data to identify distinct customer segments based on their spending behavior. The goal is to help the mall develop targeted marketing strategies by understanding different types of shoppers.

Using **Exploratory Data Analysis (EDA)** and **K-Means Clustering**, customers are grouped according to their **Annual Income** and **Spending Score**. These segments reveal patterns in purchasing behavior that can guide business decisions such as promotions, loyalty programs, and personalized marketing campaigns.

---

## Business Objective

The objective of this analysis is to segment mall customers based on their spending behavior in order to guide marketing strategies and improve customer engagement.

Key questions addressed in this project include:

* Do customers with higher income spend more?
* Are there identifiable groups of customers with similar shopping behaviors?
* Which customer segments are most valuable to the mall?

By answering these questions, the mall can tailor marketing campaigns to different customer groups and maximize revenue.

---

## Dataset

The dataset contains information about mall customers, including demographic details and purchasing behavior.

### Features

| Feature                | Description                                                    |
| ---------------------- | -------------------------------------------------------------- |
| CustomerID             | Unique identifier for each customer                            |
| Gender                 | Male or Female                                                 |
| Age                    | Age of the customer                                            |
| Annual Income (k$)     | Customer's yearly income                                       |
| Spending Score (1–100) | Score assigned by the mall based on customer spending behavior |

For clustering purposes, the most relevant features are:

* **Annual Income**
* **Spending Score**

These variables capture a customer's **purchasing power** and **spending behavior**, which are essential for meaningful segmentation.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## Project Workflow

### 1. Data Exploration

Initial exploration was performed to understand the dataset structure.

Key steps:

* Checked dataset shape and data types
* Verified presence of missing values
* Generated summary statistics

---

### 2. Exploratory Data Analysis (EDA)

Several visualizations were used to understand the distribution of variables and relationships between them.

#### Univariate Analysis

Histograms were used to explore the distributions of:

* Age
* Annual Income
* Spending Score

A bar chart was used to analyze the distribution of **Gender**.

#### Bivariate Analysis

Scatter plots and box plots were used to explore relationships between variables, including:

* **Annual Income vs Spending Score**
* **Age vs Spending Score**
* **Gender vs Spending Score**

These visualizations revealed patterns suggesting that meaningful customer groups might exist in the dataset.

---

### 3. Feature Selection

For clustering, the following features were selected:

* **Annual Income**
* **Spending Score**

These variables directly represent customer **purchasing capacity** and **spending behavior**, making them ideal for segmentation.

The **CustomerID** column was excluded since it serves only as a unique identifier and does not provide analytical value.

---

### 4. Feature Scaling

Since K-Means is a **distance-based algorithm**, feature scaling was applied to ensure that variables with larger ranges (such as income) do not dominate the clustering process.

Standardization was applied so that each feature contributes equally to the clustering algorithm.

---

### 5. Determining the Optimal Number of Clusters

The **Elbow Method** was used to determine the optimal number of clusters (K).

The analysis suggested that **K = 5** provides a good balance between model simplicity and cluster separation.

---

### 6. K-Means Clustering

The K-Means algorithm was applied to group customers into clusters based on their income and spending behavior.

The clustering results were visualized using a scatter plot, where each color represents a different customer segment.

---

### 7. Cluster Profiling

After clustering, a **cluster profile table** was created by calculating the average values of key variables for each cluster.

This helped interpret the segments and assign meaningful business labels.

| Segment           | Persona                       | Marketing Strategy                                                     |
| ----------------- | ----------------------------- | ---------------------------------------------------------------------- |
| Luxury Shoppers   | Wealthy frequent buyers       | Offer VIP services and premium experiences                             |
| Careful Wealthy   | Wealthy but occasional buyers | Promote convenience services such as online shopping and home delivery |
| Young Impulsive   | Impulse-driven buyers         | Use limited-time promotions and flash sales                            |
| Budget Customers  | Price-conscious shoppers      | Offer discounts and budget deals                                       |
| Average Customers | Moderate income and spending  | Encourage loyalty through rewards programs                             |

---

## Key Insights

* Customers can be clearly segmented based on **income and spending behavior**.
* High-income customers with high spending scores represent the most valuable segment.
* High-income customers with low spending scores represent a **growth opportunity** for targeted marketing campaigns.
* Young customers tend to display more impulsive purchasing behavior.

These insights allow businesses to tailor marketing strategies for different customer segments.

---

## Future Improvements

Potential extensions of this project include:

* Incorporating **Age** into the clustering model to explore age-based behavioral segments
* Testing additional clustering algorithms such as **Hierarchical Clustering** or **DBSCAN**
* Performing deeper behavioral analysis using additional customer data

---

## How to Run the Project

1. Clone the repository
2. Install required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Launch Jupyter Notebook:

```bash
jupyter notebook
```

4. Open the notebook and run the cells to reproduce the analysis.

---

## Author

Rosemary Njoroge

This project is part of my **data science portfolio**, demonstrating skills in:

* Exploratory Data Analysis
* Data Visualization
* Customer Segmentation
* Unsupervised Machine Learning
