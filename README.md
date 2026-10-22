# Decodelabs Internship: Project 1 - Data Cleaning & Preprocessing

This repository contains the dataset, scripts, and documentation for Project 1 of the DecodeLabs Data Analytics Internship. The primary objective of this project was to establish a rigorous data cleaning pipeline on raw transactional data, resolving inconsistencies, formatting anomalies, and structural issues.

## Project Overview

Raw data in e-commerce workflows is frequently messy, inconsistent, and unstructured. This project takes a dataset of 1,200 unique sales orders and runs a complete cleaning and preprocessing routine to ensure downstream analytical models or database queries produce accurate results.

### Project File Inventory

* **`Dataset for Data Analytics.xlsx`**: The finalized, clean spreadsheet containing the preprocessed transaction table.
* **`DATA ANALYTICS p1.pdf`**: The official training kit and requirements specification.
* **`report.docx`**: A detailed report outlining the step-by-step cleaning operations.

---

## Cleaning & Preprocessing Pipeline

The data preparation was executed using Python (`pandas` and `openpyxl`) to ensure exact, reproducible styling and structural conversion.

### 1. Data Integrity and Duplicate Auditing
* **Duplicate Scan**: Evaluated the 1,200 rows of transaction records for exact-row duplicates.
* **Primary Key Audit**: Verified the uniqueness of the `OrderID` column (primary key).
* **Result**: The dataset contains zero duplicate rows and zero primary key conflicts, ensuring that all 1,200 records represent unique sales transactions.

### 2. Missing Value Imputation
* **Audit Finding**: The `CouponCode` column (column L) contained 309 null values.
* **Imputation Strategy**: Rather than deleting these records (which would discard valuable purchase data), all null values were imputed with the string `"None"`. This maintains structural integrity for future queries and grouping.

### 3. Data Format Standardization
* **Currency Formatting**: The columns `UnitPrice` (column F) and `TotalPrice` (column N) were converted from General style to standard currency notation: `"$#,##0.00"`.
* **Date Consistency**: Validated that all date strings are correctly parsed in the standard ISO format (`YYYY-MM-DD`).
* **Logic Validation**: Cross-checked that `TotalPrice = Quantity * UnitPrice` across all 1,200 records. All rows passed with zero mathematical discrepancies.

### 4. Structured Table Conversion
* **Conversion**: The cell range `A1:N1201` was converted into a formal, named Excel Table: `OrdersData`.
* **Styling**: Applied `TableStyleMedium2` (blue banded rows) to improve visibility.
* **Filters**: Enabled header sorting and filter dropdowns, allowing end-users to search, sort, and segment the transactional data on the fly.

---

## Technology Stack & Tools

* **Excel engine**: Openpyxl (Python library for writing Excel files without corruption)
* **Data manipulation**: Pandas
* **Format standard**: standard Microsoft Excel XML (OpenXML)

## On my portfolio

- Case study: [ghostiemoh.com/#work](https://ghostiemoh.com/#work)
