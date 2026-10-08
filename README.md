# Azure Data Pipeline Project

Learning project: cleaning data with pandas and storing it in Azure Data Lake Storage Gen2.

## What I've done so far
- Created Azure Data Lake (ADLS Gen2) with a raw-data container
- Practiced pandas: filtering, sorting, removing duplicates, handling missing values

## Tech
Python, pandas, SQL, Azure Storage

## Next steps
- Read data directly from Azure into pandas
- Save cleaned data to a clean folder
- Automate with Azure Data Factory

- ## Project 1: Retail Sales Data Pipeline

**Problem:** Raw sales data had duplicates and missing values.

**Steps:**
1. Stored raw CSV in Azure Data Lake (raw-data/sales)
2. Inspected data quality with pandas (info, isnull, duplicated)
3. Cleaned: removed duplicates, dropped rows with missing product/city, filled missing quantity with median
4. Added a total column (quantity x price)
5. Saved cleaned CSV to Azure (raw-data/clean)
6. Answered business questions with groupby

**Findings:** Tea generated the highest revenue; Lahore had the highest sales.

**Notebook:** [retail_project.ipynb](retail_project.ipynb)

**Tech:** Python, pandas, Azure Data Lake Storage Gen2
