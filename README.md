# ⚙️ Power Query Fundamentals – CFI Course

<img width="1584" height="396" alt="banner" src="images/banner.png" />

Welcome! This repository contains my hands-on work from the Power Query Fundamentals course offered by Corporate Finance Institute (CFI). Covers core data preparation techniques including data transformation, data extraction, data consolidation, and error handling using Power Query in Excel.

---

## 🛠 Tools Used
  - Microsoft Excel (Power Query Editor)

---

## 📂 Data Folder

<a href="/dataset">This</a> folder contains all the datasets I used to complete the challenges.  
In addition, it also includes other exercise datasets that were part of the practice and learning process.

---

## 🧠 Challenges

1. [Basic Transformations](#1-basic-transformations)
2. [Extracting Data](#2-extracting-data)
3. [Consolidating Data](#3-consolidating-data)
4. [Dealing with Errors](#4-dealing-with-errors)

---

 ## 1. Basic Transformations

⚔️ Challenge
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

📌 Outcome
The final dataset provides:  
- **Quarterly Sales & Margin** data  
- Clean categories and store references  
- Structured format ready for reporting and analysis 

---

## 2. Extracting Data

⚔️ Challenge
 - Create a new CSV query to fetch data for **File 2Z**.
 - Transform the *Duty Free Margins Dataset B* into a clean, structured dataset for analysis.

<img width="1280" height="720" alt="2z - Extracting Information" src="https://github.com/user-attachments/assets/14b5f93c-0bab-4a20-b6cb-fc171825104c" />
   
🔢 Steps Overview
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

📌 Outcome
 - **Division, Department, Supplier, Brand, Quarter, Margin**  
 - Cleaned, standardized, and reshaped values  
 - Ready for analysis of duty-free margins by division, department, and brand. 

---

## 3. Consolidating Data

⚔️ Challenge
 - Create a new CSV query to fetch data for **File 3Z**.
 - Aggregate daily sales and margin data from multiple managers into a clean monthly summary.

<img width="1280" height="720" alt="3z Consolidating Data" src="https://github.com/user-attachments/assets/f2cae6c7-68e6-415c-8972-19daab60ceb2" />

🔢 Steps Overview
 - Added **Total Sales** by summing all manager sales.  
 - Calculated individual manager margins (`Sales × Margin`) and total margin.  
 - Cleaned up by removing intermediate calculation columns.  
 - Transformed **Transaction Date** to the first day of the month.  
 - Grouped data by month to compute **Total Sales** and **Total Margin**.  

📌 Outcome
  - The final dataset provides a **monthly view of total sales and margins**, aggregated across all managers.

---

## 4. Categorizing Sales Data – Exercise 4Z

⚔️ Challenge
- Create a new CSV query to fetch data for **File 4Z**.
- Transform raw sales data by mapping category codes to readable labels and cleaning the dataset.

<img width="1280" height="720" alt="4z - Dealing with Errors" src="https://github.com/user-attachments/assets/dc1e4b56-c30e-4075-ac97-626411e1a17a" />

🔢 Steps Overview
 - Promoted headers for proper column names.  
 - Added a conditional column to map category codes (`ALC`, `TOB`, `FD`, `LXY`, `PER`) into meaningful labels (Alcohol, Tobacco, Food, Luxury, Perfume, Other).  
 - Filtered out rows with null `Sales` values.  
 - Removed the original `Cat` column.  
 - Converted `Date` column to **date format** (UK locale).  
 - Adjusted data types for `Sales` (number) and `Category` (text).  

📌 Outcome
 - A **clean, categorized sales dataset** with proper labels, valid dates, and numeric sales values — ready for reporting or analysis.

---

## Assessment A – Sales Aggregation

⚔️ Challenge
Transform the raw CSV dataset with hundreds of columns into a clean, aggregated table, focusing on Store 2.

<img width="1280" height="720" alt="Assessment A" src="https://github.com/user-attachments/assets/231e3ee0-8d99-49e9-8fa3-d766e88e14b1" />


🔢 Steps Overview
 - Removed extra top rows and unnecessary columns.  
 - Promoted headers to column names.  
 - Unpivoted the dataset (from wide to long format).  
 - Filled down missing `Store` values and converted blanks to null.  
 - Converted `Value` to numeric type.  
 - Grouped data by **Store** and **Attribute**, calculating total **Sales**.  
 - Filtered to keep only **Store = 2**.  

📌 Outcome
  - The final dataset contains **summed sales by Store 2** across all attributes, reshaped into a clean long format for analysis.

---

## Assessment B 

⚔️ Challenge  
Prepare and standardize **GL Accounts** and **GL Transactions** data to build a clean chart of accounts, enrich account details, and summarize transactions for reporting.  

<img width="1280" height="720" alt="Assessment B" src="https://github.com/user-attachments/assets/1713d438-7dc8-4014-993d-4e14ea04e3fd" />

🔢 Steps Overview  

### 🔹 Part 1 – Clean & Prepare GL Accounts  
- Load the **GLAccounts** table from the Excel workbook.  
- Create a unified **GL Account Name** by combining *Balance Sheet Names* and *Income Statement Names*.  
- Remove unnecessary columns such as `Category` and `Statement`.  
- Convert `GL CODE` into the correct numeric data type.  

### 🔹 Part 2 – Clean, Merge & Aggregate GL Transactions  
- Load the **GL Transactions** sheet from the Excel workbook.  
- Remove extra rows and promote the first row as headers.  
- Drop unneeded columns such as `ID`, `Company`, `Date`, and `User`.  
- Ensure `GL Account` is stored as a number.  
- Merge transactions with the **GL Accounts table** (from Part 1) to attach account names.  
- Group data by **GL Account** and **GL Account Name**, summing up the transaction amounts.  

📌 Output 
  - A clean and structured dataset where each GL Account is linked with its name and total amount, ready for reporting and analysis.  

---


## Assessment C

⚔️ Challenge  
Combine multiple files from a folder, clean and transform the data, and produce a summarized view of values grouped by **Category (Cat)**.  

<img width="1280" height="720" alt="Assessment C" src="https://github.com/user-attachments/assets/23fa82aa-16d3-4709-8187-e4f5371d7e03" />

🔢 Steps Overview  

- **Load Data**  
  - Connected to the folder containing all source files.  
  - Filtered out hidden/system files.  
  - Invoked a custom transform function to process each file.  

- **Data Cleaning**  
  - Expanded the transformed data into one consolidated table.  
  - Removed unnecessary columns (`Source.Name`, `Metric`, `Store`, `Attribute`).  
  - Changed **Value** column to numeric.  

- **Data Transformation**  
  - Grouped rows by **Cat**.  
  - Summed the **Value** column to calculate totals per category.  

📌 Outcome  
  - A **consolidated dataset** from all files in the folder.  
  - A **category-level summary** showing total values for each **Cat**.  
  - Clean, structured data ready for reporting and analysis.  
