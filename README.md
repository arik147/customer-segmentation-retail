# 🛒 Customer Behavior Analysis & Segmentation - Retail Transaction Dataset

## 📌 Project Overview

Dalam proyek ini, dilakukan analisis perilaku pelanggan menggunakan dataset transaksi ritel berisi lebih dari 100.000 baris data. Tujuannya adalah memahami pola pembelian pelanggan dan membagi mereka ke dalam segmen-segmen berbasis perilaku untuk mendukung keputusan bisnis yang lebih tepat.

---

## 🧾 Dataset Description

Dataset transaksi pelanggan terdiri dari fitur-fitur utama berikut:

- `CustomerID`: ID unik pelanggan  
- `ProductID`: Produk yang dibeli  
- `Quantity`, `Price`, `TotalAmount`: Detail pembelian  
- `DiscountApplied`, `PriceAfterDiscount`: Diskon dan harga akhir  
- `TransactionDate`: Tanggal dan waktu transaksi  
- `PaymentMethod`, `StoreLocation`, `ProductCategory`: Info tambahan  
- Fitur turunan: `Revenue`, `Segment`, `YearMonth`, dll.

---

## 🎯 Goals

- Menganalisis perilaku pembelian pelanggan
- Menghitung metrik perilaku utama seperti:
  - **Recency** (berapa lama sejak pembelian terakhir)
  - **Total Transactions**
  - **Total Revenue**
  - **Average Order Value**
- Melakukan **behavioral clustering** menggunakan K-Means
- Memberikan insight bisnis berdasarkan hasil segmentasi

---

## 🔍 Exploratory Data Analysis

Beberapa langkah EDA yang dilakukan:

- Distribusi jumlah transaksi per pelanggan  
- Distribusi total pengeluaran  
- Segmentasi awal berdasarkan label `Segment`  
- Visualisasi time series revenue per segmen

---

## 📊 Behavioral Clustering

### 🧠 Fitur Perilaku Pelanggan

| Fitur | Deskripsi |
|-------|-----------|
| `Recency` | Hari sejak transaksi terakhir |
| `TotalTransactions` | Total transaksi per pelanggan |
| `TotalRevenue` | Total pengeluaran |
| `AvgOrderValue` | Rata-rata pengeluaran per transaksi |

### 🌀 Clustering Workflow

- Data standardization (StandardScaler)
- Menentukan jumlah cluster optimal dengan Elbow Method
- Clustering dengan **KMeans**
- Visualisasi hasil dengan **PCA 2D plot**

### 📋 Cluster Summary

| Cluster | Recency | Transactions | Revenue | Avg Order | Jumlah Customer |
|---------|---------|--------------|---------|-----------|------------------|
| 0 | 275.6 | 1 | 156.6 | 156.6 | 33,032 |
| 1 | 181.8 | 1 | 504.6 | 504.6 | 24,216 |
| 2 | 118.5 | 2 | 503.2 | 247.2 | 4,621 |
| 3 | 89.1 | 1 | 153.4 | 153.4 | 33,346 |

---

## 💡 Business Insights

- **Cluster 1**: Big spenders – jarang beli tapi nilai tinggi  
- **Cluster 2**: Pelanggan loyal – transaksi sering dan revenue tinggi  
- **Cluster 3**: Pelanggan baru – potensial untuk di-retain  
- **Cluster 0**: Pelanggan pasif – kandidat untuk retargeting

---

## 🛠️ Tools & Libraries

- Python: Pandas, NumPy, Seaborn, Matplotlib  
- Scikit-Learn: KMeans, StandardScaler, PCA  
- Jupyter Notebook

---

## 🚀 Future Improvements

- Analisis tren per kategori produk
- Segmentasi berdasarkan frekuensi waktu (bulanan, mingguan)
- Integrasi model ke aplikasi dashboard interaktif (Streamlit)

---

## 📂 Folder Structure

```bash
📦customer-behavior-analysis/
 ┣ 📁 notebooks/
 ┃ ┗ 📄 behavioral_clustering.ipynb
 ┣ 📄 dataset.csv
 ┣ 📄 README.md
 ┗ 📄 requirements.txt
