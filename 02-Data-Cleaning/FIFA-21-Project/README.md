# ⚽ FIFA 21 Data Cleaning Project (Power BI) 

## 📌 Overview
[click here for guide](https://medium.com/@jerryade75/data-cleaning-in-microsoft-power-bi-fifa-21-dataset-a910eb510486)

This project focuses on cleaning and transforming the FIFA 21 dataset using **Power BI (Power Query Editor)**.
The raw dataset contained inconsistent formats, mixed units, and messy text fields, which were transformed into a structured, analysis-ready dataset.

---

## 🎯 Objectives

* Clean and standardize messy real-world data
* Convert mixed units into consistent numerical formats
* Handle missing and inconsistent values
* Prepare dataset for further analysis and dashboard building

---

## 📂 Project Structure

```
02-Data-Cleaning/
 ├── FIFA-21-Project/
 │    ├── raw-data.csv
 │    ├── cleaned-data.csv
 │    ├── screenshots/
 │    ├── README.md
```

---

## 🧹 Data Cleaning Steps

### 1. Height Column

* Mixed formats: `5'10"` and `180cm`
* Converted all values to **centimeters**
* Used column splitting and conditional logic

---

### 2. Weight Column

* Mixed formats: `kg` and `lbs`
* Converted all values to **kilograms**
* Applied conversion:

  * `lbs → kg` using multiplier `0.453592`

---

### 3. Value, Wage, Release Clause

* Formats included:

  * `€103.5M`, `€560K`, `€900`, `€0`
* Removed currency symbols and handled suffixes:

  * `M → ×1,000,000`
  * `K → ×1,000`
* Converted all to **numeric EUR values**

---

### 4. Hits Column

* Mixed values: `445`, `1.2K`
* Converted all to numeric format:

  * `1.2K → 1200`

---

### 5. Contract Column

* Contained multiple formats:

  * `2019 - 2025`
  * `Dec 31, 2020 On Loan`
  * `Free`

Created:

* `Contract_Type` → Permanent / Loan / Free
* `StartYear`
* `EndYear`

Handled:

* Loan dates using `Date.FromText()`
* Extracted year using `Date.Year()`

---

### 6. Loan Date End

* Contained blanks and dates
* Blanks interpreted as **not on loan**

---

### 7. Data Type Fixing

* Converted:

  * Numeric columns → Whole/Decimal numbers
  * Date columns → Date type
  * Text columns → Cleaned and trimmed

---

### 8. Column Cleanup

* Removed:

  * Intermediate/helper columns
  * Duplicate columns
* Retained only analysis-relevant fields

---

## 🔄 Before vs After

- Raw data contained mixed units and inconsistent formats  
- Cleaned data is standardized and ready for analysis  

(See screenshots folder for visual comparison)

---

## ✅ Final Output

Clean dataset with:

* Consistent units
* Numeric values for calculations
* Structured categorical and date fields

---

## 🧠 Key Learnings

* Handling **mixed-format columns**
* Converting **text-based numbers (K/M)**
* Using **conditional logic in Power Query**
* Importance of **data types in analysis**
* Building a clean **ETL pipeline**

---

## 🚀 Next Step

This cleaned dataset will be used to build an **interactive Power BI dashboard** for player analysis.

---

## 📸 Screenshots

All transformation steps are documented in the `/screenshots` folder.

---

## 🛠 Tools Used

* Microsoft Power BI
* Power Query Editor

---

## 👨‍💻 Author

*ujjawalps*

---
