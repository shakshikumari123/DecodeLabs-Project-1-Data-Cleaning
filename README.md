# DecodeLabs Internship — Project 1
## Data Cleaning and Preparation

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow)
![GitHub](https://img.shields.io/badge/GitHub-Project-black)

---

## 📌 Project Overview

This project was completed as part of my **Data Analyst Internship at DecodeLabs**.

The objective of the project was to clean and prepare an e-commerce order dataset for further analysis by identifying and handling missing values, duplicate records, formatting issues, and other data-quality problems.

The complete workflow was performed using **Python and Pandas in Google Colab**.

---

## 🎯 Objectives

The main objectives of this project were to:

- Identify and handle missing values
- Detect duplicate records
- Check for duplicate Order IDs
- Validate date formats
- Validate numerical data
- Check categorical and text consistency
- Validate identifier columns
- Perform final data-quality checks
- Export the cleaned dataset
- Document the changes made during the cleaning process

---

## 📊 Dataset Overview

The dataset contains e-commerce order information.

| Attribute | Details |
|---|---|
| Domain | E-commerce |
| Records | 1,200 |
| Columns | 14 |
| Original Format | Excel (.xlsx) |
| Final Format | Excel (.xlsx) |

### Dataset Columns

- `OrderID`
- `Date`
- `CustomerID`
- `Product`
- `Quantity`
- `UnitPrice`
- `ShippingAddress`
- `PaymentMethod`
- `OrderStatus`
- `TrackingNumber`
- `ItemsInCart`
- `CouponCode`
- `ReferralSource`
- `TotalPrice`

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **Google Colab**
- **Microsoft Excel**
- **GitHub**

---

# 🧹 Data Cleaning Process

## 1. Missing Value Analysis

The dataset was initially checked for missing values using Pandas.

A total of **309 missing values** were identified in the `CouponCode` column. All other columns contained no missing values.

The missing `CouponCode` values were replaced with `Unknown` to explicitly represent unavailable coupon information.

After the replacement, the dataset contained **zero missing values**.

---

## 2. Duplicate Analysis

The dataset was checked for both completely duplicated rows and duplicate `OrderID` values.

Results:

- Duplicate rows: **0**
- Duplicate OrderIDs: **0**

Therefore, no records were removed due to duplication.

---

## 3. Date Validation

The `Date` column was examined for consistency and data type.

The column was found to have the:

```text
datetime64[ns]

data type.

The order dates ranged from:

2023-01-01

to:

2025-06-30

No missing dates were identified, and no date corrections were required.

4. Numerical Data Validation

The following numerical columns were analyzed:

Quantity
UnitPrice
ItemsInCart
TotalPrice

The numerical values were examined using descriptive statistics.

No invalid negative or zero values were identified.

TotalPrice Validation

The TotalPrice column was checked against the expected calculation:

Quantity × UnitPrice

An initial comparison produced 107 apparent mismatches.

After rounding both the calculated and recorded values to two decimal places, all records matched.

This confirmed that the apparent differences were caused by floating-point precision, rather than incorrect data.

No changes were made to the TotalPrice column.

5. Text and Categorical Data Validation

The following categorical columns were checked:

Product
PaymentMethod
OrderStatus
CouponCode
ReferralSource

The columns were examined for:

Unexpected categories
Spelling inconsistencies
Capitalization differences
Leading/trailing spaces

No categorical inconsistencies were identified.

No additional text transformations were required.

6. Identifier Validation

The identifier columns were checked for missing values and uniqueness.

OrderID
Total records: 1,200
Unique OrderIDs: 1,200
Missing OrderIDs: 0
Duplicate OrderIDs: 0
CustomerID
Total records: 1,200
Unique CustomerIDs: 1,189
Missing CustomerIDs: 0

Repeated CustomerIDs were retained because a customer can legitimately place multiple orders.

TrackingNumber
Total records: 1,200
Unique TrackingNumbers: 1,200
Missing TrackingNumbers: 0
Duplicate TrackingNumbers: 0
✅ Final Validation

After completing the cleaning process, the dataset was validated again.

Quality Check	Result
Records	1,200
Columns	14
Missing Values	0
Duplicate Rows	0
Duplicate OrderIDs	0
Duplicate TrackingNumbers	0
Unique OrderIDs	1,200
Unique TrackingNumbers	1,200
Date Data Type	datetime64[ns]

The final validation confirmed that the cleaned dataset was ready for further analysis.

📁 Project Structure
DecodeLabs-Project-1-Data-Cleaning/
│
├── README.md
│
├── Problem_Statement/
│   └── Project_1_Problem_Statement.pdf
│
├── Dataset/
│   └── Original_Dataset.xlsx
│
├── Output/
│   └── Cleaned_Dataset.xlsx
│
├── Notebook/
│   └── DecodeLabs_Project_1_Data_Cleaning.ipynb
│
└── Documentation/
    └── DecodeLabs_Project_1_Change_Log.pdf
📂 Project Files
📄 Problem Statement

Project_1_Problem_Statement.pdf

Contains the original problem statement and project requirements provided for the internship.

📊 Original Dataset

Original_Dataset.xlsx

Contains the original dataset provided for the project before cleaning.

💻 Jupyter Notebook

DecodeLabs_Project_1_Data_Cleaning.ipynb

Contains the complete Python-based data cleaning process, analysis, validation, and documentation.

📈 Cleaned Dataset

Cleaned_Dataset.xlsx

Contains the final cleaned dataset after completing the data-quality checks.

📝 Change Log

DecodeLabs_Project_1_Change_Log.pdf

Documents the changes made during the cleaning process, their purpose, impact, and validation status.

📚 Key Learning Outcomes

Through this project, I gained practical experience in:

Data cleaning using Pandas
Missing-value analysis and handling
Duplicate detection
Data-type validation
Date validation
Numerical data validation
Categorical data validation
Identifier validation
Data-quality assurance
Exporting cleaned datasets
Documenting a data-cleaning workflow
Organizing and presenting a data analytics project using GitHub



👩‍💻 Author
Shakshi Kumari
B.Tech — Computer Science with Specialization in Data Science
Data Analyst Intern — DecodeLabs
