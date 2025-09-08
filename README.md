# 🏡 Nashville Housing Data Cleaning (SQL Server)

## 📌 Project Overview
This project focuses on **cleaning and transforming raw housing data** from the Nashville real estate dataset using **SQL Server**.  
The dataset initially contained inconsistencies such as missing values, unstandardized formats, and duplicates. The goal was to clean the data and prepare it for analysis and reporting.

---

## 🛠️ Key Steps in Data Cleaning

1. **Standardize Date Format**  
   - Converted `SaleDate` into a proper `DATE` format.  
   - Created a new column `SaleDateConverted` when needed.

2. **Populate Missing Property Addresses**  
   - Used **self-join** on `ParcelID` to fill missing `PropertyAddress` values.

3. **Split Address Columns**  
   - Broke down `PropertyAddress` into `Address` and `City`.  
   - Split `OwnerAddress` into `Address`, `City`, and `State`.

4. **Normalize "Sold as Vacant" Field**  
   - Replaced `'Y'` and `'N'` with `'Yes'` and `'No'`.

5. **Remove Duplicates**  
   - Implemented a `ROW_NUMBER()` CTE to identify and filter duplicate rows.

6. **Drop Unused Columns**  
   - Removed irrelevant fields (`OwnerAddress`, `TaxDistrict`, `PropertyAddress`, `SaleDate`) to simplify the dataset.

7. **(Optional) Importing Data**  
   - Demonstrated how to use `BULK INSERT` and `OPENROWSET` for loading CSV/Excel files into SQL Server.

---

## 📊 Results
- The dataset is now **clean, consistent, and analysis-ready**.  
- Address fields are standardized and structured.  
- Redundant and duplicate data is removed.  
- Easier integration into BI tools such as **Power BI** or **Tableau**.

---

## 🚀 Next Steps
- Build interactive dashboards to visualize housing trends.  
- Perform deeper analysis (pricing trends, neighborhood comparisons, etc.).  
- Automate cleaning steps with stored procedures or scheduled ETL jobs.
