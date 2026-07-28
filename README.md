## Azure Real-Time Incremental Data Pipeline Using Azure Data Factory

- Project Overview

This project demonstrates an end-to-end Azure real-time data pipeline that ingests data from an external REST API (JSON format),
processes only new or updated records using an incremental loading strategy, and stores the data in SQL Server/Azure SQL Database for 
reporting and analytics.
The pipeline is built using Azure Data Factory (ADF) to automate data ingestion, transformation, and orchestration. Incoming data 
is first loaded into a staging table, which is truncated before each pipeline run, and then synchronized with the target Order table 
using an upsert (Insert & Update) approach.

### Architecture

![image alt](https://github.com/oladebo/Azure-Adf-Incremental-loading-project-/blob/827f402672e902dabbb5df5ace64697715f41c5c/Screen%20Shot%202026-07-28%20at%2008.36.04.png)

![image alt](https://github.com/oladebo/Azure-Adf-Incremental-loading-project-/blob/827f402672e902dabbb5df5ace64697715f41c5c/Screen%20Shot%202026-07-28%20at%2008.37.11.png)


### Features
Real-time API data ingestion
JSON data processing
Azure Data Factory orchestration
Incremental data loading
Staging table refresh
Insert new records
Update existing records
SQL-based reporting

### Business Problem

Organizations receive continuous data from external APIs, but manually downloading, cleaning, and loading 
this data into databases is time-consuming and prone to errors.

- The business requires an automated solution to:

Retrieve the latest API data.
Process only new or modified records.
Keep the Order table up to date.
Reduce manual intervention.
Support real-time reporting and analytics.

### Solution

- The solution uses Azure Data Factory to automate the complete process.

During each pipeline execution:

Retrieve JSON data from the REST API.
Load the data into a staging table.
Truncate the staging table before loading new data.
Compare staging data with the target Order table.
Insert new records.
Update existing records.
Make the latest data available for reporting and analysis.


### Summary

This project demonstrates a modern Azure real-time data integration solution using Azure Data Factory. By ingesting JSON data
from a REST API, applying incremental loading, and performing upsert operations on the Order table, the pipeline 
ensures accurate, efficient, and scalable data processing. The solution minimizes manual effort, improves data quality, and
enables organizations to make faster, data-driven decisions through reliable and up-to-date data.

By Oladebo Ayanniyi
(Cloud Data Engineer)
