# Chips Category Analysis - Data Analytics Project

## Project Overview

This project analyzes customer transaction and behavior data for a large retail chain to support the **Category Manager (Julia)** in understanding how customers purchase chips. It also evaluates the performance of a new **store layout trial** conducted in Stores **77, 86, and 88**.

The project is separated into two major components:

- **Task 1 – Customer Analytics & Commercial Strategy**
- **Task 2 – Experimentation, Control Store Selection & Uplift Testing**

All work is completed using Python, focusing on data wrangling, customer insights, store-level performance analysis, and actionable business recommendations.

---
## Project Structure

structure/
│

├── README.md                     # Project overview & instructions

├── data/                         # Raw input datasets 

├── QVI_transaction_data.xlsx # Task 1

├── QVI_purchase_behaviour.csv # Task 1

└── QVI_data.csv # Task 2

├── quantium_data_analytics_project.ipynb  

NOTE: This notebook runs end-to-end and includes All necessary library imports. Step-by-step executed cells. The reviewer only needs to open it and run the cells in order. 

---

## 🧩 Task 1 — Customer Analytics & Sales Drivers

### 🎯 Objective

Identify:
- Which customer segments spend the most on chips  
- What drives sales in each segment  
- What commercial strategy should be recommended to the Category Manager  

### 🧹 Data Preparation

Task 1 involved:

- Importing transaction and customer datasets  
- Checking for missing values and inconsistent data types  
- Detecting and removing outliers (e.g., 200-unit bulk purchases)  
- Creating new variables such as:
  - **PACK_SIZE** (grams extracted from product names)
  - **BRAND** (first word of product name)
- Merging customer demographics with transaction-level data

These steps ensured the dataset was clean, reliable, and ready for analysis.

### 📊 Key Metrics Calculated

To understand purchasing behavior across customer segments, the following metrics were computed:

- Total chip sales  
- Number of customers  
- Total units sold  
- Number of transactions  
- Units per customer  
- Spend per customer  
- Price per unit  
- Transactions per customer  

All metrics were calculated across **LIFESTAGE × PREMIUM_CUSTOMER** segments.

### 🔍 Insights From Task 1

**1. Mature households drive the majority of chip sales**  
The highest-spending groups were:
- Older Families  
- Retirees  
- Older Singles/Couples  

These customers have higher purchasing power and larger basket sizes.

**2. Higher revenue is driven by more customers, not higher prices**  
- Unit prices were similar across all segments  
- Segments with the highest sales simply had **more customers**

**3. Spend is driven by **basket size**, not by how often customers shop**  
- Transactions per customer were similar across segments  
- Older segments bought more **units**, meaning larger baskets

**4. Younger households are underdeveloped**  
- New Families and Young Families had lower chip penetration  
- This represents an opportunity for targeted pack sizes and promotions


### 🧠 Strategic Recommendation (Task 1)
 
**1. Protect & grow the mature household segments**
- Focus on range, shelf space, and availability  
- Run multipack deals and volume-based promotions  
- Encourage larger baskets rather than price discounts  

**2. Develop younger family segments**
- Introduce smaller, kid-friendly packs  
- Market family value bundles  
- Offer introductory promotions  

**3. Avoid heavy discounting**
- Price per unit is uniform across segments  
- Discounting will not significantly change behavior  

---

## Task 2 — Experimentation & Uplift Testing

### 🎯 Objective

Evaluate the performance of a new **store layout trial** in Stores **77, 86, and 88** by:

1. Selecting appropriate control stores  
2. Measuring trial vs pre-trial sales performance  
3. Running significance tests  
4. Providing rollout recommendations  

### Control Store Selection

Control stores were selected using **similarity of pre-trial monthly trends** in:

- Total sales  
- Number of customers  
- Transactions per customer  

The closest matches were:

| Trial Store | Selected Control Store |
|------------|-------------------------|
| 77         | 167                     |
| 86         | 159                     |
| 88         | 201                     |

These stores have similar baseline behavior and form valid comparisons.

### 📈 Trial vs Control Store Performance (Summary)

**Store 77 — Positive Impact**
- Strong uplift in total sales  
- Driven by **more purchasing customers**  
- Statistically significant improvement  
- Excellent candidate for rollout  

**Store 86 — Negative Impact**
- Sharp decline in performance compared to control  
- Fewer customers and fewer transactions  
- Statistically significant deterioration  
- Layout should **not** be rolled out to stores like 86  

**Store 88 — Mixed / Neutral Impact**
- Slight decline in customer counts  
- Slight increase in transactions per customer  
- Net effect is small and slightly negative  
- Layout effect inconclusive for similar stores  

### Final Recommendation (Task 2)

1. Roll out the layout to stores similar to **Store 77**
Reliable and significantly positive uplift.

2. Do **not** roll out to stores like **Store 86**
Impact is clearly negative.

3. Use caution for stores similar to **Store 88**
Mixed evidence; layout may need refinement before scaling.
