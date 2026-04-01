![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge\&logo=pandas\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge\&logo=numpy\&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github\&logoColor=white)

# 📊 E-Commerce Analytics Dashboard (Power BI)

A production-style, two-page Power BI dashboard analysing marketplace performance using the Brazilian Olist e-commerce dataset.

This project demonstrates end-to-end business intelligence capability, including data modelling, transformation, DAX development, and insight delivery for stakeholders.

---

## 📚 Table of Contents

1. Project Overview
2. Business Objectives
3. Data Architecture
4. Data Model
5. Dashboard Overview
6. Key Insights
7. Tools & Technologies
8. Repository Structure
9. Key Learnings
10. Contact

---

## 🚀 Project Overview

This dashboard delivers a comprehensive analytical view of an e-commerce marketplace, covering:

* Revenue and order performance
* Customer distribution and behaviour
* Product category trends
* Payment method usage
* Delivery performance and logistics
* Order value distribution

The solution is designed for business stakeholders who require clear, actionable insights to support commercial and operational decision-making.

---

## 🎯 Business Objectives

* Develop a scalable **star schema data model** optimised for reporting
* Analyse customer behaviour across geographic regions
* Identify high-performing product categories
* Evaluate payment method distribution and trends
* Assess delivery performance and fulfilment efficiency
* Communicate insights through intuitive, executive-level dashboards

---

## 🧱 Data Architecture

The project follows a standard BI pipeline:

```
Raw CSV Files
    ↓


Power Query (Data Cleaning & Transformation)
    ↓


Star Schema Data Model
    ↓


DAX Measures & KPI Layer
    ↓


Power BI Visualisation
    ↓


Business Insights & Reporting
```

### Key Transformations

* Cleaned and standardised customer, product, and order datasets
* Normalised geolocation data for accurate regional analysis
* Built dimension and fact tables for scalability
* Created calculated measures for KPIs and aggregations using DAX

---

## 🗂️ Data Model

A **star schema** was implemented to ensure performance, flexibility, and maintainability.

### Fact Tables

* `fact_orders` — order-level data
* `fact_order_items` — product-level transactions
* `fact_payments` — payment records

### Dimension Tables

* `dim_customers`
* `dim_products`
* `dim_sellers`
* `dim_geolocation`

### Key Relationship

```
dim_customers[customer_id] 1 → * fact_orders[customer_id]
```

This enables consistent customer-level analysis across all metrics.

---

## 📊 Dashboard Overview

### 📍 Page 1 — Performance Overview

![Dashboard1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Dashboad1.png)

**Purpose:** Provide a high-level view of business performance.

**Core KPIs**

* Total Revenue
* Total Orders
* Average Review Score
* Total Customers
* Total Sellers

**Key Visuals**

* Revenue by Product Category
* Orders by State (Geographic Map)
* Monthly Order Trends
* Delivery Time Distribution
* Review Score Distribution

---

### 📍 Page 2 — Customer & Product Insights

![Dashboard2](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Dashboard.png)

**Purpose:** Analyse customer behaviour, product performance, and payment trends.

**Customer Analysis**

* Customer distribution by state and city
* Orders per customer
* Customer concentration metrics

**Product Analysis**

* Top categories by revenue
* Category share of total orders

**Payment & Behaviour**

* Payment method breakdown
* Order value distribution

---

## 📸 Additional Visuals

### KPIs

![KPI1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/KPI1.png)
![KPI2](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/KPI.png)

### Filters & Slicers

![Slicer1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Slicer1.png)
![Slicer2](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Slicer.png)

### Operational & Behavioural Insights

* Delivery Performance by State
  ![Delivery](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/DeliveryPerformance.png)

* Payment Type Breakdown
  ![Payment](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/PaymentBreakdown.png)

* Category Share of Orders
  ![Category](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/CategoryOrders.png)

* Orders by State

  ![State](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/StateOrder.png)

---

## 🔍 Key Insights

### 👥 Customer Insights

* ~99K unique customers analysed
* Majority of customers placed a single order (dataset limitation)
* Demand is highly concentrated in **São Paulo**, **Rio de Janeiro**, and **Belo Horizonte**
* Strong regional dominance in Southeast Brazil

### 🛍️ Product Insights

* **Beleza & Saúde** is the highest revenue-generating category
* Other top categories include **Relógios & Presentes**, **Cama, Mesa & Banho**, and **Esporte & Lazer**
* Long-tail distribution across niche categories

### 💳 Payment Behaviour

* Credit card accounts for ~75% of transactions
* Boleto represents ~20%
* Minimal usage of vouchers and debit cards

### 🚚 Delivery & Order Value

* Majority of orders fall below £200
* Delivery times typically range between 10–20 days
* Longer delivery durations are associated with inter-state shipping

---

## 🛠️ Tools & Technologies

* Power BI Desktop
* Power Query (ETL)
* DAX (Data Analysis Expressions)
* Python (Pandas, NumPy)
* Star Schema Modelling
* Git & GitHub

---

## 📁 Repository Structure

```
📦 ecommerce-analytics-dashboard/
├── 📁 data/          # Raw and processed datasets
├── 📁 pipeline/      # Data cleaning and transformation scripts
├── 📁 pbix/          # Power BI dashboard file
├── 📁 visuals/       # Dashboard screenshots
└── 📄 README.md
```

---

## 🧠 Key Learnings

* Designed a scalable and efficient star schema data model
* Developed reusable KPI measures using DAX
* Built a structured, multi-page BI dashboard
* Translated raw data into actionable business insights
* Identified dataset limitations and adjusted analysis accordingly
* Delivered a portfolio-ready analytics project aligned with industry standards

---

## 📬 Contact

**Israel Obiomah**
Data Analyst | Power BI | Python | SQL

LinkedIn: https://linkedin.com/in/israel-obiomah-6ba609253
GitHub: https://github.com/teejay7729

 


[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![GitHub](https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/teejay7729)