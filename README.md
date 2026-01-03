# Retail Distribution Sales Dashboard

## 📌 Project Overview
This project presents an end-to-end **Retail Distribution Sales Dashboard** built using **Power BI**, focusing on sales performance, customer (outlet) behavior, product contribution, and warehouse & supply chain insights.

The dashboard is designed to support **data-driven decision-making** for management by transforming raw transactional data into clear, actionable business insights.

---

## 🎯 Business Objectives
- Monitor overall sales and order performance
- Analyze sales growth and ordering behavior over time
- Identify top-performing products and warehouses
- Understand customer (outlet) ordering patterns
- Highlight risks related to declining order value
- Provide executives with a clear, high-level performance overview

---

## 🧩 Data Description
- **Source**: Retail distribution transactional data
- **Grain**: Order line level (each row represents a product within an order)
- **Rows**: 218,773 records
- **Key Entities**:
  - Outlets (Customers)
  - Warehouses
  - Products
  - Sales Representatives
  - Calendar (Date dimension)

### Important Modeling Note
An **Order Key** was created to correctly represent unique orders, as the raw data does not include a single order identifier.

```DAX
Order Key = FORMAT(sales[Date], "yyyymmdd") & "-" & sales[Outlet_Id] & sales[Warehouse Name]
```

This ensures accurate order counting across all analyses.

---

## 🏗️ Data Model
- **Fact Table**: `sales`
- **Dimension Tables**:
  - `Calendar`
  - `outlets`
  - `warehouse`
  - `rep_list`

A **star schema** design was used to optimize performance and simplify DAX calculations.

---

## 📊 Key KPIs
- Total Sales
- Total Orders
- Average Order Value (AOV)
- Orders per Outlet
- Units per Order
- Year-over-Year (YoY) Growth (Sales & Orders)
- Warehouse Contribution %

All KPIs are fully dynamic and respond to slicers and filters.

---

## 📄 Dashboard Pages

### 1️⃣ Executive Overview
**Purpose:** High-level performance snapshot for decision-makers.

**Highlights:**
- Sales & Orders YoY performance
- Sales trend with rolling average
- Top products and warehouses

**Key Insight:**
> Overall performance shows stable ordering activity, while revenue fluctuations are primarily driven by changes in average order value rather than order count.

---

### 2️⃣ Sales & Products Performance
**Purpose:** Deep dive into product-level contribution and sales structure.

**Highlights:**
- Product contribution tree
- Top-selling products
- Units per order analysis

**Key Insight:**
> Sales concentration in a limited number of products suggests opportunities to improve cross-selling and increase order value across outlets.

---

### 3️⃣ Order & Customer Behavior
**Purpose:** Analyze ordering frequency and customer (outlet) behavior.

**Highlights:**
- Orders over time
- Orders per active outlet
- Average order value trend

**Key Insight:**
> Ordering frequency remains relatively stable over time, but declining average order value limits long-term sales growth across outlets.

---

### 4️⃣ Warehouse & Supply Chain Performance
**Purpose:** Evaluate warehouse contribution and order distribution.

**Highlights:**
- Sales and orders per warehouse
- Warehouse contribution percentage

**Key Insight:**
> Order volume is relatively distributed across warehouses, with the top warehouse contributing 22% of total orders, indicating no single-warehouse dependency.

---

### 5️⃣ YoY Comparison Note
> Year-over-Year metrics are calculated based on the available period in the selected year. Partial-year data may distort YoY results and should be interpreted accordingly.

---

## 🛠️ Tools & Technologies
- Power BI Desktop
- DAX
- Power Query
- Data Modeling (Star Schema)

---

## 📈 Key Takeaways
- Sales decline is primarily driven by reduced **average order value**, not order volume
- Product sales are concentrated, presenting cross-selling opportunities
- Warehouse operations are well-balanced with no major dependency risks
- Stable customer ordering behavior indicates strong retention potential

---

## 🚀 Next Steps & Recommendations
- Introduce product bundles or promotions to increase AOV
- Expand product penetration across outlets
- Monitor pricing and discount strategies
- Further analyze outlet-level segmentation

---

## 👤 Author
**Mohamed Heta**  
Data Analyst | Power BI Developer

---

## 🔖 Tags
`Power BI` `Data Analytics` `Retail Analytics` `Dashboard Design` `Business Intelligence`

