# 📊 Supply Chain Performance & Sales Analysis

### Python | Pandas | NumPy | Matplotlib | Seaborn | Exploratory Data Analysis

## 📌 Project Overview

This project explores sales performance, profitability, customer segments, product demand, and shipping efficiency using the **DataCo Smart Supply Chain Dataset**. The goal is to turn raw transactional data into actionable insights that support business decisions in sales, logistics, and supply chain management.

## 🎯 Project Objectives

- Analyze annual and monthly sales trends.
- Identify high-revenue product categories and customer segments.
- Examine the relationship between sales and profitability.
- Assess shipping delays and delivery efficiency.
- Compare profit ratio distributions across global markets.
- Recommend business actions based on the findings.

## 📂 Dataset

| Attribute | Details |
|---|---|
| Dataset | DataCo Smart Supply Chain Dataset (with missing values) |
| Source | [Kaggle – DataCo Smart Supply Chain](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis) |
| Original records | 180,519 |
| Original columns | 53 |
| File used in notebook | `Supply Chain.csv` |

**Important fields:** `Sales`, `Category Name`, `Customer Segment`, `Order Item Profit Ratio`, `Market`, `Days for shipping (real)`, `Days for shipment (scheduled)`, and `order date (DateOrders)`.

## 🛠️ Tools & Technologies

- **Python** – data analysis
- **Pandas** – data loading, cleaning, grouping, and aggregation
- **NumPy** – numerical operations
- **Matplotlib & Seaborn** – charts and exploratory visualization
- **Jupyter Notebook** – analysis and documentation

## 🔄 Project Workflow

### 1. Data Loading & Understanding

Loaded the CSV file, inspected the dataset's dimensions, columns, data types, and descriptive statistics, and separated numerical from categorical attributes.

### 2. Data Cleaning & Preprocessing

- Replaced 8 missing `Customer Lname` values and 3 missing `Customer Zipcode` values with `Unknown`.
- Removed `Order Zipcode` (86.24% missing) and `Product Description` (100% missing).
- Checked for exact duplicate records; **none were found**.
- Converted order and shipping dates into datetime format.
- Extracted time-related features including order year and month.

**Cleaning result:** 180,519 rows, 56 columns after feature engineering, **0 remaining missing values**, and **0 duplicate rows** (as reported in the notebook).

### 3. Exploratory Data Analysis (EDA)

| Business question | Visualization | Main insight |
|---|---|---|
| How have sales changed over the years? | Bar chart | Sales decreased slightly from 2015 to 2017; 2018 contains only January data. |
| Which product categories generate the highest sales? | Horizontal bar chart | **Fishing** is the leading category by sales. |
| How is revenue distributed across customer segments? | Pie chart | Customer segments contribute different shares of revenue, informing retention priorities. |
| What is the relationship between sales and profit? | Scatter plot | Higher transaction sales do not automatically ensure a positive profit ratio. |
| What is the distribution of shipping delays? | Histogram | Positive shipping-delay values identify shipments exceeding scheduled duration. |
| How does profitability vary across markets? | Box plot | **Pacific Asia** has the highest approximate median profit ratio (0.26), while **LATAM** has the lowest (0.20). |
| How do monthly sales patterns vary across years? | Heatmap | Monthly sales were relatively stable in 2015–2016, with larger fluctuations toward the end of 2017. |
 

## 📈 Key Findings

1. **Sales trends:** Annual sales were approximately 12.3 million in 2015, 12.1 million in 2016, and 11.5 million in 2017. The much smaller 2018 total reflects incomplete year coverage and should not be treated as a comparable full-year result.
2. **Product demand:** The **Fishing** category generated the highest sales among the categories analyzed.
3. **Profitability:** Sales value alone does not determine profit performance; some transactions have negative profit ratios.
4. **Regional profitability:** **Pacific Asia** had the highest median profit ratio (approximately 0.26), compared with approximately 0.20 for **LATAM**. All markets include loss-making transactions.
5. **Shipping efficiency:** Actual versus scheduled shipping days provides a useful measure for identifying delivery delays.
6. **Monthly patterns:** September 2017 recorded approximately 1.14 million in sales, followed by lower totals in November and December. These changes warrant further investigation rather than an assumed seasonal explanation.

## 💡 Business Recommendations

- **Improve profitability:** Review loss-making transactions, discounts, and cost structures instead of prioritizing revenue alone.
- **Reduce shipping delays:** Track positive delay days and investigate recurring logistics bottlenecks.
- **Prioritize product demand:** Use category-level revenue to guide inventory allocation and merchandising, while also considering margins.
- **Strengthen customer retention:** Focus on valuable customer segments and evaluate opportunities in lower-contributing segments.
- **Monitor markets and monthly trends:** Investigate low-margin markets and unexpected sales fluctuations before making expansion or inventory decisions.

## ✅ Final Conclusion

This project transformed raw supply chain data into clean, structured information and business-oriented visual insights. The analysis identifies **profitability, shipping efficiency, and product demand** as three important priorities for improving operational performance, resource allocation, and sustainable business growth.
