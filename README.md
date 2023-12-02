

# noSQL_challenge

Assignments demonstrating my work.

## PyMongo Exercise

### Introduction

This README offers a comprehensive overview of an exercise conducted using PyMongo, a Python driver for MongoDB, a widely used NoSQL database. The exercise focused on interacting with MongoDB, retrieving data, and performing data analysis using the Pandas library.

### Prerequisites

Before starting the exercise, ensure the following prerequisites are installed on your system:

- Python (version 3.x recommended)
- PyMongo library
- Pandas library
- MongoDB instance (local or remote)

### Exercise Overview

This exercise aimed to impart the fundamentals of working with MongoDB data using PyMongo, followed by data analysis using Pandas. Here are the key steps covered in this exercise:

### Connecting to MongoDB

Initiate a connection to a MongoDB instance using the PyMongo library:

```python
from pymongo import MongoClient

# Connect to MongoDB
client = MongoClient('localhost', 27017)
```

### Querying MongoDB

Perform queries on MongoDB collections using the `find` method to retrieve documents that match specific criteria:

```python
# Define query conditions
query = {"score.Hygiene": 20}

# Retrieve matching documents
results = list(collection.find(query))
```

### Converting to a Pandas DataFrame

Convert query results into a Pandas DataFrame for easier data analysis:

```python
import pandas as pd

# Convert list of dictionaries to DataFrame
df = pd.DataFrame(results)
```

### Analyzing Data

Utilize Pandas DataFrame capabilities for basic data analysis:

```python
# Display number of rows in DataFrame
num_rows = len(df)
print("Number of rows in DataFrame:", num_rows)

# Display first 10 rows of DataFrame
print(df.head(10))
```

### Advanced Queries and Operations

The code snippets provided demonstrate more advanced queries and operations on the MongoDB data using PyMongo:

```python
# Advanced search with criteria and sorting
# Code snippet for searching within a specified range of latitude and longitude, filtering by rating value and sorting by hygiene score.

# Similarly, code for creating a pipeline to match establishments with a hygiene score of 0, grouping by Local Authority, and sorting results.

# Additional code for retrieving establishments with a hygiene score of 0, aggregating by Local Authority, and presenting the results in a Pandas DataFrame.
```

### Conclusion

This exercise provided a practical understanding of working with MongoDB data using PyMongo and performing data analysis using Pandas in Python. The skills gained here can be applied to real-world scenarios where MongoDB serves as a data source.

