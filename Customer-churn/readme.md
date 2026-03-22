# Telecom Customer Churn Analysis

## Project Overview

This project explores a telecom customer dataset to understand the
factors associated with customer churn. The goal of the analysis is to
identify patterns and customer behaviors that may indicate a higher
likelihood of churn.

Customer churn is a major concern for telecom companies because
acquiring new customers is often more expensive than retaining existing
ones. By identifying characteristics of customers who churn, businesses
can develop targeted retention strategies.

------------------------------------------------------------------------

## Dataset Description

The dataset contains customer usage and service information. Key
variables include:

-   **Churn** -- Indicates whether the customer left the service (1 =
    churned, 0 = retained)
-   **AccountWeeks** -- Number of weeks the account has been active
-   **ContractRenewal** -- Whether the customer renewed their contract
-   **DataPlan** -- Whether the customer has a data plan
-   **DataUsage** -- Amount of data used
-   **CustServCalls** -- Number of customer service calls made
-   **DayMins** -- Minutes used during the day
-   **DayCalls** -- Number of calls made during the day
-   **MonthlyCharge** -- Monthly billing amount
-   **OverageFee** -- Additional charges for exceeding plan limits
-   **RoamMins** -- Minutes spent roaming

------------------------------------------------------------------------

## Data Cleaning

The following preprocessing steps were performed before analysis:

-   Checked for duplicate records
-   Verified and handled missing values
-   Confirmed correct data types for each column
-   Examined the distribution of the **Churn** variable

These steps ensured the dataset was suitable for exploratory data
analysis.

------------------------------------------------------------------------

## Exploratory Data Analysis (EDA)

The EDA focused on understanding how different customer attributes
relate to churn.

### 1. Churn Distribution

The first step was to examine the balance of churn vs non-churn
customers to understand the dataset composition.

### 2. Contract Renewal vs Churn

A bar chart was used to compare churn rates between customers who
renewed their contracts and those who did not.

**Insight:** Customers without contract renewal tend to show higher
churn rates.

### 3. Monthly Charge vs Churn

A boxplot was used to compare monthly charges between churned and
retained customers.

**Goal:** Determine whether higher billing amounts contribute to churn.

### 4. Customer Service Calls vs Churn

A bar chart was created showing churn rate by the number of customer
service calls.

**Insight:** Customers with more service calls may indicate
dissatisfaction and show higher churn probability.

### 5. Overage Fee vs Churn

A boxplot and average comparison were used to explore whether higher
overage fees are associated with churn.

### 6. Interaction Heatmap

A heatmap combining **Customer Service Calls** and **Overage Fee bands**
was created to identify high-risk customer segments.

This visualization helps reveal how multiple factors interact to
influence churn.

### 7. Correlation Heatmap

A correlation matrix was generated for all numeric features to identify
variables most strongly related to churn.

This helps prioritize features for predictive modeling.

------------------------------------------------------------------------

## Key Insights

Some important patterns explored during the analysis include:

-   Customers who make frequent **customer service calls** may have a
    higher churn risk.
-   Higher **overage fees** may contribute to dissatisfaction and churn.
-   Customers without **contract renewal** may be more likely to leave.
-   Pricing variables such as **monthly charge** may influence churn
    behavior.

------------------------------------------------------------------------

## Tools Used

-   Python
-   Pandas
-   Matplotlib
-   Seaborn

These tools were used for data manipulation, statistical analysis, and
visualization.

------------------------------------------------------------------------

## Future Work

Possible next steps for this project include:

-   Feature engineering for churn prediction
-   Building machine learning models such as:
    -   Logistic Regression
    -   Random Forest
    -   Gradient Boosting
-   Evaluating model performance using metrics such as:
    -   Accuracy
    -   Precision
    -   Recall
    -   ROC-AUC

The goal would be to develop a model capable of predicting which
customers are most likely to churn.

------------------------------------------------------------------------

## Author

Data analysis project developed as part of learning and practicing data
science and exploratory data analysis techniques.
