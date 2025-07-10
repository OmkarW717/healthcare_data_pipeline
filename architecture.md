# Architecture Overview

## Pipeline Flow
1. **Raw Data** is uploaded to **AWS S3**.
2. **AWS Glue Job** processes and transforms the data.
3. Transformed data is saved back to **S3 (Parquet format)**.
4. **Python script** loads the Parquet files into **Snowflake** using `snowflake-connector`.
5. Optional dashboards created using **Power BI/Tableau** on Snowflake tables.
