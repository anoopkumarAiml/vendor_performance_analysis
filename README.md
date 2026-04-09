# Vendor Performance Analysis

## Project Overview

This project analyzes vendor and brand performance in a retail inventory environment. The goal is to identify vendors and brands contributing most to revenue and profitability while detecting underperforming vendors, inefficient inventory patterns, and pricing issues.

The project demonstrates an end-to-end analytics workflow using **Python, SQL, and Power BI**.

The workflow includes data ingestion, database storage, data aggregation, exploratory analysis, and dashboard visualization.

---

## Business Problem

Retail companies often face challenges related to inefficient inventory management, vendor dependency, and poor pricing strategies. These problems can lead to reduced profitability and high inventory holding costs.

This project aims to solve the following problems:

• Identify underperforming brands that may require pricing or promotional adjustments
• Determine top vendors contributing to overall sales and gross profit
• Analyze the impact of bulk purchasing on unit cost efficiency
• Evaluate inventory turnover to reduce holding costs
• Investigate profitability differences between high-performing and low-performing vendors

---

## Project Architecture

The project follows the following workflow:

Business Problem
↓
Data Collection (CSV files)
↓
Data Cleaning and Processing using Python
↓
Load Data into MySQL Database
↓
Create Aggregated Analytical Tables using SQL
↓
Exploratory Data Analysis using Jupyter Notebook
↓
Build Interactive Dashboard using Power BI
↓
Generate Business Insights

---

## Data Processing

Raw CSV datasets were processed using Python scripts.

The ingestion pipeline performs the following tasks:

• Reads raw CSV files
• Cleans and prepares the data
• Loads the data into a MySQL database using SQLAlchemy
• Logs the ingestion process for monitoring

After loading the raw tables into the database, SQL queries were used to create an aggregated dataset called:

**vendor_sales_summary**

This aggregated table summarizes vendor level performance including sales, purchases, profit metrics, and inventory indicators.

This dataset is later used for analysis and dashboard visualization.

---

## Exploratory Data Analysis

Exploratory analysis was performed using Jupyter Notebook to understand patterns such as:

• vendor contribution to total sales
• profitability distribution
• vendor dependency
• low performing brands
• sales vs profit margin relationships

These insights were used to design the final dashboard.

---

## Power BI Dashboard

An interactive Power BI dashboard was created to visualize vendor performance.

The dashboard provides insights into:

• Total Sales
• Total Purchases
• Gross Profit
• Profit Margin
• Vendor Purchase Contribution
• Top Vendors by Sales
• Top Brands by Sales
• Low Performing Vendors
• Profitability distribution analysis

The dashboard helps decision makers quickly identify vendors driving revenue and vendors requiring improvement.

---

## Project Structure

```
Vendor_Performance_Analysis
│
├── data
│   ├── begin_inventory.csv
│   ├── end_inventory.csv
│   ├── purchase_prices.csv
│   ├── vendor_invoice.csv
│   └── vendor_sales_summary.csv
│
├── notebooks
│   ├── 01_data_ingestion_demo.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   └── 03_vendor_performance_analysis.ipynb
│
├── scripts
│   ├── ingestion_db.py
│   └── get_vendor_summary.py
│
├── sql
│   └── vendor_summary.sql
│
├── dashboard
│   └── vendor_performance_dashboard.pbix
│
├── Output
│   └── dashboard_preview.png
│
├── requirements.txt
└── README.md
```

---

## Technologies Used

Python
Pandas
NumPy
SQL (MySQL)
SQLAlchemy
Power BI
Jupyter Notebook

---

## Note

Some large datasets such as **sales.csv** and **purchases.csv** were excluded from this repository due to GitHub file size limitations. The project structure and analytical workflow remain fully documented in this repository.

---

## Key Outcome

This project demonstrates how data engineering and analytics techniques can be used to transform raw operational data into actionable insights that help businesses improve vendor performance, optimize inventory management, and increase profitability.
