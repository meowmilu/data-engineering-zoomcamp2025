
```sql
-- Creating external table referring to gcs path
CREATE OR REPLACE EXTERNAL TABLE `kestra-nancy.de_zoomcamp.external_yellow_tripdata`
OPTIONS (
  format = 'PARQUET',
  uris = ['gs://kestra-nancy-bucket/yellow_tripdata_2024-*.parquet']
);
```

```sql
-- Create a table for the external table
CREATE OR REPLACE TABLE kestra-nancy.de_zoomcamp.yellow_tripdata AS
SELECT * FROM kestra-nancy.de_zoomcamp.external_yellow_tripdata;
```

