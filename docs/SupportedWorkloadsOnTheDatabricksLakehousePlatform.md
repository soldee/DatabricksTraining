# Supported Workloads on the Databricks Lakehouse Platform

### Data Warehousing

We know that traditional data warehouses are no longer able to keep up with the needs of today's world. 

![Complex solution using Data warehouse and Data lake](img/complex_dataWarehoue_dataLake.PNG)

- With this approach (Data warehouse for BI and Data Lake for AI/ML) used by some organizations, lots of challenges come to light to provide value from the data in a timely or cost effective manner.

The databricks Lakehouse Platform provides several features to support the data warehousing workload
- Warehousing workload refers to:
    - SQL analytics
    - BI tasks
        - Ingest, transform and query data
        - Building dashboards

These tasks are supported by databricks SQL and serverless SQL

![Data warehousing on databricks](img/data_warehousing_on_databricks.PNG)


<br>


### Data Engineering

- Data engineering workload refers to:
    - Ingesting, transforming and orchestrating data out to different data teams
 

#### Challenges for the data engineering workload:
- Complex data ingestion methods
- Support for data engineering principles
    - Agile development methods
    - Isolated development and production environments
    - CI/CD
    - Version control transformations
- Third-party orchestration tools
    - Increases operational overhead
    - Decreases reliability
- Pipeline and architecture performance tuning
    - Requires ...
        - knowledge of the underlying architecture
        - constantly observing throughput parameters
- Inconsistencies between data warehouse and data lake providers

#### Key capabilities of data engineering on the lakehouse
- Easy data ingestion
- Automated ETL pipelines
    - help reduce development time and effort
    - data engineers can focus on implementing business logic and data quality checks
- Data quality checks
- Batch and streaming tuning
    - data latency can be tuned with cost controls
- Automatic recovery
    - recover from common errors during pipeline execution
- Data pipeline observability
    - monitor overall pipeline status
- Simplified operations
    - easily deploy data pipelines to production
    - roll back pipelines and minimize downtime
- Scheduling and orchestration


#### Data ingestion
- As data loads into the delta lake, databricks automatically infers the schema

##### AutoLoader
Optimized data ingestion tool that processes new data files as they arrive in the lake house cloud storage.

It auto detects the schema and enforces it on your data.
Data ingestion for data analysts is easy with the *COPY INTO* SQL command that loads data from a folder into de Delta lake table. When run, only new files from the source will be processed.


#### Data transformation
##### Delta live tables
- ETL framework that uses a simple declarative approach to building reliable data pipelines
- Automatically autoscales infrastructure
- Data Engineers treat their data as code and apply software engineering best practices to deploy reliable pipelines at scale.
- Supports Python and SQL 
- Supports streaming and batch workloads

![Delta live tables](img/dlt.PNG)


#### Databricks Workflows
Fully managed orchestration service that allows data teams to build reliable workflows on any cloud without needing to manage a complex infrastructure. 

- Eliminates operational overhead for data engineers.
- You can create workflows using ...
    - databricks workflows API
    - databricks UI
    - external orchestrators like Apache Airflow 


<br>


### Data Streaming


