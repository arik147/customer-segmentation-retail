# 🛒 Customer Behavior Analysis & Segmentation - Retail Transaction Dataset

## 📌 Project Overview

This project explores customer behavior using a retail transaction dataset with over 100,000 rows. The goal is to understand purchasing patterns and segment customers based on behavior to support more effective business decisions.

---

## 🧾 Dataset Description

The dataset contains key features such as:

- `CustomerID`: Unique customer ID  
- `ProductID`: Purchased product  
- `Quantity`, `Price`, `TotalAmount`: Purchase details  
- `DiscountApplied`, `PriceAfterDiscount`: Discounts and final price  
- `TransactionDate`: Transaction timestamp  
- `PaymentMethod`, `StoreLocation`, `ProductCategory`: Additional info  
- Engineered features: `Revenue`, `Segment`, `YearMonth`, and more

---

## 🎯 Goals

- Analyze customer purchasing behavior  
- Compute key behavioral metrics:
  - **Recency** (days since last purchase)  
  - **Total Transactions**  
  - **Total Revenue**  
  - **Average Order Value**
- Perform **behavioral clustering** using K-Means  
- Generate actionable business insights from segmentation

---

## 🔍 Exploratory Data Analysis

Key EDA steps included:

- Distribution of transaction counts per customer  
- Spending distribution  
- Initial segment breakdown  
- Revenue trends over time per segment

---

## 📊 Behavioral Clustering

### 🧠 Behavioral Features

| Feature              | Description                            |
|----------------------|----------------------------------------|
| `Recency`            | Days since last transaction            |
| `TotalTransactions`  | Total transactions per customer        |
| `TotalRevenue`       | Total spending                         |
| `AvgOrderValue`      | Average spend per transaction          |

### 🌀 Clustering Workflow

- Feature standardization using `StandardScaler`  
- Optimal cluster selection using **Elbow Method**  
- Customer segmentation with **KMeans**  
- Cluster visualization using **PCA 2D projection**

### 📋 Cluster Summary

| Cluster | Recency | Transactions | Revenue | Avg Order | Customers |
|---------|---------|--------------|---------|-----------|-----------|
| 0       | 275.6   | 1            | 156.6   | 156.6     | 33,032    |
| 1       | 181.8   | 1            | 504.6   | 504.6     | 24,216    |
| 2       | 118.5   | 2            | 503.2   | 247.2     | 4,621     |
| 3       | 89.1    | 1            | 153.4   | 153.4     | 33,346    |

---

## 💡 Business Insights

- **Big Spenders** and **Frequent Buyers** contributed **47.7%** of total revenue.
- **Champions** had the **highest transaction frequency** (1.34x per customer), signaling strong loyalty potential.
- **Recent Customers** and **Loyal Customers** were engaged and ripe for retention strategies.
- **Others** and **Lost** segments showed lower value, ideal for reactivation campaigns.

---

## 📈 Impact & Strategic Recommendations

- 🎯 **Upsell Campaigns** for Big Spenders and Frequent Buyers → Estimated 10–15% revenue lift
- 🔁 **Retention Programs** for Champions → Encourage repeat purchases
- 🚀 **Welcome Offers** for Recent Customers → Convert to loyal buyers
- ♻️ **Reactivation Strategies** for Lost Customers → Recover dormant users

### 🧮 Simulated Impact

If 20% of **Champions** make an extra purchase:
- ➕ Estimated revenue gain: **Rp540,175**

---

## 🛠️ Tools & Libraries

- Python: `pandas`, `numpy`, `seaborn`, `matplotlib`
- Scikit-Learn: `KMeans`, `StandardScaler`, `PCA`
- Jupyter Notebook

---

## 📂 Folder Structure

```bash
📦 customer-behavior-analysis/
 ┣ 📄 df_segmented.csv
 ┣ 📄 rfm_segmented.csv
 ┣ 📄 retail_analytics.ipynb
 ┣ 📄 retail_explore.ipynb
 ┣ 📄 Retail_Transaction_Dataset.csv
 ┗ 📄 README.md
