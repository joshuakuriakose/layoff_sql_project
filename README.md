# Company Layoffs SQL Project

## Overview
This project demonstrates **SQL-based data cleaning and exploratory data analysis (EDA)** on a company layoffs dataset. The goal was to clean, standardize, and analyze the dataset to uncover trends in layoffs across companies, industries, and time periods.

## Dataset
The dataset includes the following fields:
- `company`: Name of the company
- `location`: City/region of the company
- `industry`: Industry sector
- `total_laid_off`: Number of employees laid off
- `percentage_laid_off`: Percentage of workforce laid off
- `date`: Date of layoff announcement
- `stage`: Company stage (startup, growth, etc.)
- `country`: Country of operation
- `funds_raised_millions`: Funding raised by the company in millions USD

## Project Steps

### 1. Data Cleaning
- Removed duplicate rows using `ROW_NUMBER()` and `DELETE`.
- Standardized text fields with `TRIM()` and cleaned inconsistent industry and country names.
- Converted date strings to proper `DATE` type using `STR_TO_DATE()`.
- Handled null and blank values; populated missing industry values using self-joins.
- Dropped unnecessary columns.

### 2. Exploratory Data Analysis (EDA)
- Calculated aggregate metrics like `SUM(total_laid_off)`, `AVG(percentage_laid_off)`, and `MAX`/`MIN`.
- Ranked companies by layoffs using `DENSE_RANK()`.
- Time-based analysis: monthly layoffs trends using `SUBSTRING(date,1,7)` and rolling totals with `SUM() OVER`.
- Analysis by company, industry, and funding stage.

## Key SQL Concepts
- Common Table Expressions (CTEs)
- Window functions (`ROW_NUMBER()`, `DENSE_RANK()`, `SUM() OVER`)
- Joins and self-joins
- Aggregations and grouping
- Data type conversion
- Data cleaning techniques

## Files
- `01_data_cleaning.sql`: All SQL scripts for data cleaning.
- `02_eda.sql`: SQL scripts for exploratory data analysis.

## Insights
Some example insights from the dataset:
- Top companies affected by layoffs.
- Industries most affected by layoffs.
- Month-wise and year-wise layoffs trends.
- Average layoffs by company stage.

## Tools
- MySQL / MariaDB

---

This project demonstrates **end-to-end SQL skills**, including cleaning, transformation, aggregation, and time-based analysis, making it suitable for data analyst or business intelligence portfolios.
