# 📊 Sales, Customer & Stock Performance Analytics

## 🎯 Project Overview
This project is an end-to-end, highly interactive Business Intelligence dashboard designed to provide a 360-degree view of corporate performance. It empowers stakeholders and decision-makers to track KPIs, analyze customer behavior, and monitor inventory movements through advanced DAX logic and dynamic filtering.

## ❓ Strategic Business Questions Answered
This dashboard provides immediate answers to critical business questions, enabling stakeholders to make data-driven decisions:

**Sales & Profitability:**
* *Are we on track to meet our yearly/quarterly targets for revenue and profit?*
* *How does our current performance compare to the same period last year across different metrics (Sales, Profits, Orders)?*
* *What is the average order value (AOV), and is our profit margin expanding or shrinking?*

**Customer Insights & Retention:**
* *Who are our most valuable customers, and what are their specific purchasing habits (Top 5 products)?*
* *Which key accounts are showing a decline in Year-Over-Year growth (ΔYOY < 0), indicating a potential churn risk?*
* *Geographically, where is our sales volume concentrated, and what products are driving growth in those specific regions?*

**Inventory & Product Performance:**
* *What are our absolute best (or worst) performing products based on dynamic ranking (Top/Bottom N)?*
* *How is our sales volume distributed across different buying packages (Each, Carton, Packet) and product colors?*
* *Which products have the highest variance in YoY performance, requiring immediate supply chain attention?*
* 
## 🛠️ Key Features & Technical Highlights

### 1. Sales Performance (Executive View)
* **Smart KPI Architecture:** Utilizes modern cards with embedded sparklines and target tracking. Reference labels are heavily used to display Last Year (LY) and Year-Over-Year (YoY) growth without cluttering the UI.
* **Space Optimization:** Instead of multiple static charts, a single dynamic Column Chart compares Current vs. Last Year data.
* **Parameter Switching:** A built-in Button Slicer allows users to instantly toggle the entire page's context between Sales, Profits, and Orders.
* **Context-Rich Tooltips:** Custom report page tooltips dynamically update based on the selected metric, showing Top 5 Cities, Top 5 Products, and YoY growth for any specific month hovered.

*![Sales Performance Dashboard](images/GIF/Sales_Analysis.gif)*

---

### 2. Customers Analysis (Deep Dive & Geolocation)
* **Advanced Tabular Visuals:** The Top 20 Customers table integrates in-cell data bars for visual baseline comparisons between the current and previous year.
* **Conditional Formatting Logic:** Highly customized $\Delta$ YoY variance and percentage columns using color-coded text and icons to instantly flag churn risks or growth accounts.
* **Geospatial Insights:** Azure Maps integration highlights geographic sales density, cross-filtered with the Top 10 Selling Cities.
* **Interactive Cross-Filtering:** Hovering over any customer or city instantly filters a custom tooltip revealing their specific Top 5 purchased products.

*![Custoemr Analysis Dashboard](images/GIF/Customer_Analysis.gif)*
---

### 3. Stock Analysis (Self-Service Analytics)
* **Dynamic What-If Ranking:** Built a highly complex DAX architecture allowing end-users to dynamically rank products. Users can toggle between **Top** or **Bottom** performers, and manually adjust the **N-value** (e.g., Top 3, Bottom 5, Top 15) on the fly.
* **Measure Swapping:** The dynamic ranking is fully integrated with a button slicer, meaning the Top/Bottom N logic seamlessly recalculates across Sales, Profits, or Orders.
* **Inventory Distribution:** Clean visualizations tracking the percentage of sales by Buying Package and Most Ordered Colors to assist supply chain and inventory decisions.

*![Stock Analysis Dashboard](images/GIF/Stock_Analysis.gif)*
---
## 💡 Key Business Insights

* **Regional Expansion & Growth Drivers:** 
  A deep-dive analysis into geographic performance reveals that the top revenue growth was not accidental. While the #1 leading city experienced a slight 10% dip in sales, **the remaining 9 top cities exhibited extraordinary YoY growth ranging between +
  15%(Knights Landing City) and +212% (Panaca City)**. 
  
  * **Business Impact:** This proves that the company's regional expansion strategy and market penetration in secondary hubs successfully offset minor losses in mature markets, driving the overall revenue surge.
  ---
## 🧠 Technical Skills Applied
* **Advanced DAX:** Calculation Groups, Field Parameters, Dynamic Ranking (`RANKX`, `TOPN`), and customized conditional formatting measures.
* **Data Modeling:** Robust relational model engineered using a **Star Schema** architectural pattern. This model handles multiple Fact tables (with different granularities, e.g., Sales vs Targets) and dimensions (`Customer`, `Date`, `StockItem`, `City`, `Employee`) to ensure optimal DAX performance and reporting flexibility.

![Project Data Model](images/Modeling.png)

* **UI/UX Design:** Implemented dynamic header text (e.g., `Filters Applied >> Year: 2015`) to maintain state awareness, clear navigation menus, and clean whitespace management for executive reporting.
