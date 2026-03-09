# Nashville Housing Data Cleaning (SQL)

## Overview
This project focuses on cleaning a real-world housing dataset using SQL.  
The goal was to transform raw housing data into a cleaner and more structured format by fixing inconsistent values, handling missing data, and preparing fields for analysis.

The dataset contains housing sales information from Nashville, Tennessee.

Dataset source:  
https://www.kaggle.com/datasets/tmthyjames/nashville-housing-data

---

## Objectives
- Standardise inconsistent data formats
- Populate missing values
- Split combined fields into structured columns
- Clean categorical values
- Identify duplicate records
- Prepare the dataset for further analysis

---

## Techniques Used

### Date Standardisation
Converted datetime values into a consistent date format.

Functions used:
- `CONVERT()`

---

### Handling Missing Data
Missing property addresses were filled using matching Parcel IDs.

Functions used:
- `ISNULL()`

---

### Splitting Address Fields
Combined address fields were separated into individual components.

Functions used:
- `SUBSTRING()`
- `CHARINDEX()`
- `PARSENAME()`
- `REPLACE()`

New columns created:
- `PropertySplitAddress`
- `PropertySplitCity`
- `OwnerSplitAddress`
- `OwnerSplitCity`
- `OwnerSplitState`

---

### Standardising Categorical Values
Converted abbreviated values to consistent labels.

Example:

Y -> Yes
N -> No

Function Used:
- 'CASE'

---

### Duplicate Detection
Duplicate rows were identified using window funcitons.

Technique used:
- 'ROW_NUMBER()' with Common Table Expressions (CTEs)

---

## Technologies Used
- SQL Server
- SQL

## File
'nashville-housing-data-cleaning-cleaning.sql'
Contains the full SQL workflow used to clean the dataset. 

