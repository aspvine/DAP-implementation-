
# AWS Data Analytic Platform for The City of vancouver
## Project Overview
This project focuses on analyzing data related to street trees using AWS Glue, Amazon Athena, and AWS Data Catalog. The workflow includes data ingestion, schema creation, and querying the data to derive insights.

---

## Tools and Technologies
- **AWS Glue**: For ETL (Extract, Transform, Load) processes and data cataloging.
- **Amazon Athena**: For querying the data stored in AWS Data Catalog.
- **AWS Data Catalog**: For organizing and maintaining metadata of the datasets.
- **S3 Storage**: The primary data source for storing raw data.

---

## Project Workflow
1. **Data Ingestion**: Raw data is stored in Amazon S3 buckets.
   ![Data ingestion1](https://github.com/user-attachments/assets/1e2d8baf-2df3-49ff-a743-ce5849c81246)
as seen from the shot
2. 
3. **Crawler Setup**: AWS Glue crawlers are created to scan the data, infer schemas, and populate metadata in the AWS Data Catalog.
4. **Schema Creation**: The crawlers extract schemas and automatically create tables in the AWS Data Catalog.
5. **Querying Data**: Amazon Athena is used to run SQL queries on the structured data.

---

## data process
###![Extraction1](https://github.com/user-attachments/assets/1bb1f7cf-77b6-4e5e-bf20-a2f7c26ee965)
 1. AWS Glue Crawlers Setup

- **Description**: The screenshot shows the list of AWS Glue Crawlers used to scan the datasets.
- **Details**:
  - Three crawlers are displayed with their respective statuses as **Ready**.
  - Each crawler scans a specific dataset and updates the table schemas.
  - The results of the last run show tables created in the Data Catalog.
### Data transformation
![Data ingestion2](https://github.com/user-attachments/assets/95ee2cec-e540-42f8-8ffa-7d3d4375ef02)
The image is a screenshot of the AWS DataBrew interface, specifically showing the "Jobs" section. It displays a list of "Recipe jobs" with one job listed. The job name is "van-sttrs-sau," and its status is marked as "Succeeded" with a green checkmark. The job's input includes a project named "van-sttrs-dtp..." and a dataset named "Street-Trees." The job output indicates "1 output." The last run of this job was 7 minutes ago, on November 25, 2024, at 11:31 PM. The job was created 9 minutes ago, on the same date, at 11:28 PM, by a user named "voclabs."
This job is part of a data transformation step within AWS DataBrew. In this step, data from the "Street-Trees" dataset is processed and transformed according to the recipe defined in the project. The purpose of this step is to clean, enrich, or restructure the raw data to prepare it for further analysis, reporting, or machine learning tasks.

The interface includes options to view details, run the job, perform actions, 
### 2. Amazon Athena Query Results
![IMG-20241214-WA0024](https://github.com/user-attachments/assets/66c67a2d-7a29-40da-b088-4523bb5b6de5)

- **Description**: The screenshot shows a SQL query executed in Amazon Athena.
- **Details**:
  - The query retrieves all rows from a table named `tra-user` in the `street_trees-datacatalog-sau` database.
  - The results include columns like `tree_id`, `civic_number`, `std_street`, `genus_name`, `species_name`, `common_name`, and neighborhood details.
  - The output confirms successful querying and displays 536 records.

