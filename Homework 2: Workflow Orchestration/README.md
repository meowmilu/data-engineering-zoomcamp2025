
## Module 2 Homework

### Quiz Questions

Complete the Quiz shown below. It’s a set of 6 multiple-choice questions to test your understanding of workflow orchestration, Kestra and ETL pipelines for data lakes and warehouses.

## Question 1: Within the execution for `Yellow` Taxi data for the year `2020` and month `12`: what is the uncompressed file size (i.e. the output file `yellow_tripdata_2020-12.csv` of the `extract` task)?
- 128.3 MB
- 134.5 MB
- 364.7 MB
- 692.6 MB

### Answer: 128.3 MB

Execute the flow `06_gcp_taxi`

![HW2_Q1](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q1.png)

Check the file size in GCP Bucket

![HW2_Q1_2](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q1_02.png)

## Question 2. What is the rendered value of the variable `file` when the inputs `taxi` is set to `green`, `year` is set to `2020`, and `month` is set to `04` during execution?
- `{{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv` 
- `green_tripdata_2020-04.csv`
- `green_tripdata_04_2020.csv`
- `green_tripdata_2020.csv`

### Answer: green_tripdata_2020-04.csv

## Question 3. How many rows are there for the `Yellow` Taxi data for all CSV files in the year 2020?
- 13,537.299
- 24,648,499
- 18,324,219
- 29,430,127

### Answer: 24,648,499

In the flow `06_gcp_taxi_scheduled`, click `Backfill executions` under `Triggers` tab, set up duration from `2020-01-01 00:00:00` to `2020-12-31 23:59:59`and select `yellow` as taxi type

![HW3_Q3](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q3.png)

Check `Number of rows` in the `details` of table `yellow_tripdata` in GCP

![HW3_Q3_2](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q3_02.png)

## Question 4. How many rows are there for the `Green` Taxi data for all CSV files in the year 2020?
- 5,327,301
- 936,199
- 1,734,051
- 1,342,034

### Answer: 1,734,051

In the flow `06_gcp_taxi_scheduled`, click `Backfill executions` under `Triggers` tab, set up duration from `2020-01-01 00:00:00` to `2020-12-31 23:59:59`and select `green` as taxi type

![HW4_Q4](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q4.png)

Check `Number of rows` in the `details` of table `green_tripdata` in GCP

![HW4_Q4_2](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q4_02.png)


## Question 5. How many rows are there for the `Yellow` Taxi data for the March 2021 CSV file?
- 1,428,092
- 706,911
- 1,925,152
- 2,561,031

### Answer: 1,925,152

Execute the flow `06_gcp_taxi` 

![HW4_Q5](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q5.png)

Check `Number of rows` in the `details` of table `yellow_tripdata_2021_03` in GCP

![HW4_Q5_2](https://github.com/meowmilu/data-engineering-zoomcamp2025/blob/main/Homework%202%3A%20Workflow%20Orchestration/images/HW2_Q5_02.png)

## Question 6. How would you configure the timezone to New York in a Schedule trigger?
- Add a `timezone` property set to `EST` in the `Schedule` trigger configuration  
- Add a `timezone` property set to `America/New_York` in the `Schedule` trigger configuration
- Add a `timezone` property set to `UTC-5` in the `Schedule` trigger configuration
- Add a `location` property set to `New_York` in the `Schedule` trigger configuration  

### Answer: Add a `timezone` property set to `America/New_York` in the `Schedule` trigger configuration

## !!IMPORTANT!! Don't include any credentials information in your GitHub!!
