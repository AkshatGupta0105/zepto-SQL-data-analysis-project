# 🛒 Zepto Product Inventory Analysis (SQL Project)

This project is a comprehensive **SQL-based data analysis** of a simulated product inventory dataset inspired by **Zepto**, an Indian quick-commerce company. It showcases the process of cleaning, exploring, and analyzing real-world retail product data to extract valuable business insights.

---

## 🎯 Project Aim

The main objective of this project is to:

- Analyze a product inventory dataset using **SQL**
- Clean and transform raw data into meaningful formats
- Discover patterns in pricing, stock levels, discounts, and sales readiness
- Answer key business questions that can help improve inventory and pricing strategy
- Generate actionable insights related to **revenue estimation**, **product performance**, and **category-level metrics**

---

## 🧪 Dataset Overview

The dataset represents a collection of products sold on an online grocery platform, with information such as:

- Product name and category
- Maximum Retail Price (MRP)
- Discount offered
- Final selling price
- Product weight
- Available stock quantity
- Stock status (in or out of stock)

Each product is stored as an individual record (SKU).

---

## 🛠 Procedure

The project was divided into three key stages:

### 1️⃣ Data Cleaning

- **Removed invalid entries:** Products with MRP or selling price equal to zero were identified and removed, as they represent incomplete or inaccurate data.
- **Unit correction:** Prices were corrected by converting values from paise to rupees (where needed) to standardize currency units.
- **Missing values check:** Records with missing critical fields (like name, category, MRP, or stock status) were identified for potential exclusion or further inspection.
- **Duplicates check:** Products with the same name listed multiple times were reviewed for duplication or variation across SKUs.

### 2️⃣ Data Exploration

- **Category analysis:** Identified the various product categories and how many products each contained.
- **Stock analysis:** Explored how many products were currently in stock versus out of stock.
- **Product frequency:** Checked if any product names were listed multiple times to spot duplicates or variations (e.g., different sizes of the same item).
- **Basic summary stats:** Viewed samples of the data and understood its structure before deeper analysis.

### 3️⃣ Business-Focused Data Analysis

Key questions answered through the analysis included:

- **Top Value Products:** Identified products offering the highest discounts, highlighting marketing or clearance opportunities.
- **Out-of-Stock Premium Products:** Found high-MRP products that are out of stock, indicating potential loss of high-value sales.
- **Revenue Estimation:** Calculated estimated revenue for each category based on current stock and selling prices.
- **Price Sensitivity Analysis:** Found high-priced products with low discounts to understand premium pricing strategy.
- **Category Discounting Trends:** Determined which categories have the highest average discounts, offering insights into promotional focus.
- **Value for Money:** Calculated selling price per gram to evaluate how cost-effective products are by weight.
- **Weight Categorization:** Grouped products into size categories (Low, Medium, Bulk) to understand logistical and delivery requirements.
- **Total Inventory Load:** Computed the total inventory weight per category, which can help in storage and transport planning.

---

## 📈 Outcomes & Key Insights

- Identified the **top 10 best-value products** based on discount percentage, highlighting attractive deals for customers.
- Found that some **high-priced products were out of stock**, indicating lost sales opportunities and the need for better inventory planning.
- Estimated **potential revenue** per product category, helping prioritize categories that generate the most income.
- Revealed that certain categories had **significantly higher discount averages**, likely due to perishability or competition.
- Discovered products offering **better price-per-gram value**, useful for pricing strategy and marketing.
- Grouped products into **Low, Medium, and Bulk** weight classes to assist with operational logistics and packaging needs.
- Identified the **heaviest inventory categories**, useful for supply chain optimization.

---

## 🧠 Business Applications

This type of SQL analysis can be directly applied in:

- **E-commerce inventory management**
- **Discount strategy planning**
- **Revenue forecasting**
- **Stock replenishment decisions**
- **Customer value proposition analysis**
- **Logistics and delivery optimization**

---

## 🚀 Tools Used

- **PostgreSQL** for writing and executing SQL queries
- **SQL IDEs** such as DBeaver or pgAdmin for managing the database
- Structured Query Language (SQL) as the core analysis language

---

## 🧩 Future Enhancements

- Visualize insights using **Power BI** or **Tableau**
- Build an **interactive dashboard** for category-level revenue tracking
- Use **Python/Streamlit** for a dynamic user interface
- Add **sales data over time** to enable time-series and forecasting analysis

---

## 📘 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙋‍♀️ Contributions

Suggestions, improvements, and pull requests are always welcome. Fork the repository, open an issue, or submit a PR to contribute.

---

## ✨ Summary

This project demonstrates how raw product inventory data can be transformed using SQL into a valuable source of insights for business decision-making. It showcases the power of SQL for:

- Data exploration
- Data cleaning
- Business-focused analysis
- Revenue and inventory strategy

It's a great portfolio project for **data analysts**, **business analysts**, and **data science learners** looking to work on real-world use cases using structured data.

