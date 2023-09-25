# noSQL_challenge
Assignments demonstrating my work.


### PyMongo Exercise


---

## Introduction

This README provides a detailed overview of the exercise conducted with PyMongo, a Python driver for MongoDB, which is a widely used NoSQL database. In this exercise, we learned how to interact with MongoDB, perform data retrieval, and analyze data using the Pandas library.

---

## Prerequisites

Before diving into this exercise, ensure you have the following prerequisites installed on your system:

- Python (version 3.x recommended)
- PyMongo library
- Pandas library
- MongoDB instance (either running locally or accessible remotely)

---

## Exercise Overview

This exercise aimed to teach the fundamentals of working with MongoDB data using PyMongo, followed by data analysis using Pandas. Below are the key steps covered in this exercise:

---

## Connecting to MongoDB

We initiated our exercise by establishing a connection to a MongoDB instance. The following code demonstrates how to connect to MongoDB using the PyMongo library. Replace 'localhost' and '27017' with your MongoDB server details.

```python
from pymongo import MongoClient

# Connect to MongoDB
client = MongoClient('localhost', 27017)
```

---

## Querying MongoDB

Next, we delved into querying MongoDB collections. We used the `find` method to retrieve documents that match specific criteria. The query condition can be customized as needed to filter data from the collection.

```python
# Define the query condition
query = {"score.Hygiene": 20}

# Use find to retrieve matching documents
results = list(collection.find(query))
```

---

## Converting to a Pandas DataFrame

To facilitate data analysis, we converted the query results into a Pandas DataFrame. The Pandas library is a powerful tool for data manipulation and analysis in Python.

```python
import pandas as pd

# Convert the list of dictionaries to a DataFrame
df = pd.DataFrame(results)
```

---

## Analyzing Data

If the data successfully loads into a Pandas DataFrame, it should demonstrate some basic data analysis operations. This includes displaying the number of rows in the DataFrame and showing the first few rows of data.

```python
# Display the number of rows in the DataFrame
num_rows = len(df)
print("Number of rows in the DataFrame:", num_rows)

# Display the first 10 rows of the DataFrame
print(df.head(10))
```

---

## Conclusion

This exercise introduced the essential concepts of working with MongoDB data using PyMongo and conducting data analysis using Pandas in Python. The skills acquired here can be extended to real-world scenarios where MongoDB is used as a data source.

Feel free to customize and expand upon these concepts to address specific data analysis tasks in your projects.



