# AzureDataEngg_SmartVehicles_project
Project for processing IoT data files using Azure Data Engineering tools.


Problem Statement:
A third party device scans and generates real time data of vehicles and uploads the same in JSON format on AWS S3 bucket on daily basis. The task is to ingest the JSON file, validate data, report incorrect data and process and load correct data to database for storage and analysis.


Solution & Architecture Diagram:
In order to ingest JSON data, we need to connect to the public S3 bucket and ingest JSON file into a landing folder in Azure Data Lake Storage account. Further, this data needs to be validated and sorted into 'staging' and 'rejected' blob storage directories. Validation will be done using Azure Function that checks for incorrect schema, missing fields and uploads correct data files into a staging folder which are further loaded as table data in Azure SQL Database. The inconsistent data will be rejected and uploaded to a 'rejected' folder and same will be reported via mail to relevent stakeholders and attachment of incorrect data will also be shared.

  Architecture Diagram:


![image](https://github.com/Saurify27/AzureDataEngg_SmartVehicles_project/assets/70844496/3f8842a2-f76b-4a28-8704-575a2eb6f142)



























  
