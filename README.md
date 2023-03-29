# 1. Azure Data Factory

![AzureDataFactory.png](https://github.com/developer-onizuka/Diagrams/blob/main/AzureDataFactory/AzureDataFactory.png)

# 2. Azure Stream Analytics

![stream-analytics-e2e-pipeline.png](https://github.com/developer-onizuka/AzureDataFactory/blob/main/stream-analytics-e2e-pipeline.png)

# 3. Azure Data Factory vs Azure Stream Analytics

| Service | Query Mechanism | Input | Output | Description |
| :--- | :--- | :--- | :--- | :--- |
| Data Factory | Apache Spark | Some reference data <br> - SQL Database <br> - csv files in Data Lake Gen2 | - Data warehouse (Dedicated SQL pool) | - A data integration service that connects any data source and enables automated workflows.<br> - In situations where various data store products and services are used on-premises or on the Azure side, it is often used when interconnection and pipeline processing are required. |
| Stream Analytics | SQL | Streaming services <br> - Event Hubs <br> - IoT Hub <br> - Azure Blob storage | - Data warehouse (Dedicated SQL pool) <br> - Power BI | - Performs real-time streaming processing, and you can describe the necessary processing in a SQL-like query language.<br> - It supports Azure IoTHub, EventHubs and BLOB Storage as data input sources while supporting BLOB Storage, Data Lake Store, SQL Database EventHubs, PowerBI etc as output destinations.<br> - In particular, stream-processed data can be stored directly in the storage area of PowerBI, so you can easily create a monitoring dashboard in which values and graphs change in real time.|
