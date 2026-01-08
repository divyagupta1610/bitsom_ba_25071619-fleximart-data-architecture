# FlexiMart Data Architecture Project

**Student Name:** DIVYA GUPTA 
**Student ID:** bitsom_ba_25071619
**Email:** divyagupta16oct@gmail.com
**Date:** 07 January 2026  

---

## Project Overview
This project implements an end-to-end data architecture solution for FlexiMart, covering transactional data processing, NoSQL analysis, and data warehousing. It includes an ETL pipeline, business analytics queries, MongoDB-based product catalog analysis, and a star-schema data warehouse with OLAP queries.

---

## Repository Structure
```
studentID-fleximart-data-architecture/
├── README.md
├── part1-database-etl/
│   ├── etl_pipeline.py
│   ├── schema_documentation.md
│   ├── business_queries.sql
│   ├── data_quality_report.txt
│   └── data/
│       ├── customers_raw.csv
│       ├── products_raw.csv
│       └── sales_raw.csv
├── part2-nosql/
│   ├── nosql_analysis.md
│   ├── mongodb_operations.js
│   └── products_catalog.json
└── part3-datawarehouse/
    ├── star_schema_design.md
    ├── warehouse_schema.sql
    ├── warehouse_data.sql
    └── analytics_queries.sql
```
---

## Technologies Used
- Python 3.x, pandas, mysql-connector-python  
- MySQL 8.0  
- MongoDB 6.0 
- SQL
- JavaScript (MongoDB Shell) 

---

## Setup Instructions

### Database Setup
```bash
# Create databases
mysql -u root -p -e "CREATE DATABASE fleximart;"
mysql -u root -p -e "CREATE DATABASE fleximart_dw;"

# Run ETL Pipeline
python part1-database-etl/etl_pipeline.py

# Run Business Queries
mysql -u root -p fleximart < part1-database-etl/business_queries.sql

# Data Warehouse Scripts
mysql -u root -p fleximart_dw < part3-datawarehouse/warehouse_schema.sql
mysql -u root -p fleximart_dw < part3-datawarehouse/warehouse_data.sql
mysql -u root -p fleximart_dw < part3-datawarehouse/analytics_queries.sql

### MongoDB Setup
mongosh < part2-nosql/mongodb_operations.js
```
## Key Learning 
This project strengthened my understanding of ETL pipelines, relational and NoSQL database design, and data warehousing concepts. I learned how to design star schemas, write analytical SQL queries, and evaluate database technologies based on use cases.

## Challenges Faced
1. Handling duplicate and inconsistent data during ETL, resolved using data cleaning and validation logic.

2. Designing analytical queries with correct aggregations and window functions, resolved through careful schema alignment.

## Submission

https://github.com/divyagupta1610/bitsom_ba_25071619-fleximart-data-architecture


