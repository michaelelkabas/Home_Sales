# Home_Sales
In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached. This project involves analyzing home sales data using Apache Spark. The dataset contains various attributes of home sales, such as price, bedrooms, bathrooms, sqft living, sqft lot, floors, waterfront, view, and date built.

# Home Sales Analysis with Apache Spark

This project involves analyzing home sales data using Apache Spark. The dataset contains various attributes of home sales, such as price, bedrooms, bathrooms, sqft living, sqft lot, floors, waterfront, view, and date built. The primary goal is to demonstrate the capabilities of Apache Spark for big data processing, including reading and writing data, performing SQL queries, and optimizing performance through caching.

## Project Description

The Home Sales Analysis project showcases the use of Apache Spark for processing and analyzing large datasets. This project includes the following key tasks:

1. **Data Ingestion**: Read a large CSV file containing home sales data into a Spark DataFrame.
2. **Data Partitioning and Storage**: Partition the DataFrame by the `date_built` field and save it as Parquet files. Parquet is a columnar storage file format optimized for large-scale queries.
3. **SQL Queries**: Create a temporary table using the partitioned Parquet data and run SQL queries to analyze the data.
4. **Performance Optimization**: Cache the temporary table to improve the performance of repeated queries. Measure and compare the execution times of cached and uncached queries.
5. **Results Interpretation**: Analyze the results to gain insights into the home sales data, such as the average price of homes based on their view rating.

### Detailed Steps

1. **Data Ingestion**:
    - Read the CSV data into a Spark DataFrame using Spark's built-in capabilities to handle large datasets efficiently.
    - The dataset is hosted on an AWS S3 bucket and is accessed directly via its URL.

2. **Data Partitioning and Storage**:
    - Partition the data by the `date_built` field to optimize query performance.
    - Save the partitioned data in Parquet format, which provides efficient data compression and encoding schemes.

3. **SQL Queries**:
    - Create a temporary table from the partitioned Parquet data.
    - Perform SQL queries on the temporary table to calculate the average home prices grouped by the `view` rating.
    - Filter the results to include only those entries where the average home price is greater than or equal to $350,000.

4. **Performance Optimization**:
    - Cache the temporary table to store the data in memory, reducing the time required for repeated queries.
    - Measure and compare the execution times of cached and uncached queries to highlight the performance benefits of caching.

5. **Results Interpretation**:
    - Interpret the results of the SQL queries to understand trends and patterns in the home sales data.
    - The analysis includes identifying the average home prices based on different view ratings and understanding how caching can significantly improve query performance.

## Prerequisites

Ensure you have the following software installed on your machine:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Apache Spark](https://spark.apache.org/downloads.html)
- [Hadoop DLL files](https://github.com/steveloughran/winutils) (for Windows users)

### Environment Variables

Set the following environment variables:

- `JAVA_HOME`: Path to your JDK installation
- `SPARK_HOME`: Path to your Spark installation
- `HADOOP_HOME`: Path to the directory containing the Hadoop DLL files
- Add the `bin` directory of Spark and Hadoop to the system `PATH`

Example:
```shell
export JAVA_HOME=C:\Program Files\Zulu\zulu-22
export SPARK_HOME=C:\Users\spark-3.5.1-bin-hadoop3
export HADOOP_HOME=C:\Users\spark-3.5.1-bin-hadoop3
export PATH=$PATH:C:\Users\spark-3.5.1-bin-hadoop3\bin


