# Azure Data Pipeline Project

Learning project: cleaning data with pandas and storing it in Azure Data Lake Storage Gen2.

## What I've done so far
- Created Azure Data Lake (ADLS Gen2) with a raw-data container
- Practiced pandas: filtering, sorting, removing duplicates, handling missing values

## Tech
Python, pandas, SQL, Azure Storage

## Project 1: Retail Sales Data Pipeline

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

## Project 2: SQL Analysis on Cleaned Sales Data

**Problem:** Cleaned sales data needed to be queried like a real database.

**Steps:**
1. Loaded the cleaned CSV (from Project 1) into a SQLite database
2. Wrote SQL queries to answer business questions:
   - Total sales
   - Revenue by product (GROUP BY, ORDER BY)
   - Revenue by city
   - Orders above 1000 (WHERE)
   - Average order value per product (AVG)
3. Verified SQL results match the pandas groupby results from Project 1

**Notebook:** [sql_project.ipynb](sql_project.ipynb)

**Tech:** Python, pandas, SQLite, SQL

## Project 3: Reading Data Directly from Azure Data Lake

**Problem:** Data was moved manually between laptop and cloud.

**Steps:**
1. Connected Python (pandas + adlfs) to Azure Data Lake Storage Gen2
2. Read the cleaned CSV directly from raw-data/clean using an abfs:// path
3. Kept credentials out of the code before publishing

**Notebook:** [azure_project.ipynb](azure_project.ipynb)

**Tech:** Python, pandas, adlfs, Azure Data Lake Storage Gen2

## Next steps
- Automate the pipeline with Azure Data Factory
- Learn secure credential handling (SAS tokens, Key Vault)
