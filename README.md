# SWYNEX – Data Cleaning & Preparation

## 📌 Project Overview

This project was completed as part of the SWYNEX Technologies Data Analyst Internship.

The objective of this project was to clean and prepare a public Zomato delivery dataset for further analysis by identifying missing values, duplicate records, invalid values, and inconsistent data formats.

---

## 🎯 Objectives

- Profile the raw dataset
- Identify missing values
- Check for duplicate records
- Detect invalid numerical values
- Standardize inconsistent time formats
- Handle missing categorical values
- Validate the cleaned dataset
- Prepare an analysis-ready dataset

---

## 🗂️ Dataset

*Dataset:* Zomato Delivery Dataset

The dataset contains information related to food delivery operations, including delivery personnel, ratings, weather conditions, traffic density, order timing, vehicle conditions, locations, and delivery time.

### Original Dataset

- Rows: *45,584*
- Columns: *20*

The dataset was obtained from a publicly available source and was independently profiled and cleaned for this project.

---

## 🔍 Data Quality Issues Identified

### 1. Missing Values

Missing values were identified in several columns, including:

- Delivery person age
- Delivery person ratings
- Order time
- Weather conditions
- Road traffic density
- Multiple deliveries
- Festival
- City

### 2. Duplicate Records

Exact duplicate-row checking was performed.

*Result: 0 duplicate rows found.*

### 3. Invalid Values

The following invalid values were identified:

- *38* delivery-person age values were outside the selected valid range.
- *53* delivery-person rating values were outside the selected valid range.

These values were corrected according to the defined cleaning rules.

### 4. Inconsistent Time Format

The Time_Orderd column contained different representations of time.

Some values were stored in standard HH:MM format, while *4,068 values* were stored as Excel-style fractional time values.

These valid time representations were converted into a consistent time format instead of being discarded.

---

## 🛠️ Cleaning Performed

### Numerical Data

- Missing delivery-person ages were handled using the median age.
- Missing delivery-person ratings were handled using the median rating.
- Invalid age values were identified and corrected.
- Invalid rating values were identified and corrected.

### Categorical Data

Missing values in selected categorical columns were represented as:

Unknown

This approach preserved the records without inventing a specific category.

### Time Data

The Time_Orderd column was standardized by handling:

- Standard HH:MM values
- Excel fractional time values

Genuinely missing order times were preserved as missing rather than assigning artificial values.

---

## ✅ Validation Results

| Validation | Result |
|---|---:|
| Original rows | 45,584 |
| Cleaned rows | 45,584 |
| Original columns | 20 |
| Cleaned columns | 20 |
| Duplicate rows before cleaning | 0 |
| Duplicate rows after cleaning | 0 |
| Invalid ages corrected | 38 |
| Invalid ratings corrected | 53 |
| Excel-style time values converted | 4,068 |
| Remaining missing order times | 1,731 |

No rows or columns were intentionally removed during the cleaning process.

---

## 💻 Tools & Technologies

- Python
- Pandas
- NumPy
- Google Colab
- GitHub

---

## 📁 Project Files

```text
SWYNEX-Data-Cleaning-Preparation/
│
├── data/
│   └── zomato_cleaned_by_manisha.csv
│
├── notebooks/
│   └── SWYNEX-DATA-CLEANING_PREPARATION.ipynb
│
└── README.md
