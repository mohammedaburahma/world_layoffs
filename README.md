# 📊 Layoffs Data Analysis (MySQL Project)

## 📌 Project Overview

This project focuses on analyzing global layoffs data using **MySQL**.
The workflow includes **data cleaning, transformation, and exploratory data analysis (EDA)** to uncover trends and insights about layoffs across companies, industries, and time.

---

## 🧹 Data Cleaning Process

The raw dataset contained:

* Duplicate records
* Inconsistent formatting
* Missing and null values
* Incorrect data types

### Key Cleaning Steps:

* **Created staging tables** to preserve raw data
* **Removed duplicates** using `ROW_NUMBER()` with CTEs
* **Standardized text fields**:

  * Trimmed company names
  * Unified industry labels (e.g., "Crypto")
  * Cleaned country names
* **Converted date column** from text → `DATE` format
* **Handled missing values**:

  * Filled missing industries using self-join logic
  * Removed rows with no layoff information
* **Dropped helper columns** after cleaning (`row_num`)

---

## 🔍 Exploratory Data Analysis (EDA)

### 📈 General Insights

* Identified **maximum layoffs** and **full company layoffs (100%)**
* Determined **date range** of the dataset

### 🏢 Company Analysis

* Total layoffs per company
* Average percentage layoffs per company
* Top companies by layoffs per year (using `DENSE_RANK()`)

### 🌍 Industry & Country Analysis

* Total layoffs by industry
* Total layoffs by country

### 📅 Time-Based Analysis

* Yearly layoffs trends
* Monthly layoffs aggregation
* **Rolling total layoffs over time** using window functions

### 🚀 Advanced SQL Techniques Used

* **CTEs (Common Table Expressions)**
* **Window Functions**:

  * `ROW_NUMBER()`
  * `SUM() OVER()`
  * `DENSE_RANK()`
* **Aggregations** (`SUM`, `AVG`, `MAX`)
* **Date functions** (`YEAR`, `STR_TO_DATE`)

---

## 📊 Key Insights

* Certain companies experienced **complete layoffs (100%)**, often despite high funding
* Layoffs are concentrated in specific **industries and countries**
* Clear **spikes in layoffs over time**, visible through rolling totals
* Top companies contributing to layoffs change **year by year**

---

## 🛠️ Tools Used

* **MySQL**

---