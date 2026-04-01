# E-Commerce Analytics Data Pipeline

This project is an end-to-end data engineering pipeline for processing raw e-commerce data into clean, analysis-ready datasets and a Power BI dashboard.

---

## 🚀 Project Overview

The pipeline takes raw CSV files (orders, customers, products), cleans and transforms them using Python, and outputs processed datasets for analytics. These cleaned files are then used to build a Power BI dashboard.

This project demonstrates:
- Data cleaning and transformation
- Feature engineering
- Analytical modelling
- Dashboard creation

---

## 🧱 Architecture

Raw Data (CSV)
      ↓
Python ETL (cleaning, transformations)
      ↓
Processed Data (clean CSV outputs)
      ↓
Power BI Dashboard (DAX, visuals, insights)

---

## 🛠 Technologies Used

- Python (Pandas)
- CSV storage
- Power BI
- Git & GitHub

---

## 📂 Project Structure

ecommerce-analytics-pipeline/
│
├── data/
│   ├── raw/               (original CSV files)
│   └── processed/         (cleaned output files)
│
├── pipeline/
│   ├── clean_data.py
│   ├── transform.py
│   └── pipeline.py
│
├── powerbi/
│   └── dashboard.pbix     (Power BI file)
│
└── README.md

---

## 🔧 ETL Pipeline Steps

### 1. Extract
Loads raw CSV files:
- orders.csv
- customers.csv
- products.csv

### 2. Transform
- Remove missing values
- Fix data types
- Standardize categories
- Create revenue, profit, margin columns
- Join tables
- Create summary tables

### 3. Load
Outputs cleaned datasets into:

data/processed/
- cleaned_orders.csv
- cleaned_customers.csv
- cleaned_products.csv
- sales_summary.csv

These files are used in Power BI.

---

## 📊 Power BI Dashboard

### Key Metrics
- Total Revenue
- Total Profit
- Average Order Value
- Total Customers
- Repeat Customer Rate

### Visuals
- Revenue by Month
- Top 10 Products
- Profit by Category
- Customer Segments

### Data Model
Customers (1) → (∞) Orders  
Products (1) → (∞) Orders

### Example DAX Measures

Total Revenue = SUM(Orders[Revenue])  
Total Profit = SUM(Orders[Profit])  
AOV = DIVIDE([Total Revenue], DISTINCTCOUNT(Orders[OrderID]))

---

## ▶️ How to Run the Project

### 1. Clone the repository
git clone https://github.com/teejay7729/ecommerce-analytics-pipeline.git

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run the ETL pipeline
python pipeline/pipeline.py

### 4. Open Power BI
Load the cleaned CSVs from data/processed/

---

## 📘 Data Dictionary

OrderID – unique order identifier  
CustomerID – customer reference  
ProductID – product reference  
Quantity – units purchased  
Price – unit price  
Revenue – Quantity × Price  
Profit – Revenue − Cost  
OrderDate – date of purchase  

---

## 📈 Future Improvements

- Add SQL database storage  
- Add API ingestion  
- Automate pipeline with Airflow  
- Deploy dashboard to Power BI Service  

---

## 👤 Author

Teejay  
Data Engineering & Analytics Enthusiast  
London, UK