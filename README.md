#  E-Commerce Data Pipeline (End-to-End)

##  Project Overview
This project demonstrates a complete **end-to-end data pipeline** built using **Databricks, PySpark, and Delta Lake**.

The goal is to transform raw e-commerce data into **business-ready insights** using a layered architecture and visualize key performance metrics through a dashboard.

---

##  Business Problem
E-commerce companies generate large volumes of data daily, but raw data cannot be directly used for decision-making.

This project solves:
- Lack of visibility into revenue trends  
- Difficulty in identifying top customers and products  
- No clear understanding of category performance  
- Inefficient tracking of delivery performance  

---

##  Architecture (Medallion Architecture)

Bronze Layer → Silver Layer → Gold Layer

### 🔹 Bronze Layer (Raw Data)
- Ingest raw data from source  
- No transformations applied  
- Stored in Delta format  

### 🔹 Silver Layer (Cleaned Data)
- Data cleaning (null handling, duplicate removal)  
- Data type corrections  
- Joining multiple tables  
- Creation of a **fact table (sales_detail)**  

### 🔹 Gold Layer (Business Layer)
- Aggregated data for analytics  
- KPI generation  
- Optimized for dashboarding  

---

##  Dataset Used
Brazilian E-Commerce Public Dataset (Kaggle)

### Tables:
- customers  
- orders  
- order_items  
- products  

---

##  Data Modeling (Fact Table)

We created a **fact table (`sales_detail`)** by joining:

- customers → `customer_id`  
- orders → `order_id`  
- order_items → `order_id`  
- products → `product_id`  

This table is used to calculate all KPIs.

---

##  KPIs Implemented

-  Daily Revenue  
-  Monthly Revenue  
-  Top Customers  
-  Top Products  
-  Category Performance  
-  Average Delivery Time  

---

##  Dashboard
An interactive dashboard was created in Databricks using Gold layer tables.

### Key Features:
- Line chart for revenue trends  
- Bar charts for comparisons  
- Pie chart for category distribution  
- KPI cards for quick insights  

---

##  Tools & Technologies

- Databricks  
- PySpark  
- Delta Lake  
- SQL  
- Databricks Workflows  
- Databricks Dashboard  

---

##  Pipeline Workflow

1. Bronze → Ingest raw data  
2. Silver → Clean and transform data  
3. Gold → Generate KPIs  
4. Dashboard → Visualize insights  

---

##  Key Features

- End-to-end pipeline implementation  
- Scalable data processing using PySpark  
- Reliable storage using Delta Lake (ACID transactions)  
- Automated workflow using Databricks Jobs  
- Business-focused dashboard  

---

##  Team Contribution

- Member 1 → Bronze Layer (Data Ingestion)  
- Member 2 → Silver Layer (Data Transformation)  
- Vamsi Krishna Akula → Gold Layer (KPIs & Analytics)  

---

##  Learnings

- Understanding Medallion Architecture  
- Building scalable data pipelines  
- Data cleaning and transformation using PySpark  
- Designing fact tables and KPIs  
- Creating business dashboards  

---

##  Conclusion

This project demonstrates how raw data can be transformed into **actionable business insights** using modern data engineering tools and practices.

---
