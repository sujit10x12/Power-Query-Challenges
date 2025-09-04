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

**Challenge:**
 - Create another CSV query to fetch data for 1Z & Transform the same
   
   <img width="1280" height="720" alt="1z - Basic Transformation" src="https://github.com/user-attachments/assets/d68502f9-03e3-4bf4-8a58-8ebe1a1ee7c5" />
   

## Steps Overview

### Part 1 – Data Cleaning & Reshaping
- Removed column number references and header rows.  
- Promoted first row to headers.  
- Deleted unnecessary columns (`Ref1`, `Ref2`).  
- Replaced blanks with nulls and filled down missing values.  
- Unpivoted date columns, then pivoted the **Metric** column (no aggregation).  
- Renamed the **Attribute** column for clarity.  

### Part 2 – Date Handling & Filtering
- Created a backup of the Date column (**DateBackup**).  
- Parsed the Date column while keeping errors, then deleted the original Date column.  
- Filtered out years **2017 and 2018** from DateBackup.  
- Filtered **Store** column to keep only values **1 and 2**.  
- Renamed **DateBackup** to **Quarter**.  
- Adjusted data types appropriately.  

## Outcome
The final dataset is cleaned, reshaped, and ready for analysis, with clear quarters, relevant stores, and structured metrics.

---

## 2. Extracting Data

Extract meaningful content from raw data using text and column manipulation techniques.

**Skills Covered:**
- ✅ Extract Characters from Text  
- ✅ Remove Blank Columns from Excel  
- ✅ Extract Text Using Delimiters  
- ✅ Split Columns by Position  
- ✅ Split Columns into Individual Rows  
- ✅ Add Prefixes to Columns  

---

## 3. Consolidating Data

Combine and summarize data from multiple sources to gain insights.

**Skills Covered:**
- ✅ Identify Month of Each Row  
- ✅ Group Rows by Month  
- ✅ Aggregate Similar Columns  
- ✅ Perform Table Joins  
- ✅ Combine Data from Multiple Excel Files  
- ✅ Extract Info from File Name  

---

## 4. Dealing with Errors

Handle common issues and build dynamic, error-resistant queries.

**Skills Covered:**
- ✅ Filter Errors  
- ✅ Create Calculated Columns  
- ✅ Deal with Different Date Regions  
- ✅ Create Conditional Columns  
- ✅ Create Parameters to Save Settings  
- ✅ Adapt Queries Using Parameters  

---
