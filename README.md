# 📊 SQL Data Warehouse & Power BI Analytics Project

> An end-to-end Data Warehouse built using **MySQL** following the **Medallion Architecture (Bronze → Silver → Gold)**, with an interactive **Power BI Dashboard** for business analytics and reporting.

---

# 📖 Project Overview

Organizations often collect data from multiple systems, making it difficult to generate consistent and reliable reports.

This project demonstrates how raw CRM and ERP data can be transformed into a clean, business-ready analytical model using modern data warehousing principles.

The project includes:

- Data ingestion from CSV files
- ETL pipeline using SQL
- Data cleaning and validation
- Dimensional Modeling (Star Schema)
- Business-ready Gold Layer
- Business Analysis using SQL
- Interactive Power BI Dashboard

---

# 🏗️ Architecture

```
                   CSV Files
                       │
                       ▼
               Bronze Layer
              (Raw Ingestion)
                       │
                       ▼
               Silver Layer
     (Data Cleaning & Standardization)
                       │
                       ▼
                Gold Layer
      (Business Views / Star Schema)
                       │
                       ▼
              Business Analysis
                  (SQL Queries)
                       │
                       ▼
              Power BI Dashboard
```

---

# ⭐ Data Warehouse Architecture

The project follows the **Medallion Architecture**.

## Bronze Layer

Purpose:

- Store raw source data
- Preserve original records
- No transformations

Tables:

- crm_cust_info
- crm_prd_info
- crm_sales_details
- erp_cust_az12
- erp_loc_a101
- erp_px_cat_g1v2

---

## Silver Layer

Purpose:

- Data Cleaning
- Standardization
- Validation
- Business Rule Implementation

Transformations include:

- Removing duplicate customers
- Standardizing Gender
- Standardizing Marital Status
- Cleaning Product Information
- Extracting Product Categories
- Correcting Invalid Sales Values
- Handling Invalid Dates
- Cleaning ERP Data
- Calculating Product End Dates using LEAD()

---

## Gold Layer

Purpose:

Create a business-friendly analytical model.

Views:

- dim_customers
- dim_products
- fact_sales

Features:

- Business-friendly column names
- Star Schema
- Optimized for analytics
- Ready for Power BI

---

# ⭐ Star Schema

```
                     dim_customers
                           │
                           │
                           │
dim_date ─────────── fact_sales ─────────── dim_products
```

Fact Table

- fact_sales

Dimensions

- dim_customers
- dim_products
- dim_date *(future enhancement)*

---

# ⚙️ ETL Pipeline

The ETL pipeline consists of three stages.

## Extract

- Import CSV files into Bronze Layer

## Transform

- Data Cleaning
- Duplicate Removal
- Data Validation
- Business Rule Implementation
- Data Standardization

## Load

- Populate Gold Views for Business Intelligence

---

# 📈 Business Analysis

Example KPIs generated using SQL:

- Total Revenue
- Total Orders
- Total Customers
- Average Order Value
- Revenue by Product Category
- Revenue by Country
- Revenue by Gender
- Top Selling Products
- Top Customers
- Monthly Revenue Trend

---

# 📊 Power BI Dashboard

The dashboard provides interactive business insights including:

### Executive KPIs

- Total Revenue
- Total Orders
- Total Customers
- Average Order Value

### Revenue Analysis

- Revenue by Year
- Revenue by Category
- Revenue by Country

### Product Analysis

- Top Selling Products

### Customer Analysis

- Revenue by Gender

*(Add screenshots below once your dashboard is complete.)*

---

# 🛠️ Tech Stack

### Database

- MySQL

### BI Tool

- Power BI

### Languages

- SQL
- DAX

### Concepts

- ETL
- Data Warehousing
- Medallion Architecture
- Star Schema
- Data Cleaning
- Dimensional Modeling
- Business Intelligence

---

# 📁 Project Structure

```
SQL-Data-Warehouse
│
├── datasets
│
├── scripts
│   ├── bronze
│   ├── silver
│   ├── gold
│   └── analysis
│
├── dashboard
│   ├── dashboard.pbix
│   └── dashboard.png
│
├── docs
│   ├── architecture.png
│   ├── star_schema.png
│   └── data_model.png
│
├── README.md
└── LICENSE
```

---

# 🚀 Key Learnings

Throughout this project I learned:

- Designing a Data Warehouse from scratch
- Building ETL pipelines using SQL
- Data Cleaning and Standardization
- Implementing Business Rules
- Designing Star Schemas
- Writing Analytical SQL Queries
- Creating Interactive Power BI Dashboards
- Transforming raw operational data into actionable business insights

---

## Power BI Dashboard

<img width="1919" height="973" alt="image" src="https://github.com/user-attachments/assets/09bdd209-780c-4c02-aa02-80658f46ebb0" />


---

# 🔮 Future Enhancements

- Add Date Dimension
- Incremental Data Loading
- Stored Procedures for ETL
- Data Quality Monitoring
- Scheduled ETL Jobs
- Azure Data Factory Integration
- Snowflake/Azure Synapse Migration
- CI/CD for SQL Deployment

---

# 👨‍💻 Author

**Srinath Vulkunda**

If you found this project useful, feel free to ⭐ the repository.
