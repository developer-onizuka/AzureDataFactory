# 1. Azure Data Factory

![AzureDataFactory.drawio.png](https://github.com/developer-onizuka/Diagrams/blob/main/AzureDataFactory/AzureDataFactory.drawio.png)

# 2. Azure Stream Analytics

![stream-analytics-e2e-pipeline.png](https://github.com/developer-onizuka/AzureDataFactory/blob/main/stream-analytics-e2e-pipeline.png)

# 3. Azure Data Factory vs Azure Stream Analytics

| Service | Query Mechanism | Input | Output | Description |
| :--- | :--- | :--- | :--- | :--- |
| Data Factory | Apache Spark | Some reference data <br> - SQL or No-SQL Database <br> - Some file format such as csv or parquet files in Data Lake Gen2 | - Data warehouse (Dedicated SQL pool) | **Batch Oriented Service** <br> - A data integration service that connects any data source and enables automated workflows.<br> - In situations where various data store products and services are used on-premises or on the Azure side, it is often used when interconnection and pipeline processing are required. |
| Stream Analytics | SQL | Streaming services <br> - Event Hubs <br> - IoT Hub <br> - Azure Blob storage | - Data warehouse (Dedicated SQL pool) <br> - Power BI | **Stream Oriented Service** <br> - Performs real-time streaming processing, and you can describe the necessary processing in a SQL-like query language.<br> - [Native support for windowing functions, enabling developers to author complex stream processing jobs with minimal effort](https://learn.microsoft.com/en-us/azure/stream-analytics/stream-analytics-window-functions) <br> - It supports Azure IoTHub, EventHubs and BLOB Storage as data input sources while supporting BLOB Storage, Data Lake Store, SQL Database EventHubs, PowerBI etc as output destinations.<br> - In particular, stream-processed data can be stored directly in the storage area of PowerBI, so you can easily create a monitoring dashboard in which values and graphs change in real time.|


# 4. Difference between Hive, Presto and Spark

| | Hive | Presto | Spark |
| :--- | :--- | :--- | :--- |
|Function| MPP SQL engine | MPP SQL engine | General purpose execution framework |
|Processing Type| Batch processing using **Apache Tez** or MapReduce compute frameworks | Executes **queries in memory**, pipelined across the network between stages, thus avoiding unnecessary I/O | Optimized directed acyclic graph (DAG) execution engine and actively **caches data in-memory** |
|SQL Support| HiveQL | ANSI SQL | Spark SQL |
|Usage| **Optimized for query throughput** | **Optimized for latency** | General purpose, often used for **data transformation and Machine Learning workloads** |
|Use cases| - **Large data aggregations** <br> - Data warehouse | - **Interactive queries** and quick data exploration <br> - Amazon Athena <br> - a fast SQL query engine designed for interactive analytic queries over large datasets from multiple sources | General purpose, often used for **data transformation and Machine Learning workloads** |


# 5. Power BI vs Azure Synapse: What are the differences?

Developers describe Power BI as "A business analytics service". It aims to provide interactive visualizations and business intelligence capabilities with an interface simple enough for end users to create their own reports and dashboards. On the other hand, Azure Synapse is detailed as "Analytics service that brings together enterprise data warehousing and Big Data analytics". It is an analytics service that brings together enterprise data warehousing and Big Data analytics. It gives you the freedom to query data on your terms, using either serverless on-demand or provisioned resources—at scale. It brings these two worlds together with a unified experience to ingest, prepare, manage, and serve data for immediate BI and machine learning needs.

Power BI can be classified as a tool in the **"Business Intelligence"** category, while Azure Synapse is grouped under **"Big Data Tools"**.
