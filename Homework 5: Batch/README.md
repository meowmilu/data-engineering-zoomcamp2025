
# Module 5 Homework

In this homework we'll put what we learned about Spark in practice.

For this homework we will be using the Yellow 2024-10 data from the official website: 

```bash
wget https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2024-10.parquet
```


## Question 1: Install Spark and PySpark

- Install Spark
- Run PySpark
- Create a local spark session
- Execute spark.version.

What's the output?

> [!NOTE]
> To install PySpark follow this [guide](https://github.com/DataTalksClub/data-engineering-zoomcamp/blob/main/05-batch/setup/pyspark.md)

## Answer: 3.5.5

```python
import pyspark
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .master("local[*]") \
    .appName('test') \
    .getOrCreate()
spark.version
```
![HW5_Q1](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q1.png)


## Question 2: Yellow October 2024

Read the October 2024 Yellow into a Spark Dataframe.

Repartition the Dataframe to 4 partitions and save it to parquet.

What is the average size of the Parquet (ending with .parquet extension) Files that were created (in MB)? Select the answer which most closely matches.

- 6MB
- 25MB
- 75MB
- 100MB

## Answer: 25MB
![HW5_Q2_1](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q2_1.png)
![HW5_Q2_2](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q2_2.png)

## Question 3: Count records 

How many taxi trips were there on the 15th of October?

Consider only trips that started on the 15th of October.

- 85,567
- 105,567
- 125,567
- 145,567

## Answer: 128893

![HW5_Q3](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q3.png)

## Question 4: Longest trip

What is the length of the longest trip in the dataset in hours?

- 122
- 142
- 162
- 182

## Answer:162

![HW5_Q4](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q4.png)

## Question 5: User Interface

Spark’s User Interface which shows the application's dashboard runs on which local port?

- 80
- 443
- 4040
- 8080

## Answer: 4040

## Question 6: Least frequent pickup location zone

Load the zone lookup data into a temp view in Spark:

```bash
wget https://d37ci6vzurychx.cloudfront.net/misc/taxi_zone_lookup.csv
```

Using the zone lookup data and the Yellow October 2024 data, what is the name of the LEAST frequent pickup location Zone?

- Governor's Island/Ellis Island/Liberty Island
- Arden Heights
- Rikers Island
- Jamaica Bay

## Answer: Governor's Island/Ellis Island/Liberty Island

![HW5_Q6](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%205%3A%20Batch/images/HW5_Q6.png)

## Submitting the solutions

- Form for submitting: https://courses.datatalks.club/de-zoomcamp-2025/homework/hw5
- Deadline: See the website

