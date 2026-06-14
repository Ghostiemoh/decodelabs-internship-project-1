# E-Commerce Data Cleaning & Preparation (Week 1)

This repository contains the dataset and documentation for the Week 1 data cleaning project. The objective was to clean, format, and structure a raw transaction dataset containing 1,200 orders to make it ready for analysis.

## Repository Contents

The following files are included in this project:

| File Name | Format | Description |
| :--- | :---: | :--- |
| `Dataset for Data Analytics.xlsx` | Excel Workbook | The finalized, cleaned dataset containing the formatted data table. |
| `Dataset for Data Analytics (1).xlsx` | Excel Workbook | The original reference raw dataset. |
| `report.docx` | Word Document | A detailed step-by-step report of the cleaning and preparation operations. |
| `DATA ANALYTICS p1.pdf` | PDF Document | The original project assignment and training kit. |

## Data Cleaning & Preparation Steps

The data cleaning pipeline involved the following operations:

1. **Null Values & Missing Data**:
   * Scanned the dataset for missing entries.
   * Identified 309 empty cells in the `CouponCode` column (L2:L1201).
   * Replaced the missing cells with the placeholder string `"None"` to maintain consistent data rows.

2. **Duplicates Audit**:
   * Audited the entire 1,200 row sheet for exact duplicate rows and duplicate `OrderID` entries.
   * Confirmed that the dataset contains zero duplicates or primary key conflicts.

3. **Data Format Correction**:
   * Formatted the pricing metrics, specifically `UnitPrice` (column F) and `TotalPrice` (column N), to display as standard currency (`$#,##0.00`).
   * Validated that the calculation $\text{TotalPrice} = \text{Quantity} \times \text{UnitPrice}$ holds true for all rows.

4. **Structured Table Conversion**:
   * Converted the range `A1:N1201` into a formal Excel Table named `OrdersData`.
   * Applied the `TableStyleMedium2` style (blue banded rows) with filter dropdowns enabled for easier data navigation and sorting.
