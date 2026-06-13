# Task-1-Isaac_Okoile
# Project 1: Data Integrity & Cleaning Audit
### DecodeLabs Data Analytics Internship

---

## 📌 What This Project Is About

This project focuses on Phase 2 of the Data Analytics process — The Integrity Audit.
The goal was to clean a raw sales dataset, identify and resolve data quality issues,
and document every change made before the data could be used for analysis.

The core principle: **One Truth, One Record.**

---

## 📊 Dataset Overview

| Property | Detail |
|----------|--------|
| Dataset | Sales Orders |
| Total Rows | 1,200 |
| Total Columns | 14 |
| Tool Used | Microsoft Excel & Power Query |

### Columns in Dataset:
- OrderID, Date, CustomerID, Product, Quantity, UnitPrice
- ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber
- ItemsInCart, CouponCode, ReferralSource, TotalPrice

---

## 🛠️ Tools Used

- Microsoft Excel
- Power Query (M Language)
- Power BI (Column Distribution & Profiling)

---

## 🔍 Data Quality Issues Found & Resolved

### 1. Missing Values — Coupon Column
- **Issue:** 309 missing values found in the CouponCode column (~30% of dataset)
- **Investigation:** Missing values were not errors — they indicated no coupon was used
- **Resolution:** Filled with "No Coupon"
- **Impact:** 309 records preserved

### 2. Date Column Format
- **Issue:** Date column came in as numbers instead of date format
- **Resolution:** Used Locale settings in Power Query to convert to proper date format
- **Impact:** All rows reformatted correctly

### 3. Duplicate Check — OrderID
- **Finding:** 1,000 distinct, 1,000 unique — no duplicates found
- **Action:** Verified and confirmed clean

### 4. CustomerID Duplicates
- **Finding:** Some CustomerIDs repeat
- **Conclusion:** Expected — one customer can place multiple orders. No action taken.

---

## 📋 Change Log (CR DOC)

| Change ID | Description | Impact | Status |
|-----------|-------------|--------|--------|
| CR001 | Replaced 309 null CouponCode values with "No Coupon" | Saved 309 records | Resolved |
| CR002 | Converted Date column from numeric to Date format using Locale | All rows reformatted | Resolved |

---

## 🔑 Key Takeaways

- Not all missing values are errors — context determines the fix
- Removing duplicates from non-ID columns deletes valid records
- Every change must be documented before touching any data
- **If it isn't documented, it didn't happen**

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `project_1_dataset.xlsx` | Original raw dataset |
| `project_1_cleaned.xlsx` | Cleaned dataset with all changes applied |
| `CR_DOC.xlsx` | Full change log with all 4 entries |
| `README.md` | This documentation file |

---

## 👤 Author
**Isaac Okolie**
DecodeLabs Data Analytics Intern
