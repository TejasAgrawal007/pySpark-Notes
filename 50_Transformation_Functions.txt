**🔥 50 Essential PySpark Transformation Functions**

### **1️⃣ Basic Transformations**
1. `select(*cols)` – Selects specific columns.
2. `filter(condition)` – Filters rows based on condition (same as `where()`).
3. `where(condition)` – Alias for `filter()`.
4. `distinct()` – Removes duplicate rows.
5. `withColumn(colName, expression)` – Creates or modifies a column.
6. `drop(*cols)` – Drops specified columns.
7. `alias(newName)` – Renames a column.
8. `limit(n)` – Limits the number of rows.
9. `sample(fraction)` – Returns a random sample of rows.
10. `orderBy(*cols)` – Sorts rows based on specified columns.

### **2️⃣ Aggregation & Grouping**
11. `groupBy(*cols).agg(aggregations)` – Groups data and applies aggregate functions.
12. `count()` – Counts number of rows.
13. `sum(column)` – Calculates sum of a column.
14. `avg(column)` – Calculates average of a column.
15. `min(column)` – Finds minimum value in a column.
16. `max(column)` – Finds maximum value in a column.
17. `mean(column)` – Computes mean of a column.
18. `approxQuantile(column, probabilities, relativeError)` – Computes approximate quantiles.
19. `cube(*cols).agg(aggregations)` – Performs multi-dimensional grouping.
20. `rollup(*cols).agg(aggregations)` – Creates hierarchical aggregation.

### **3️⃣ Joins & Merging**
21. `join(df, on, how='inner')` – Joins two DataFrames (`inner`, `left`, `right`, `full`).
22. `union(df)` – Appends another DataFrame (same schema required).
23. `unionByName(df)` – Appends another DataFrame (matching column names, not order).
24. `intersect(df)` – Returns common rows between two DataFrames.
25. `subtract(df)` – Returns rows that exist in one DF but not the other.
26. `crossJoin(df)` – Returns cartesian product of two DataFrames.
27. `coalesce(numPartitions)` – Reduces number of partitions.
28. `repartition(numPartitions)` – Redistributes DataFrame into specified partitions.
29. `hint(name, *parameters)` – Provides optimization hints for joins.
30. `cache()` – Caches DataFrame in memory for faster access.

### **4️⃣ Window Functions (Advanced Aggregation)**
31. `row_number().over(windowSpec)` – Assigns a unique row number per partition.
32. `rank().over(windowSpec)` – Assigns rank, allowing ties.
33. `dense_rank().over(windowSpec)` – Assigns consecutive rank without skipping.
34. `ntile(n).over(windowSpec)` – Divides dataset into `n` groups.
35. `lag(column, offset)` – Retrieves previous row value.
36. `lead(column, offset)` – Retrieves next row value.
37. `first(column).over(windowSpec)` – Gets first value in a partition.
38. `last(column).over(windowSpec)` – Gets last value in a partition.
39. `cume_dist().over(windowSpec)` – Calculates cumulative distribution.
40. `percent_rank().over(windowSpec)` – Computes percentile rank.

### **5️⃣ String & Data Handling**
41. `cast(newType)` – Changes column data type.
42. `substr(column, start, length)` – Extracts a substring.
43. `split(column, delimiter)` – Splits a string into an array.
44. `concat_ws(delimiter, *cols)` – Concatenates multiple columns into one string.
45. `explode(column)` – Converts array-type column into multiple rows.
46. `fillna(value, subset)` – Fills null values with a specified value.
47. `replace(to_replace, value)` – Replaces values in a column.
48. `regexp_replace(column, pattern, replacement)` – Replaces substrings using regex.
49. `translate(column, matching, replace)` – Replaces characters in a string.
50. `date_format(column, format)` – Formats date columns into custom formats.

💡 **These are only transformations** – they don't modify the original DataFrame but return a **new** transformed DataFrame.

