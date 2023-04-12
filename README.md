# 1. Azure Data Factory

![AzureDataFactory.drawio.png](https://github.com/developer-onizuka/Diagrams/blob/main/AzureDataFactory/AzureDataFactory.drawio.png)

# 2. Azure Stream Analytics

![stream-analytics-e2e-pipeline.png](https://github.com/developer-onizuka/AzureDataFactory/blob/main/stream-analytics-e2e-pipeline.png)

# 3. Azure Data Factory vs Azure Stream Analytics

| Service | Query Mechanism | Input | Output | Description |
| :--- | :--- | :--- | :--- | :--- |
| Data Factory | Apache Spark | Some reference data <br> - SQL or No-SQL Database <br> - Some file format such as csv or parquet files in Data Lake Gen2 | - Data warehouse (Dedicated SQL pool) | **Batch Oriented Service** <br> - A data integration service that connects any data source and enables automated workflows.<br> - In situations where various data store products and services are used on-premises or on the Azure side, it is often used when interconnection and pipeline processing are required. |
| Stream Analytics | SQL | Streaming services <br> - Event Hubs <br> - IoT Hub <br> - Azure Blob storage | - Data warehouse (Dedicated SQL pool) <br> - Power BI | **Stream Oriented Service** <br> - Performs real-time streaming processing, and you can describe the necessary processing in a SQL-like query language.<br> - It supports Azure IoTHub, EventHubs and BLOB Storage as data input sources while supporting BLOB Storage, Data Lake Store, SQL Database EventHubs, PowerBI etc as output destinations.<br> - In particular, stream-processed data can be stored directly in the storage area of PowerBI, so you can easily create a monitoring dashboard in which values and graphs change in real time.|


# 4. Difference between Hive, Presto and Spark

| | Hive | Presto | Spark |
| :--- | :--- | :--- | :--- |
|Function| MPP SQL engine | MPP SQL engine | General purpose execution framework |
|Processing Type| Batch processing using Apache Tez or MapReduce compute frameworks | Executes queries in memory, pipelined across the network between stages, thus avoiding unnecessary I/O | Optimized directed acyclic graph (DAG) execution engine and actively caches data in-memory |
|SQL Support| HiveQL | ANSI SQL | Spark SQL |
|Usage| Optimized for query throughput | Optimized for latency | General purpose, often used for data transformation and Machine Learning workloads |
|Use cases| Large data aggregations | Interactive queries and quick data exploration. | General purpose, often used for data transformation and Machine Learning workloads. |
