# 📊 Superstore Retail Analytics – Power BI Dashboard

## 🔍 Project Overview
This project focuses on analyzing and visualizing sales performance data of a fictional retail company, **Superstore**, using **Power BI**. The dashboard provides actionable insights into sales, profit, customer segments, product categories, shipping trends, and returns across different geographies and time periods.

> ✅ **Goal**: Enable data-driven decision-making for stakeholders by creating an interactive, insightful, and user-friendly Power BI dashboard.

---

## 🗃️ Dataset Description

- **Source**: [Superstore Sales Dataset](https://www.kaggle.com/datasets)
- **File**: `SuperStore_Sales_Dataset.csv`
- **Rows**: 5,900+ | **Columns**: 23
- **Key Fields**:
  - `Order Date`, `Ship Date`, `Sales`, `Profit`, `Quantity`
  - `Customer ID`, `Segment`, `Region`, `State`
  - `Product Category`, `Sub-Category`, `Product Name`
  - `Payment Mode`, `Return Status`, `Discount`

---

## 🧱 Data Modeling & Transformation

### 🔄 Power Query (ETL)
- Cleaned and transformed raw data:
  - Parsed date columns
  - Removed nulls and fixed inconsistencies
  - Trimmed and standardized text fields
- Added calculated columns and flags (e.g., return status indicator)

### ⭐ Star Schema Design

| Fact Table | Dimension Tables |
|------------|------------------|
| `Sales` (Order-level facts) | `Date`, `Customer`, `Product`, `Geography`, `Ship Mode` |

> ✅ Relationships were created based on keys (Customer ID, Product ID, Order Date, etc.) for efficient querying.

---

## 🧮 Key DAX Measures

| Measure | Description |
|--------|-------------|
| `Total Sales` | Sum of all sales transactions |
| `Total Profit` | Sum of profit across all orders |
| `Profit Margin %` | `(Profit / Sales) * 100` |
| `YOY Sales Growth` | Year-over-year growth using `SAMEPERIODLASTYEAR` |
| `Return Rate` | % of orders returned by customers |
| `Monthly Sales Trend` | Rolling sales by month using time-intelligence |

---

## 📊 Dashboard Features

### ✅ Key Visuals
- 📍 **Map**: Sales by State with conditional formatting
- 📈 **Trend Charts**: Monthly Sales and Profit analysis
- 🧑‍💼 **Customer Segment Analysis**: Sales & Profit by segment
- 📦 **Product Analysis**: Top-performing categories & sub-categories
- 🚚 **Shipping Mode Impact**: Shipping cost vs profit
- 🔁 **Returns Summary**: Products and categories with highest return rates

### 🧩 Interactive Features
- **Slicers** for Segment, Region, Ship Mode, Payment Type
- **Drill-downs** from Category → Sub-Category → Product
- **Drill-through**: Explore customer-specific purchase history
- **Bookmarks**: Pre-set insights for storytelling (e.g., “Executive Overview”)

---

## 💡 Insights & Recommendations

1. **Top Segment**: Corporate and Consumer segments generated over 70% of total profit.
2. **High Return Items**: Furniture category had the highest return rates; suggests quality review.
3. **Best Region**: Western region showed 15% YoY growth—ideal for regional marketing campaigns.
4. **Payment Insights**: Digital payments (UPI, Credit Card) associated with higher average order value.

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| **Power BI** | Data visualization and dashboard creation |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Advanced measures and KPIs |
| **Excel/CSV** | Raw dataset input |
| **Git & GitHub** | Version control and project documentation |

---


