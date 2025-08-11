# 🛒 Zepto Product Dataset SQL Analysis

This project focuses on the **data analysis of a product inventory dataset** inspired by Zepto (an instant delivery platform). Using PostgreSQL, we perform data exploration, cleaning, and generate actionable insights.

---

## 📁 Table of Contents

- [📌 About the Project](#-about-the-project)
- [🧾 Dataset Structure](#-dataset-structure)
- [🧹 Data Cleaning](#-data-cleaning)
- [📊 Data Exploration](#-data-exploration)
- [📈 Data Analysis & Business Insights](#-data-analysis--business-insights)
- [🛠️ Setup & Execution](#️-setup--execution)
- [🔚 Conclusion](#-conclusion)

---

## 📌 About the Project

Zepto delivers groceries and essentials in under 10 minutes. This dataset simulates their product inventory, including details like pricing, availability, category, and weight. The project uses SQL to:

- Explore data distributions
- Clean anomalies
- Generate business insights
- Estimate revenue and inventory metrics

---

## 🧾 Dataset Structure

The dataset is stored in a table called `zepto`, with the following schema:

| Column Name            | Data Type       | Description                          |
|------------------------|------------------|--------------------------------------|
| `sku_id`               | SERIAL PRIMARY KEY | Unique product identifier           |
| `category`             | VARCHAR(120)     | Product category                      |
| `name`                 | VARCHAR(150)     | Product name                          |
| `mrp`                  | NUMERIC(8,2)     | Maximum Retail Price (₹)              |
| `discountPercent`      | NUMERIC(5,2)     | Discount % applied                    |
| `availableQuantity`    | INTEGER          | Units available in inventory          |
| `discountedSellingPrice` | NUMERIC(8,2)  | Final selling price after discount    |
| `weightInGms`          | INTEGER          | Weight of product in grams            |
| `outOfStock`           | BOOLEAN          | Whether product is out of stock       |
| `quantity`             | INTEGER          | Units ordered                         |

---

## 🧹 Data Cleaning

- Removed rows with MRP or discounted price = 0
- Converted prices from paise to rupees where applicable
- Identified and handled NULL values

```sql
DELETE FROM zepto WHERE mrp = 0;

UPDATE zepto
SET mrp = mrp / 100.0,
    discountedSellingPrice = discountedSellingPrice / 100.0;
