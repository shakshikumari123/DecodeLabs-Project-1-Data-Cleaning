# DecodeLabs Internship — Project 1
## Data Cleaning and Preparation

### 📌 Project Overview

This project was completed as part of my Data Analyst internship at DecodeLabs.

The objective of the project was to clean and prepare an e-commerce order dataset for further analysis by identifying and handling missing values, duplicate records, data-format issues, and other data-quality problems.

---

## 🎯 Objectives

The main objectives of this project were to:

- Identify missing values
- Detect duplicate records
- Check for duplicate Order IDs
- Validate date formats
- Validate numerical data
- Check text and categorical consistency
- Validate identifier columns
- Perform final data-quality checks
- Export the cleaned dataset

---

## 📊 Dataset Overview

| Attribute | Details |
|---|---|
| Dataset Type | E-commerce Order Data |
| Records | 1,200 |
| Columns | 14 |
| Original Format | Excel (.xlsx) |
| Final Format | Excel (.xlsx) |

### Columns

- OrderID
- Date
- CustomerID
- Product
- Quantity
- UnitPrice
- ShippingAddress
- PaymentMethod
- OrderStatus
- TrackingNumber
- ItemsInCart
- CouponCode
- ReferralSource
- TotalPrice

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- Google Colab
- Microsoft Excel
- GitHub

---

## 🧹 Data Cleaning Process

### 1. Missing Value Analysis

The dataset was checked for missing values.

Initially, 309 missing values were identified in the `CouponCode` column. After examining the affected records, the missing values were replaced with `Unknown` because the dataset did not provide enough information to determine whether a missing value represented no coupon or unavailable coupon information.

After cleaning, the dataset contained zero missing values.

### 2. Duplicate Analysis

The dataset was checked for completely duplicated rows and duplicate `OrderID` values.

Results:

- Duplicate rows: 0
- Duplicate OrderIDs: 0

No records were removed due to duplication.

### 3. Date Validation

The `Date` column was verified to have the `datetime64[ns]` data type.

The dates followed the `YYYY-MM-DD` format and ranged from `2023-01-01` to `2025-06-30`.

No missing dates were found, so no date corrections were required.

### 4. Numerical Data Validation

The following numerical columns were examined:

- `Quantity`
- `UnitPrice`
- `ItemsInCart`
- `TotalPrice`

No invalid negative or zero values were identified.

The `TotalPrice` column was also validated against:

```text
Quantity × UnitPrice
