# MSFabric_covid_test
A full automatic pipeline pulling data from a public API and building a Power BI report using MS Fabric

# Project Overview
The project is aimed to learn MS Fabric mainly emphasizing on how to connect to an API to pull data, cleanse data, load in to a Data Lakehouse, create a pipeline using Azure Data Factory and then scheduling the pipeline to run automatically on a daily basis to provide fresh data. The data relates to world wide covid cases which is pulled using an API which is publically available at Rapid API. You can access the API [here](https://rapidapi.com/api-sports/api/covid-193).

Technologies used: Python, PySPark, MS Fabric (Data Engineering, Data Factory, Power BI).

# Getting Started
1. Create a Project in MS Fabric.
2. Stay in (Synapse) Data Engineering mode (Bottom left).
3. Add notebooks to the project.
4. Run the Covid_Bronze notebook first and then run covid_silver notebook. This will create json file as well as the data table which can be queried in SQL layer (SQL Analytic Endpoint).
5. Add model to Semantic Layer.
6. Select Power BI mode from bottom left.
7. Create new report.
8. Add an existing semantic model and select the model you created.
9. Create Power BI report and save.
10. Select Data Factory mode from Bottom Left.
11. Create new pipeline.
12. Add notebooks to pipeline (Covid_Bronze and covid_silver) and create a flow from Bronze to Silver notebook.
13. Validate pipeline.
14. Run Pipeline and resolve if any issues.
15. There is a Schedule button on top in pipeline menu, click on it and schedule the pipeline as per your requirement.
16. It will now run automatically and Power BI report will get refreshed automatically.

# Repository Contents
The repository mainly includes python code to execute the project. The python code first imports the raw data and then cleanse it for analysis and reporting.
1. Covid_Bronze: This code connects to API and pulls the data in raw form and saves it in a json file.
2. covid_silver: This code cleanse the data, converts into columns and fields, removes unnecessary columns and ultimately loads the data into a table in lakehouse.

# Pre-requisites
- Microsoft Fabric Account.
- Fabric Administrator (or access to individual with Admin account).
- Familiarity with Python, Spark, and basic data engineering concepts.
- Basic Power BI skills.
