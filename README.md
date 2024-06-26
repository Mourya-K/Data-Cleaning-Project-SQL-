# Data-Cleaning-Project-SQL

## Overview
This repository contains a SQL script for cleaning and preparing the Nashville housing dataset. The script performs various data cleaning operations to standardize the data and make it suitable and ready for analysis.

This dataset was obtained from GitHub, initially posted on Kaggle.

### If you want to jump straight to running the SQL queries, read just this following point:
1. If you use DB Management tools like Azure Data Studio like I do, then the direct import of the csv file will not be allowed until you change the data types of the fields *__SalePrice__* and *__SoldAsVacant__* to NVARCHAR(255).
2. If you use DB Management tools like Microsoft Sql Server Studio, the direct import of the .xlsx files will be allowed and I have handled the altering of data types of the fields mentioned in the previous point through SQL in the [Script.sql](./Script.sql) file.

That's it, download the dataset files, import into your DB Management tool and run the [Script.sql](./script.sql) file, all the queries should run perfectly.

### For the people who want to know more about the project and how it was done
## Purpose
The purpose of this project is to demonstrate data cleaning techniques using SQL for the Nashville housing dataset. By executing the provided script, users can clean the dataset and prepare it for further analysis.

## Skills Used
- Substring
- CharIndex
- ParseName
- Ranking functions (ROW_NUMBER)
- Common Table Expressions (CTEs)
- Joins
- Window Functions
- Aggregate Functions
- Altering and updating columns
  
## Files
- `Script.sql`: SQL script for cleaning the Nashville housing dataset.
- `Nashville Housing Data for Data Cleaning.csv`: Dataset file in csv format
- `Nashville Housing Data for Data Cleaning.xlsx`: Dataset file in xlsx (excel workbook) format

## Script Breakdown
1. **Load Dataset**: Initial step to load the NashvilleHousing dataset.
2. **Standardize Date Format**: Changes the column name of SaleDate_datetime and standardizes the date format.
3. **Populate Property Address Data**: Handles NULL PropertyAddress values by updating them with corresponding values from other rows.
4. **Breaking out Address**: Splits PropertyAddress and OwnerAddress columns into individual components (Address, City, State).
5. **Change Y and N to Yes and No**: Updates values in the SoldAsVacant field from 'Y' and 'N' to 'Yes' and 'No', respectively.
6. **Remove Duplicates**: Deletes duplicate rows based on selected columns to ensure data integrity.
7. **Delete Unused Columns**: Removes columns (OwnerAddress, TaxDistrict, PropertyAddress) that are no longer needed.

## Dataset:   
Link: https://github.com/AlexTheAnalyst/PortfolioProjects/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning%20(reuploaded).xlsx

The Nashville Housing dataset used in this project is sourced from this GitHub repo, initially posted on Kaggle
