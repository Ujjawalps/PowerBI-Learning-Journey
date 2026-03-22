# Data Cleaning in Power BI (Power Query)

This section covers how to clean and prepare raw data before creating dashboards.

---

## 🔹 Why Data Cleaning is Important

Raw data is often:
- Incomplete (missing values)
- Inconsistent (wrong formats)
- Messy (extra columns, duplicates)

Cleaning ensures:
- Accurate analysis
- Better performance
- Correct insights

---

## 🔹 Power Query (Your Cleaning Tool)

Power BI uses Power Query for data transformation.

To open:
Home → Transform Data

---

## 🔹 Common Cleaning Steps

### 1. Remove Null / Blank Values
- Home → Remove Rows → Remove Blank Rows

---

### 2. Change Data Types
- Text → Number / Date
- Important for correct calculations

---

### 3. Remove Unnecessary Columns
- Right-click → Remove

---

### 4. Rename Columns
- Double click column name → Rename

---

### 5. Filter Data
- Click dropdown → Select required values

---

### 6. Remove Duplicates
- Select column → Remove duplicates

---

### 7. Replace Values
- Example: "N/A" → 0

---

## 🔹 My Learning Notes

- Always clean data before visualization
- Never modify original dataset
- Use Power Query instead of Excel edits

---

## 🔹 Example Workflow

1. Import dataset  
2. Open Power Query  
3. Clean data (nulls, types, duplicates)  
4. Apply changes  
5. Build visuals  

---

## 🔹 Beginner Mistakes

- Skipping cleaning  
- Wrong data types  
- Not checking duplicates  
