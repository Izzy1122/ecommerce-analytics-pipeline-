![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)



# 📊 E‑Commerce Analytics Dashboard (Power BI)

A two‑page Power BI dashboard analysing sales performance, customer behaviour, product trends, and payment insights using the Brazilian Olist e‑commerce dataset.  
This project demonstrates end‑to‑end BI capability: data modelling, DAX, visual analytics, and insight communication.

---

# 📚 Table of Contents
1. [Project Summary](#project-summary)
2. [Objectives](#objectives)
3. [Architecture](#architecture)
4. [Data Model](#data-model)
5. [Dashboard Pages](#dashboard-pages)
   - [Page 1 — E‑commerce Performance Overview](#page-1--e-commerce-performance-overview)
   - [Page 2 — Customer & Product Insights](#page-2--customer--product-insights)
6. [Key Insights](#key-insights)
7. [Tools & Technologies](#tools--technologies)
8. [Repository Structure](#repository-structure)
9. [What I Learned](#what-i-learned)
10. [Contact](#contact)

---

# 🚀 Project Summary

This project provides a comprehensive analytical view of an e‑commerce marketplace, focusing on:

- Sales performance  
- Customer distribution  
- Product category behaviour  
- Payment preferences  
- Delivery performance  
- Order value patterns  

The dashboard is designed for business stakeholders who need a clear, actionable view of marketplace performance.  
It demonstrates strong BI skills across data modelling, DAX, visual storytelling, and insight communication.

---

# 🎯 Objectives

- Build a clean, professional **Power BI dashboard** using a star schema  
- Analyse customer behaviour across states and cities  
- Identify top‑performing product categories  
- Understand payment method distribution  
- Explore order value and delivery time patterns  
- Present insights clearly and visually for decision‑making  

---

# 🧱 Architecture

The project follows a standard BI pipeline:


## 🧱 Architecture

- 📁 **Raw CSV Files**  
  ↓  
- 🧹 **Power Query (Cleaning & Transformation)**  
  ↓  
- 🗂️ **Star Schema Data Model**  
  ↓  
- 📐 **DAX Measures & KPIs**  
  ↓  
- 📊 **Power BI Visualisation Layer**  
  ↓  
- 💡 **Insights & Storytelling**


### Key Transformations
- Cleaned and normalised customer, product, and order tables  
- Standardised geolocation data  
- Built dimension tables  
- Created fact tables for orders, items, and payments  
- Added DAX measures for KPIs and aggregations  

---

# 🗂️ Data Model

The model uses a **star schema** for clarity and performance.

### **Fact Tables**
- `fact_order` — order-level data  
- `fact_order_items` — product-level order details  
- `fact_payments` — payment transactions  

### **Dimension Tables**
- `dim_customers`  
- `dim_products`  
- `dim_sellers`  
- `dim_geolocation`  

### **Key Relationship**
dim_customers[customer_id] 1 → * fact_order[customer_id]


This enables customer-level analysis across the entire model.

---

# 📊 Dashboard Pages

## 📍 Page 1 — E‑commerce Performance Overview

![Dashboard1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Dashboad1.png)

This page provides a high‑level view of marketplace performance.

### **KPIs**
- Total Revenue  
- Total Orders  
- Average Review Score  
- Total Sellers  
- Total Customers  

### **Visuals**
- Revenue by Category  
- Orders by State (Map)  
- Orders by Month  
- Delivery Time Distribution  
- Review Score Distribution  

### **Purpose**
To give stakeholders a quick understanding of overall business performance and operational efficiency.

---

## 📍 Page 2 — Customer & Product Insights

![Dashboard](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Dashboard.png)

This page focuses on customer demographics, product behaviour, and payment trends.

### **Customer KPIs**
- Total Customers  
- Orders per Customer  
- Avg Orders per Customer  
- Customer Distribution  

### **Customer Segmentation**
- Top States by Customers  
- Top Cities by Customers  

### **Product Insights**
- Top Categories by Revenue  
- Category Share of Orders  
- Top Products (optional extension)  

### **Payment & Order Behaviour**
- Payment Type Breakdown  
- Order Value Distribution  

### **Purpose**
To understand who the customers are, what they buy, and how they pay.


📍More Visuals

## KPIs

![KPI1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/KPI1.png)

![KPI](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/KPI.png)

## Slicers

![Slicer1](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Slicer1.png)

![Slicer](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/Slicer.png)

## Delivery Performance by State (Time vs Late %)

![DeliveryPerformance](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/DeliveryPerformance.png)

## Payment Type Breakdown

![PaymentBreakdown](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/PaymentBreakdown.png)

## Category Share of Oders

![CategoryOrders](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/CategoryOrders.png)

## Total Orders by State
![StateOrder](https://raw.githubusercontent.com/teejay7729/ecommerce-analytics-pipeline/refs/heads/main/Visuals/StateOrder.png)


---

# 🔍 Key Insights

## 👥 Customer Insights
- 99K unique customers in the dataset  
- All customers placed **one order** (dataset limitation)  
- Customer demand is concentrated in **São Paulo**, **Rio de Janeiro**, and **Belo Horizonte**  
- Strong urban dominance in the Southeast region  

## 🛍️ Product Insights
- **beleza_saude** is the highest‑revenue category  
- Other strong categories include **relogios_presentes**, **cama_mesa_banho**, and **esporte_lazer**  
- Category distribution shows a long tail of niche product groups  

## 💳 Payment Behaviour
- **Credit card** dominates with 75% of all transactions  
- **Boleto** accounts for ~20%  
- Voucher and debit card usage is minimal  

## 🚚 Delivery & Order Value
- Most orders fall under **£200**  
- Delivery times cluster between **10–20 days**  
- Longer delivery times correlate with inter‑state shipments  

---

# 🛠️ Tools & Technologies

- **Power BI Desktop**  
- **Power Query**  
- **DAX**  
- **Star Schema Modelling**  
- **GitHub** for version control  
- **CSV / Flat Files**  

---

# 📁 Repository Structure

📦 ecommerce-analytics-dashboard/ 
├── 📁 data/          # Raw and cleaned datasets 
├── 📁 Pipeline/      # Data- cleaning/ingestion , transformation
├── 📁 pbix/          # Power BI project file 
├── 📁 Visuals/       # Dashboard screenshots │ 
└── 📄 README.md      # Project documentation

---

# 🧠 What I Learned

- How to design a clean, scalable star schema  
- How to build KPI measures using DAX  
- How to structure a multi‑page dashboard  
- How to communicate insights visually  
- How to identify dataset limitations and adjust analysis  
- How to create a portfolio‑ready BI project  

---

# 📬 Contact

**Teejay — Data Analyst | Power BI | Python | SQL**  
LinkedIn: [linkedin.com/in/israel-obiomah-6ba609253] 


[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![GitHub](https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/teejay7729)