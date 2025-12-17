# 🛍️ RFM E-commerce Customer Segmentation Analysis

## Project Overview

This is a comprehensive, full-cycle data analysis case study focused on applying **Recency, Frequency, and Monetary (RFM) analysis** to a transactional dataset of 1,000 e-commerce customers.

The primary goal was to segment the customer base into distinct, actionable groups, allowing the marketing team to transition from mass campaigns to targeted, personalized retention and growth strategies. The entire workflow was executed using Python, Pandas, and Matplotlib.

## 🎯 Executive Summary

The analysis revealed a highly polarized customer base, with **69.5% classified as 'Lost/Dormant'**. The core strategic challenge is a high churn rate paired with an opportunity to cultivate a small group of **'New/High Value Single Buyers' (21.6%)**. Immediate action must focus on large-scale win-back campaigns and aggressive loyalty conversion for recent purchasers.

---

## Methodology and Technical Workflow

The project followed a standard data science methodology, implemented entirely in the provided Jupyter Notebook (`rfm_analysis.ipynb`):

1.  **Data Cleaning:** Handled data type conversion (e.g., `PurchaseDate` to datetime format) and ensured data integrity by confirming no non-positive transactions existed.
2.  **RFM Calculation:** Aggregated transaction data by `CustomerID` to calculate the three core metrics using a `Snapshot Date` (2023-06-11) set one day after the last purchase.
3.  **Scoring & Segmentation:** Raw metrics were converted into scores (1-4) using **custom quantile-based functions** to handle data ties robustly. Scores were combined into strategic business segments (e.g., 'Champions', 'At Risk').
4.  **Visualization:** Matplotlib and Seaborn were used to visualize the segment distribution, providing a clear executive-level overview.

---

## Key Findings and Segment Distribution

The customer base is primarily split between dormant and new customers, with a small number of critical high-value groups.

| Segment | # Customers | % of Base | Description |
| :--- | :--- | :--- | :--- |
| **06. Lost/Dormant** | 695 | 69.5% | Purchased long ago (Low R), low F and M. |
| **03. New/High Value Single Buyer** | 216 | 21.6% | Purchased recently (High R), but only once (Low F). |
| **01. Champions** | 18 | 1.8% | Best customers: High R, F, and M. |
| **04. At Risk** | 17 | 1.7% | Used to be loyal (High F), but Recency is low (Low R). |

### Customer Segment Visualization



---

## 💡 Actionable Business Recommendations

The following strategies are tailored to maximize the return on investment (ROI) for each critical segment:

### 1. **Focus: Lost/Dormant Customers (69.5%)**
* **Strategy:** Launch a large-scale **deep-discount win-back campaign** (e.g., $35$ off a purchase of $70$ or more) with a strong sense of urgency (7-day expiry).
* **Goal:** Reactivate the largest pool of former buyers to generate an immediate, high-volume revenue boost.

### 2. **Focus: New/High Value Single Buyers (21.6%)**
* **Strategy:** Deploy a **personalized loyalty on-ramp sequence**. Offer a unique free shipping or small dollar-amount coupon specifically for their *second* purchase, tied to product recommendations related to their first order.
* **Goal:** Convert recent, high-spending first-time buyers into loyal, multi-purchase customers to secure future CLV.

### 3. **Focus: Champions (1.8%)**
* **Strategy:** Implement an **exclusive VIP rewards program** that grants early access to new product launches or limited-edition items. **Do not use discounts.**
* **Goal:** Retain the highest-value segment by making them feel valued, ensuring continued loyalty and maximizing their already high spending.

---

### **View the Full Analysis**

The complete code, data cleaning steps, methodology, and all outputs are available in the linked Jupyter Notebook:

➡️ **[rfm\_analysis.ipynb](RFM_Portfolio_Project.ipynb)**
