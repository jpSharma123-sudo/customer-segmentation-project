# 🛍️ Customer Segmentation Using Unsupervised Learning

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-2.x-green?logo=pandas)

> An end-to-end ML project segmenting mall customers into distinct behavioral groups using **K-Means Clustering**.

---

## 📁 Project Structure

```
customer_segmentation/
├── data/
│   └── Mall_Customers.csv
├── notebooks/
│   └── customer_segmentation.ipynb
├── outputs/
│   ├── 01_eda_overview.png
│   ├── 02_correlation_heatmap.png
│   ├── 03_elbow_silhouette.png
│   ├── 04_cluster_scatter.png
│   ├── 05_cluster_profiles.png
│   └── 06_cluster_donut.png
├── reports/
│   └── Customer_Segmentation_Report.pdf
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

| Feature | Description |
|---|---|
| `CustomerID` | Unique ID (dropped before modeling) |
| `Gender` | Male / Female |
| `Age` | Customer age (18–70) |
| `Annual Income (k$)` | Annual income in thousands |
| `Spending Score (1-100)` | Mall-assigned spending behavior score |

**200 rows · 5 columns · 0 missing values**

---

## ⚙️ Tech Stack

```
Python 3.10+  |  pandas  |  numpy  |  matplotlib  |  seaborn  |  scikit-learn
```

```bash
pip install -r requirements.txt
```

---

## 🔄 Pipeline

```
Load Data → EDA → Encode & Scale → Elbow + Silhouette → KMeans(K=5) → Visualize → Insights
```

---

## 🔍 Key Results

| Metric | Value |
|---|---|
| Optimal K | **5** |
| Silhouette Score | **0.5547** |
| Algorithm | K-Means++ |
| Features | Annual Income, Spending Score |

---

## 👥 Customer Segments

| Cluster | Label | Avg Income | Avg Spend | n |
|---|---|---|---|---|
| C0 | Average Customers | $55.3k | 49.5 | 81 |
| C1 | VIP — High Income High Spend | $86.5k | 82.1 | 39 |
| C2 | Impulsive — Low Income High Spend | $25.7k | 79.4 | 22 |
| C3 | Cautious — High Income Low Spend | $88.2k | 17.1 | 35 |
| C4 | Budget — Low Income Low Spend | $26.3k | 20.9 | 23 |

---

## 💡 Business Recommendations

- **VIP (C1)** → Premium memberships, early access, concierge
- **Cautious Rich (C3)** → Trust-building campaigns, quality emphasis
- **Impulsive (C2)** → Flash sales, BNPL/EMI options
- **Budget (C4)** → Value packs, discount coupons
- **Average (C0)** → Loyalty points, seasonal promotions

---

## 🚀 Run

```bash
git clone https://github.com/jpSharma123-sudo/customer-segmentation-project
cd customer-segmentation && pip install -r requirements.txt
jupyter notebook notebooks/customer_segmentation.ipynb
```
