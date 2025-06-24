# ETL_Midterm_Chad_884
# DSA2040A ETL Midterm - Chad 884

## 1. Project Overview
ETL pipeline processing sales data with:
- Data extraction and profiling
- Cleaning and enrichment
- Loading to SQLite/Parquet

## 2. ETL Phases
- **Extract**: 1. etl_extract.ipynb

Tasks Performed:

Data Loading:
Imports raw_data.csv and incremental_data.csv 
Preserves original files in /data directory
Initial Analysis:
Displays .head() and .info() for both datasets
Identifies data quality issues (missing values, duplicates, outliers)
Output:
Saves raw copies to /data folder
Generates observation report in markdown cells

- **Transform**: 2. etl_transform.ipynb

Tasks Performed:

Data Cleaning:
Handles missing values (customer names, regions, prices)
Removes duplicate order IDs
Filters invalid records (negative prices)
Enrichment:
Calculates total_price (quantity × unit_price)
Adds order_month and is_weekend datetime features
Flags high-value orders (>$1000)
Output:
Saves cleaned data as:
transformed_full.csv
transformed_incremental.csv

- **Load**: Stored in SQLite DB

## 3. Tools Used
- Python 3.10
- Pandas 2.0
- SQLite3

## 4. How to Run
1. Install requirements: `pip install pandas sqlalchemy`
2. Run notebooks in order:
   - `etl_extract2.ipynb`
   - `etl_transform.ipynb` 
   - `etl_load.ipynb`

## 5. Screenshot
