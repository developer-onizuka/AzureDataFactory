# 1. Azure Data Factory

![AzureDataFactory.png](https://github.com/developer-onizuka/Diagrams/blob/main/AzureDataFactory/AzureDataFactory.png)

# 2. Azure Stream Analytics

![stream-analytics-e2e-pipeline.png](https://github.com/developer-onizuka/AzureDataFactory/blob/main/stream-analytics-e2e-pipeline.png)

# 3. Azure Data Factory vs Azure Stream Analytics

| Service | Query Mechanism | Input | Output |
| :--- | :--- | :--- |
| Data Factory | Apache Spark | Some reference data <br> - SQL Database <br> - csv files in Data Lake Gen2 | - Data warehouse |
| Stream Analytics Jobs | SQL | Streaming services <br> - Event Hubs <br> - IoT Hub <br> - Azure Blob storage | - Data warehouse <br> - Power BI |
