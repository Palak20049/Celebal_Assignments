# Delta Lake Incremental Processing Assignment

## Overview

This project is based on incremental data processing using Delta Lake in Databricks.  
I used the Superstore dataset, cleaned it, saved it as a Delta table, created some new incremental records, and then applied a MERGE operation to update old records and insert new ones.

The main purpose of this assignment was to understand how Delta Lake handles updates, inserts, validation, and historical data changes in a practical data engineering workflow.

## Tools Used

- Databricks
- PySpark
- Delta Lake
- Superstore dataset
- GitHub for submission

## Work Completed

First, I loaded the Superstore data into a Databricks notebook and checked the rows and columns. After that, cleaned the dataset by fixing column names, handling null values, removing duplicates, and converting data types where needed.

After cleaning, I saved the data into a Delta table. Then created a small incremental dataset by taking a few existing records for update and adding some new records for insert.Also used the MERGE command to update matching records and insert non-matching records.

I also added SCD Type 2 logic for customer data so that old customer records can be expired and new versions can be stored separately. This helps in maintaining history when customer information changes.

## Main Steps

1. Loaded the dataset into Databricks.
2. Checked raw records and column structure.
3. Cleaned the data by removing duplicates and handling missing values.
4. Saved the cleaned data as a Delta table.
5. Created incremental data for update and insert.
6. Applied Delta Lake MERGE operation.
7. Validated the final data using row count and duplicate checks.
8. Implemented SCD Type 2 for customer history.
9. Captured screenshots of notebook outputs.

## Folder Structure

```text
delta-lake-assignment/
│
├── data/
│   └── Sample-Superstore.csv
│
├── notebook/
│   └── delta_lake_assignment.ipynb
│
├── screenshots/
│   └── delata_lake_assignment_screenshots.pdf
│
├── README.md
```

## How to Run

Open the notebook in Databricks and run the cells one by one.  
Make sure the dataset is already uploaded or available as a table in the Databricks workspace.

After running all cells, the final Delta tables will be created and the output can be checked using display commands.

## Output

The final output shows:

- Cleaned Superstore data
- Incremental records
- Updated Delta table after MERGE
- Duplicate validation result
- Final summary
- SCD Type 2 customer history records

## Conclusion

This assignment helped me understand how Delta Lake is useful for incremental processing. The MERGE operation made it easy to update existing records and insert new ones. SCD Type 2 also helped in understanding how historical changes can be maintained in real projects.
]()
