# ⚙️ Power Query Fundamentals – CFI Course

<img width="1584" height="396" alt="banner" src="images/banner.png" />

Welcome!  
This repository contains my **hands-on work** from the **Power Query Fundamentals** course offered by **Corporate Finance Institute (CFI)**.  

It covers core **data preparation techniques** including:
- Data transformation  
- Data extraction  
- Data consolidation  
- Error handling  

using **Power Query in Excel**.

---

## 🛠 Tools Used
- Microsoft Excel (Power Query Editor)

---

## 📂 Data Folder
This folder contains all the datasets I used to complete the challenges.  
It also includes other exercise datasets that were part of the practice and learning process.  

📑 The full Excel workbook containing all solutions is available here.

---

## 🧠 Challenges

### 1. Basic Transformations (File 1Z)
**⚔️ Challenge**  
Clean and reshape raw CSV data into a structured format for analysis.  

**🔢 Steps Overview**
- Removed top/bottom rows (extra notes/headers).  
- Promoted headers & removed unnecessary columns.  
- Replaced blanks → null, filled down values.  
- Unpivoted & pivoted columns to reshape data.  
- Parsed & filtered dates, retained errors.  
- Adjusted data types.  

**📌 Outcome**  
- Quarterly Sales & Margin data  
- Clean categories and store references  
- Structured format ready for reporting and analysis  

---

### 2. Extracting Data (File 2Z)
**⚔️ Challenge**  
Transform the **Duty Free Margins Dataset B** into a clean, structured dataset.  

**🔢 Steps Overview**
- Removed non-data rows.  
- Split & promoted headers.  
- Standardized Division/Department.  
- Expanded Brands into rows, cleaned text.  
- Reshaped quarterly columns into rows.  

**📌 Outcome**  
- Division, Department, Supplier, Brand, Quarter, Margin  
- Clean, standardized, and ready for margin analysis  

---

### 3. Consolidating Data (File 3Z)
**⚔️ Challenge**  
Aggregate daily sales and margin data into a **monthly summary**.  

**🔢 Steps Overview**
- Summed manager sales.  
- Calculated margins.  
- Transformed dates to first of the month.  
- Grouped by month.  

**📌 Outcome**  
- Monthly total sales and margins aggregated across all managers  

---

### 4. Categorizing Sales Data (File 4Z)
**⚔️ Challenge**  
Transform raw sales data by mapping category codes into readable labels.  

**🔢 Steps Overview**
- Added conditional column mapping (ALC → Alcohol, TOB → Tobacco, etc.).  
- Filtered null sales.  
- Converted date formats and adjusted types.  

**📌 Outcome**  
- Clean, categorized sales dataset  
- Proper labels, valid dates, numeric sales values  

---

## 📝 Assessments

### Assessment A – Sales Aggregation
- Cleaned and reshaped a wide-format CSV dataset.  
- Aggregated sales by Store and Attribute.  
- Filtered for Store 2.  

**📌 Outcome**: Summed sales for Store 2 in a clean long format.  

---

### Assessment B – GL Accounts & Transactions
**Part 1 – GL Accounts**  
- Unified GL Account Name (Balance Sheet + Income Statement).  
- Cleaned columns & types.  

**Part 2 – GL Transactions**  
- Cleaned and merged with GL Accounts.  
- Grouped by GL Account for totals.  

**📌 Output**: Structured GL dataset with account names and totals.  

---

### Assessment C – Multi-file Consolidation
- Connected to a folder of files.  
- Applied custom transform function.  
- Consolidated into one table.  
- Grouped by Category to sum values.  

**📌 Outcome**: Category-level summary from multiple source files.  

---

## 📜 Course Info

- **Course**: Data-Analysis-in-Excel 
- **Provider**: Corporate Finance Institute (CFI)
  
 [**My Certificate Credential URL**](https://www.coursera.org/account/accomplishments/specialization/ILAJLO8GFP1J)

![x](/images/certificate.jpg)

---
