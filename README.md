# DecodeLabs Internship — Project 1
## Data Cleaning and Preparation

### 📌 Project Overview

This project was completed as part of my Data Analyst internship at DecodeLabs.

The objective of this project was to clean and prepare an e-commerce order dataset for further analysis by identifying missing values, duplicate records, formatting issues, and other data-quality problems.

---

## 🎯 Objectives

- Identify and handle missing values
- Detect duplicate records
- Check for duplicate Order IDs
- Validate date formats
- Validate numerical data
- Check text and categorical data consistency
- Validate identifier columns
- Perform final data-quality checks
- Export the cleaned dataset

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- Google Colab
- Microsoft Excel
- GitHub

---

## 📊 Dataset Overview

The dataset contains e-commerce order information.

| Attribute | Details |
|---|---|
| Records | 1,200 |
| Columns | 14 |
| File Format | Excel (.xlsx) |
| Domain | E-commerce Orders |

### Main Features

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

## 🧹 Data Cleaning Process

### 1. Missing Value Analysis

The dataset was checked for missing values using Pandas.

Initially, **309 missing values** were found in the `CouponCode` column.

Since the dataset did not provide enough information to determine whether a missing value represented "no coupon" or unavailable coupon information, the missing values were replaced with `Unknown`.

After cleaning, the dataset contained **zero missing values**.

### 2. Duplicate Analysis

The dataset was checked for completely duplicated rows and duplicate `OrderID` values.

- Duplicate rows: **0**
- Duplicate OrderIDs: **0**

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

The `TotalPrice` column was also validated using:

`Quantity × UnitPrice`

After rounding the calculated and recorded values to two decimal places, all records matched.

Therefore, no changes were made to the `TotalPrice` column.

### 5. Text and Categorical Validation

The following categorical columns were checked:

- `Product`
- `PaymentMethod`
- `OrderStatus`
- `CouponCode`
- `ReferralSource`

No unexpected categories, spelling inconsistencies, capitalization issues, or leading/trailing spaces were identified.

### 6. Identifier Validation

The identifier columns were checked for missing and duplicate values.

- `OrderID`: 1,200 unique values, no missing values
- `CustomerID`: 1,189 unique values, no missing values
- `TrackingNumber`: 1,200 unique values, no missing or duplicate values

Repeated `CustomerID` values were retained because a customer can place multiple orders.

---

## ✅ Final Validation

| Quality Check | Result |
|---|---:|
| Records | 1,200 |
| Columns | 14 |
| Missing values | 0 |
| Duplicate rows | 0 |
| Duplicate OrderIDs | 0 |
| Duplicate TrackingNumbers | 0 |
| Unique OrderIDs | 1,200 |
| Unique TrackingNumbers | 1,200 |
| Date data type | `datetime64[ns]` |

The cleaned dataset successfully passed the final data-quality checks.

---

## 📁 Project Files

### `DecodeLabs_Project_1_Data_Cleaning.ipynb`
Contains the complete Python-based data cleaning process, analysis, validation, and documentation.

### `Cleaned_Dataset.xlsx`
Contains the final cleaned dataset after completing the data-quality checks.

---

## 📚 Key Learning Outcomes

Through this project, I practiced:

- Data cleaning using Pandas
- Missing-value handling
- Duplicate detection
- Data-type validation
- Date validation
- Numerical data validation
- Categorical data validation
- Data-quality checks
- Exporting cleaned datasets
- Documenting a data-cleaning workflow

---

## 👩‍💻 Author

**Shakshi Kumari**

B.Tech — Computer Science with Specialization in Data Science

Data Analyst Intern — DecodeLabs
