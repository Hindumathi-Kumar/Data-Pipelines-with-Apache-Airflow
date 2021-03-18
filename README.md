# Data-Pipelines-with-Apache-Airflow
Developed a data pipeline to automate data warehouse ETL by building custom airflow operators that handle the extraction, transformation, validation and loading of data from S3 -> Redshift -> S3


## Project: Data Pipelines with Airflow
**Project Description**: 
A music streaming company wants to introduce more automation and monitoring to their data warehouse ETL pipelines and they have come to the conclusion that the best tool to achieve this is **Apache Airflow**. 
As their **Data Engineer**, I was tasked to create a reusable production-grade data pipeline that incorporates data quality checks and allows for easy backfills. 
Several analysts and Data Scientists rely on the output generated by this pipeline and it is expected that the pipeline runs daily on a schedule by pulling new data from the source and store the results to the destination.

**Data Description**: 
The source data resides in S3 and needs to be processed in a data warehouse in Amazon Redshift. The source datasets consist of JSON logs that tell about user activity in the application and JSON metadata about the songs the users listen to.

**Data Pipeline design**:
At a high-level the pipeline does the following tasks.
1. Extract data from multiple S3 locations.
2. Load the data into Redshift cluster.
3. Transform the data into a star schema.
4. Perform data validation and data quality checks.
5. Calculate the most played songs for the specified time interval.


![dag](images/dag.png)
> Structure of the Airflow DAG
