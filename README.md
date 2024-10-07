# Home Sales Analysis

This notebook primarily focuses on analyzing home sales data using PySpark, with the key objectives of performing various SQL-based operations on the dataset and optimizing performance.

#### Key Steps and Achievements:

1. **Initialization and Setup:**
   - `findspark` is used to initialize Spark within the notebook.
   - A Spark session is created using `SparkSession.builder()`.

2. **Data Loading:**
   - The dataset containing home sales information is loaded into a Spark DataFrame. The structure includes columns like `id`, `date`, `date_built`, `price`, `bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `waterfront`, and `view`.

3. **SQL Queries on the Dataset:**
   - Several SQL queries were performed on the data, using Spark's SQL functionality. Key queries include:
     - Retrieving records based on conditions (e.g., filtering homes based on price and `view` ratings).
     - Grouping the data by `view` ratings and calculating the average price for each rating.
     - Filtering homes with an average price of at least $350,000.

4. **Performance Measurement:**
   - The runtime for one of the main queries, which calculates the average home price by `view` rating, is recorded and compared before and after caching the table for performance optimization.

5. **Table Caching and Uncaching:**
   - The `home_sales` table was cached to improve query performance. Later, the table was uncached, and a check was performed to confirm that it was no longer cached.

6. **Optimization:**
   - The notebook emphasizes the importance of caching for repeated queries, showcasing the difference in runtime when querying large datasets in Spark.

#### Achievements:
- Efficient querying and aggregation on the home sales data.
- Exploration of performance improvements through table caching.
- Successfully demonstrated how Spark SQL can be used to handle large datasets and optimize query execution.