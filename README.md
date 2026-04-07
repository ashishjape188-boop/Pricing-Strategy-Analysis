# 📊 Pricing Strategy Analysis Using Demand Elasticity & Market Basket Analysis

## 📌 Project Overview

This project focuses on analyzing retail transaction data to develop **data-driven pricing strategies** using demand elasticity modeling, discount simulations, premium pricing identification, and product bundling techniques.

The objective is to determine **optimal pricing decisions** that maximize revenue while maintaining customer demand.

This project demonstrates advanced skills in:

* Exploratory Data Analysis (EDA)
* Price Elasticity Modeling
* Revenue Optimization
* Discount Strategy Simulation
* Premium Pricing Analysis
* Market Basket Analysis (Apriori Algorithm)

---

# 🎯 Business Objectives

The key business questions addressed:

* How does **price affect demand**?
* Which products should receive **discounts**?
* Which products can support **premium pricing**?
* What discount level generates **maximum revenue**?
* Which products are frequently purchased together?
* How can bundling increase overall sales?

---

# 📂 Dataset Information

The dataset contains retail transaction-level data.

### Key Features:

| Feature     | Description           |
| ----------- | --------------------- |
| InvoiceNo   | Unique transaction ID |
| StockCode   | Unique product ID     |
| Description | Product name          |
| Quantity    | Units purchased       |
| InvoiceDate | Transaction timestamp |
| UnitPrice   | Price per unit        |
| CustomerID  | Unique customer ID    |
| Country     | Customer location     |

---

# 🧹 Data Cleaning Steps

* Removed cancelled transactions
* Handled missing values
* Removed invalid records
* Filtered non-product entries (POSTAGE, BANK CHARGES)
* Converted dates into datetime format
* Created new **Revenue column**

```python
df['Revenue'] = df['Quantity'] * df['UnitPrice']
```

---

# 📊 Exploratory Data Analysis (EDA)

EDA was performed to understand:

* Quantity distribution
* Unit price distribution
* Revenue spread
* Outlier detection
* Price vs Demand relationship

### Key Observations:

* Revenue distribution shows strong right skew
* Price variations influence demand levels
* Several products show high purchase frequency

---

# 📈 Price Elasticity Modeling

A **log-log regression model** was used to measure demand elasticity.

### Model Used:

```python
LogQuantity = β0 + β1(LogPrice)
```

Where:

* β1 = Price Elasticity
* Elasticity < -1 → Elastic demand
* Elasticity > -1 → Inelastic demand

### Key Findings:

* Majority of products were **price elastic**
* Elastic products are sensitive to price changes
* Inelastic products showed stable demand

---

# 💸 Discount Strategy Simulation

Different discount levels were simulated:

| Scenario         | Revenue Outcome     |
| ---------------- | ------------------- |
| Base Revenue     | ~7.05 Million       |
| 5% Discount      | ~8.57 Million       |
| 10% Discount     | ~9.19 Million       |
| **15% Discount** | **~9.69 Million** ⭐ |

### Key Insight:

**15% discount generated the highest projected revenue.**

---

# 💰 Premium Pricing Strategy

Products with:

* Low elasticity
* High revenue

Were identified as premium candidates.

### Strategy:

* Increase price by **3–7%**
* Maintain demand stability
* Improve profit margins

Example Premium Products:

* HOT WATER BOTTLE TEA AND SYMPATHY
* WHITE SKULL HOT WATER BOTTLE
* PAPER CHAIN KIT 50'S CHRISTMAS

---

# 📦 Product Bundling Strategy (Apriori Algorithm)

Market Basket Analysis was used to find frequently purchased product combinations.

### Algorithm Used:

```python
from mlxtend.frequent_patterns import apriori
from mlxtend.frequent_patterns import association_rules
```

### Key Bundle Insights:

High-lift bundles identified:

* PINK REGENCY TEACUP + GREEN REGENCY TEACUP
* STRAWBERRY CHARLOTTE BAG + RED RETROSPOT BAG
* CHARLOTTE BAG PINK POLKADOT + RED RETROSPOT BAG

These bundles showed:

* Lift > 14 ⭐
* Strong cross-selling potential

---

# 📊 Key Performance Indicators (KPIs)

| KPI                | Value         |
| ------------------ | ------------- |
| Total Revenue      | ~7.05 Million |
| Best Discount      | **15%**       |
| Maximum Revenue    | ~9.69 Million |
| Elastic Products   | ~75%          |
| Inelastic Products | ~25%          |
| Top Bundle Lift    | **>14**       |

---

# 🧠 Business Recommendations

Based on the analysis:

### Discount Strategy

* Apply **10–15% discounts** to elastic products
* Use promotional campaigns on price-sensitive items

### Premium Pricing Strategy

* Increase prices slightly for inelastic products
* Focus on high-demand premium items

### Bundling Strategy

* Create bundle offers for frequently paired products
* Offer **10–12% bundle discounts**
* Improve cross-selling opportunities

---

# 🛠 Tools & Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Mlxtend (Apriori Algorithm)
* Jupyter Notebook

---

# 📈 Project Workflow

```text
Data Collection
        ↓
Data Cleaning
        ↓
EDA Visualization
        ↓
Elasticity Modeling
        ↓
Discount Simulation
        ↓
Premium Pricing Analysis
        ↓
Market Basket Analysis
        ↓
Business Recommendations
```

---

# 📊 Project Outcomes

This project successfully:

✔ Identified optimal discount levels
✔ Detected premium pricing opportunities
✔ Found high-value product bundles
✔ Modeled demand-price relationships
✔ Generated revenue optimization strategies

---

# 🚀 Future Improvements

* Build dynamic pricing models
* Add time-series demand forecasting
* Deploy pricing dashboard
* Integrate customer segmentation
* Apply machine learning pricing models

---

# 👨‍💻 Author

**Ashish Jape**
Data Science & Analytics

---

# ⭐ If You Found This Project Useful

Give it a ⭐ on GitHub!
