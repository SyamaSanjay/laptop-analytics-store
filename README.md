[README_md](https://github.com/user-attachments/files/31522874/README.md)
# Laptop Analytics Store — Business Analytics Capstone Project

**Grade: 100/100** | Applied Business Intelligence and Analytics, Macromedia University of Applied Sciences

## Overview

An end-to-end business analytics project simulating a niche online laptop retail business. The goal was to help customers find the best value for money laptops and support management pricing/assortment decisions using a data driven approach across Excel, SQL, and Python.

## Business Problem

The laptop market is highly fragmented hundreds of models vary widely in specs and price, making it hard for customers to compare options and for retailers to price competitively. This project builds an analytics foundation to answer:

- How are laptop prices distributed, and how much do gaming vs. non-gaming laptops differ in price?
- Which brands and spec combinations sit in the budget / mid-range / premium segments?
- Which laptops offer the best performance per unit price?
- Can laptop price be predicted from a small set of key specs?

## Approach

**1. Data Cleaning & Feature Engineering (Python + Excel)**
- Cleaned a public Kaggle laptop dataset (1,600+ listings) using Pandas
- Parsed unstructured text fields (storage, RAM, display, processor) into structured numeric fields (`RAM_GB`, `SSD_GB`, `ScreenInch`, etc.)
- Engineered features including `GamingFlag`, `SpecBand`, and a value-for-money metric (`score_per_1000`)

**2. Statistical Analysis & Dashboards (Excel)**
- Descriptive statistics on price distribution (mean, median, std dev, skewness)
- Two-sample t-test comparing gaming vs. non-gaming laptop prices (statistically significant premium confirmed, p < 0.001)
- Dynamic Excel dashboard with slicers (brand, RAM, gaming flag, release year)

**3. Database Design & SQL Analysis**
- Normalized the dataset to 3NF (separate Brand, OS, Processor, Laptop tables)
- Built a MySQL analytical table and wrote 10+ SQL queries answering specific business questions (pricing by brand, value for-money ranking, high-spec brand identification)
- Built a Power Pivot star schema in Excel for multi-dimensional slicing

**4. Predictive Modeling (Python)**
- Trained a Random Forest Regression model (scikit-learn) to predict laptop price from brand, spec score, RAM, SSD, screen size, gaming flag, and release year
- **Test R²: 0.67** | **Average % error: ~11%** | **Median absolute error: ~₹4,945**
- Visualized model performance with actual-vs-predicted scatter plots, error distribution histograms, and feature importance charts

## Key Findings

- Laptop prices are highly dispersed and right-skewed a small number of high-end models pull the average up
- Gaming laptops carry a statistically significant price premium over non-gaming laptops, consistent with higher spec scores
- RAM size is the strongest single predictor of price (highest feature importance in the Random Forest model)
- The pricing model can reasonably flag over- or under-priced laptops relative to their specs useful for a "pricing assistant" use case

## Tools Used

`Python (Pandas, scikit-learn)` · `Excel (PivotTables, Power Pivot, Dashboards)` · `MySQL` · `Matplotlib / Seaborn`

## Files in This Repo

- `Laptop_Project.ipynb` — full Python notebook (data cleaning, modeling, visualizations)
- `laptop_dss.sql` — SQL schema, normalization, and analytical queries
- `Laptop_Analytics_Store_Report.pdf` full written project report
- `images/` dashboard screenshots and chart exports

## Author

Syama Sanjay Reddy Vanga — M.A. Business Management, Macromedia University of Applied Sciences
