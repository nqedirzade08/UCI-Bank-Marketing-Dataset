# 🏦 Bank Marketing Campaign Analysis & Hypothesis Testing

This repository contains a data analysis and statistical evaluation project based on bank telemarketing campaign data. The goal is to analyze customer demographics, evaluate account balances, compute term deposit conversion rates, and perform two-sample hypothesis testing using Python.

---

## 📌 Project Overview

The analysis aims to understand customer characteristics influencing term deposit subscription (`y`). It covers exploratory data analysis (EDA), multi-variable grouping, NumPy-based matrix transformation (Z-score calculation), and inferential statistical testing (Independent T-Test).

### 📊 Dataset Information
* **Dataset:** Bank Marketing Dataset (`bank.csv`)
* **Delimiter:** `;`
* **Target Variable:** `y` (Term deposit subscription: `yes` / `no`)

---

## 🛠️ Tools & Libraries Used

* **Python 3.x**
* **Pandas:** Data loading, aggregation, filtering, and export.
* **NumPy:** Array manipulation and standardized Z-score computation.
* **SciPy (`scipy.stats`):** Independent two-sample T-test (`ttest_ind`).

---

## 🚀 Analysis Stages

### 1. Exploratory Data Analysis (EDA)
* Generated summary statistics (`describe()`) for key numerical features: **Age** and **Balance**.

### 2. Segmented Aggregation & Conversion Rate
* Grouped customers by `job` and `marital` status to compute average account balances and customer counts.
* Calculated the overall term deposit subscription (conversion) rate:
  $$\text{Conversion Rate} = \frac{521}{4521} \times 100 \approx 11.52\%$$

### 3. NumPy Vectorization & Standardization (Z-Score)
* Converted core numeric columns (`age`, `balance`, `duration`) into NumPy arrays.
* Calculated standardized Z-scores for customer account balances to detect relative financial standing across the customer base.

### 4. Hypothesis Testing (Two-Sample T-Test)
Performed an **Independent Two-Sample T-Test** to evaluate whether account balances differ significantly between subscribers (`y = yes`) and non-subscribers (`y = no`):
* **Subscriber Mean Balance (`y = yes`):** ~$1,571.96
* **Non-Subscriber Mean Balance (`y = no`):** ~$1,403.21
* **P-Value:** `0.2287`
* **Conclusion:** Since $p \approx 0.2287 > 0.05$, there is **no statistically significant difference** between the average balances of customers who subscribed and those who did not.

---

## 💡 Key Insights

* **Conversion Rate:** Only ~11.52% of targeted clients subscribed to a term deposit.
* **Account Balance Impact:** Although subscribers maintain a higher average balance than non-subscribers, statistical hypothesis testing reveals that balance alone is not a statistically significant differentiator for campaign success.

---

## 📁 Repository Structure

```text
├── bank.csv                                   # Raw dataset
├── processed_bank.csv                         # Exported/Processed dataset
├── UCI Bank Marketing Dataset.ipynb           # Main analysis script
└── README.md                                  # Project documentation
