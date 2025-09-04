# ⚙️ Power Query Fundamentals – CFI Course
Welcome! This repository contains my hands-on work from the Power Query Fundamentals course offered by Corporate Finance Institute (CFI). Covers core data preparation techniques including data transformation, data extraction, data consolidation, and error handling using Power Query in Excel.

---

## 🧠 Challenges

1. [Basic Transformations](#1-basic-transformations)
2. [Extracting Data](#2-extracting-data)
3. [Consolidating Data](#3-consolidating-data)
4. [Dealing with Errors](#4-dealing-with-errors)

---

 ## 1. Basic Transformations

## Challenge
 - Create a new CSV query to fetch data for **File 1Z**.
 - Clean and reshape the raw CSV data into a structured format for analysis.
   
<img width="1280" height="720" alt="1z - Basic Transformation" src="https://github.com/user-attachments/assets/d68502f9-03e3-4bf4-8a58-8ebe1a1ee7c5" />
   

### Steps Overview
- **Removed Top/Bottom Rows** – Skipped the first 8 and last 2 rows (extra notes/headers).  
- **Promoted Headers** – Used the first row as column headers.  
- **Removed Columns** – Dropped `Ref1` and `Ref2`.  
- **Replaced Values** – Converted blanks in `Metric` to null.  
- **Filled Down** – Filled down `Metric` values for missing rows.  
- **Unpivoted Columns** – Converted date columns into row values.  
- **Renamed Columns** – Renamed `Attribute` → `Date`.  
- **Pivoted Columns** – Reshaped `Metric` column into separate fields (`Margin`, `Sales`).  
- **Duplicated Date Column** – Created a backup (`Date - Copy`).  
- **Parsed Date** – Converted `Date` into proper date format.  
- **Kept Errors** – Retained only rows with parsing errors (e.g., non-standard values).  
- **Removed Columns** – Dropped original `Date` column.  
- **Filtered Rows** – Removed 2017 and 2018 from the backup date column.  
- **Renamed Column** – Renamed `Date - Copy` → `Quarter`.  
- **Changed Types** – Converted fields into correct data types (numbers, integers, dates).   

### Outcome
The final dataset provides:  
- **Quarterly Sales & Margin** data  
- Clean categories and store references  
- Structured format ready for reporting and analysis 

---

## 2. Extracting Data

## Challenge
 - Create a new CSV query to fetch data for **File 2Z**.
 - Transform the *Duty Free Margins Dataset B* into a clean, structured dataset for analysis.

<img width="1280" height="720" alt="2z - Extracting Information" src="https://github.com/user-attachments/assets/14b5f93c-0bab-4a20-b6cb-fc171825104c" />
   
### Steps Overview
- **Removed Top Rows** – Skipped first 4 rows containing non-data.  
- **Split Column** – Broke `Column4` into multiple columns using `" | "` as delimiter.  
- **Promoted Headers** – Used first row as headers.  
- **Filtered Rows** – Removed nulls in `Product Details`.  
- **Split Product Details** – Divided into `Division` and `Department` by `-`.  
- **Extracted Last Characters** – Kept only the last character of `Division`.  
- **Added Prefix** – Added `"Division "` before the extracted character.  
- **Renamed Columns** – Assigned proper names (`Division`, `Department`).  
- **Uppercased Text** – Standardized `Department` values to uppercase.  
- **Split Brands** – Split `Brands` column by `;` into multiple rows.  
- **Trimmed Text** – Removed extra spaces from `Brands`.  
- **Filtered Rows** – Removed empty brand values.  
- **Unpivoted Other Columns** – Reshaped quarterly columns into row format.  
- **Renamed Columns** – `Attribute` → `Quarter`, `Value` → `Margin`.  
- **Changed Type** – Converted `Margin` column to number.  

### Outcome
The final dataset contains:  
- **Division, Department, Supplier, Brand, Quarter, Margin**  
- Cleaned, standardized, and reshaped values  
- Ready for analysis of duty-free margins by division, department, and brand. 

---

## 3. Consolidating Data

## Challenge
 - Create a new CSV query to fetch data for **File 3Z**.
 - Aggregate daily sales and margin data from multiple managers into a clean monthly summary.

<img width="1280" height="720" alt="3z Consolidating Data" src="https://github.com/user-attachments/assets/f2cae6c7-68e6-415c-8972-19daab60ceb2" />

### Steps Overview
- Added **Total Sales** by summing all manager sales.  
- Calculated individual manager margins (`Sales × Margin`) and total margin.  
- Cleaned up by removing intermediate calculation columns.  
- Transformed **Transaction Date** to the first day of the month.  
- Grouped data by month to compute **Total Sales** and **Total Margin**.  

### Outcome
The final dataset provides a **monthly view of total sales and margins**, aggregated across all managers.

---

## 4. Categorizing Sales Data – Exercise 4Z

**Challenge:**  
- Create a new CSV query to fetch data for **File 4Z**.
- Transform raw sales data by mapping category codes to readable labels and cleaning the dataset.

<img width="1280" height="720" alt="4z - Dealing with Errors" src="https://github.com/user-attachments/assets/dc1e4b56-c30e-4075-ac97-626411e1a17a" />

### Steps Overview
- Promoted headers for proper column names.  
- Added a conditional column to map category codes (`ALC`, `TOB`, `FD`, `LXY`, `PER`) into meaningful labels (Alcohol, Tobacco, Food, Luxury, Perfume, Other).  
- Filtered out rows with null `Sales` values.  
- Removed the original `Cat` column.  
- Converted `Date` column to **date format** (UK locale).  
- Adjusted data types for `Sales` (number) and `Category` (text).  

### Outcome
A **clean, categorized sales dataset** with proper labels, valid dates, and numeric sales values — ready for reporting or analysis.

---
