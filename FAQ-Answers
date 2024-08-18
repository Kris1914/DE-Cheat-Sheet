# Data Engineering Cheat Sheets

## 1. Data Lake
A Data Lake is a large storage repository that holds vast amounts of raw data in its native format until it is needed. The data can come from various sources like logs, social media, IoT devices, or traditional databases. Unlike a data warehouse, which requires data to be processed before storage, a data lake stores data as-is and processes it only when it’s time to use it. This makes data lakes very flexible and scalable, but they require good governance to avoid turning into a disorganized "data swamp."

**Key Points:**
- Stores raw data in any format (structured, semi-structured, unstructured).
- Used for big data and analytics.
- Highly scalable and cost-effective.
- Needs proper management to maintain data quality and accessibility.

## 2. Data Warehouse
A Data Warehouse is a centralized repository that stores processed and structured data, often organized into tables and schemas, optimized for querying and reporting. Data in a warehouse is typically cleaned, transformed, and integrated from various sources before storage, making it ideal for business intelligence and analysis.

**Key Points:**
- Stores processed, structured data.
- Optimized for complex queries and reporting.
- Supports decision-making processes.
- Typically more expensive due to storage and processing costs.

## 3. PySpark vs Pandas
PySpark and Pandas are both data processing tools, but they serve different purposes:

- **Pandas**: A Python library used for data manipulation and analysis. It’s great for small to medium-sized datasets that can fit into memory. Pandas is user-friendly, with a rich set of functionalities for cleaning, transforming, and analyzing data.
- **PySpark**: The Python API for Apache Spark, a distributed computing framework. PySpark is designed for processing large-scale datasets that are too big to fit into memory on a single machine. It can handle massive data across a cluster of computers, making it ideal for big data applications.

**Key Differences:**
- **Scale**: Pandas for smaller datasets; PySpark for big data.
- **Speed**: PySpark can be faster for large-scale data due to distributed processing.
- **Complexity**: Pandas is simpler to use for beginners; PySpark requires understanding of distributed computing.

## 4. Python OOP (Object-Oriented Programming)
Object-Oriented Programming (OOP) in Python is a programming paradigm that uses "objects" to model real-world entities. These objects are instances of "classes," which define the properties (attributes) and behaviors (methods) of the object.

**Key Concepts:**
- **Class**: A blueprint for creating objects (e.g., a class `Car` that defines attributes like color and model, and methods like `drive`).
- **Object**: An instance of a class (e.g., `my_car` is an object of the class `Car`).
- **Inheritance**: Allows a class to inherit properties and methods from another class (e.g., `ElectricCar` inherits from `Car`).
- **Encapsulation**: Restricts access to certain components, protecting the internal state of the object.
- **Polymorphism**: Allows different classes to be treated as instances of the same class through a common interface.

## 5. CI/CD Pipelines
Continuous Integration (CI) and Continuous Deployment/Delivery (CD) pipelines are automated workflows that help in the development and deployment of software.

- **CI (Continuous Integration)**: Developers frequently integrate code into a shared repository, triggering automated builds and tests to detect issues early.
- **CD (Continuous Deployment/Delivery)**: After CI, the pipeline continues to automatically deploy the application to production (Continuous Deployment) or to a staging environment for manual review (Continuous Delivery).

**Benefits:**
- Faster development cycles.
- Reduced manual errors.
- Early detection of bugs.
- Consistent and reliable deployments.

## 6. Medallion Architecture
Medallion Architecture is a data architecture pattern used in data lakes to organize data into different layers for better management and processing. It typically consists of three layers:

- **Bronze Layer**: Raw data ingested from various sources, stored in its original format.
- **Silver Layer**: Cleaned and enriched data, often aggregated or joined with other datasets.
- **Gold Layer**: Highly curated, business-ready data that is ready for reporting and analytics.

**Key Points:**
- Improves data quality and reliability.
- Facilitates data governance.
- Simplifies the data pipeline and enhances performance.

## 7. SQL Theory
SQL (Structured Query Language) is the standard language used to communicate with relational databases. SQL allows you to perform operations like querying data, updating records, and managing database structures.

**Key Concepts:**
- **SELECT**: Retrieves data from a database.
- **INSERT**: Adds new data to a table.
- **UPDATE**: Modifies existing data in a table.
- **DELETE**: Removes data from a table.
- **JOIN**: Combines rows from two or more tables based on a related column.
- **WHERE**: Filters records that meet specific conditions.

SQL is essential for interacting with relational databases, and understanding its theory helps in efficiently querying and managing data.

## 8. Python Theory
Python is a high-level, interpreted programming language known for its simplicity and readability. It’s widely used for web development, data analysis, artificial intelligence, automation, and more.

**Key Concepts:**
- **Variables**: Store data values (e.g., `x = 10`).
- **Data Types**: Different kinds of data (e.g., integers, strings, lists).
- **Control Flow**: Decision-making structures (e.g., `if`, `else`, `for`, `while`).
- **Functions**: Reusable blocks of code that perform specific tasks (e.g., `def my_function()`).
- **Modules**: Collections of functions and variables that can be imported and used (e.g., `import math`).

Understanding Python theory provides a foundation for writing efficient and maintainable code.

## 9. ACID vs CAP
### ACID (Atomicity, Consistency, Isolation, Durability)
ACID is a set of properties that ensure reliable processing in relational database transactions.

- **Atomicity**: Ensures that a transaction is all-or-nothing. If any part of the transaction fails, the entire transaction is rolled back, so no partial updates are made.
- **Consistency**: Guarantees that a transaction will bring the database from one valid state to another, maintaining database integrity.
- **Isolation**: Ensures that transactions are executed in isolation from one another, so intermediate states are not visible to other transactions.
- **Durability**: Once a transaction is committed, it is permanently recorded in the database, even if there’s a system failure.

ACID properties are crucial for applications where accuracy and data integrity are critical, such as banking systems.

### CAP (Consistency, Availability, Partition Tolerance)
CAP theorem applies to distributed systems and states that it is impossible to achieve all three properties simultaneously:

- **Consistency**: Every read receives the most recent write or an error. The system always returns a consistent view of the data.
- **Availability**: Every request receives a response, without guaranteeing that it contains the most recent data.
- **Partition Tolerance**: The system continues to operate despite network partitions, where parts of the system cannot communicate with each other.

CAP forces trade-offs; for example, in a partitioned system, you must choose between consistency and availability.

## 10. Data Modeling
Data Modeling is the process of creating a visual representation of a complex system's data structure. It’s a way to organize and structure data to ensure that it’s stored, managed, and retrieved efficiently.

**Key Components:**
- **Entities**: Objects or concepts that have data stored about them (e.g., Customer, Order).
- **Attributes**: Details about entities (e.g., Customer Name, Order Date).
- **Relationships**: Connections between entities (e.g., a Customer can place multiple Orders).

**Types of Data Models:**
- **Conceptual Model**: High-level, abstract design that shows entities and their relationships.
- **Logical Model**: More detailed, includes specific attributes, primary keys, and relationships.
- **Physical Model**: The actual implementation in a database, including tables, columns, and data types.

Data modeling ensures that data is structured logically and efficiently, facilitating easy access and manipulation.

## 11. Explain One ETL Process
ETL (Extract, Transform, Load) is a data integration process used to prepare data for analysis:

1. **Extract**: Data is collected from various source systems (e.g., databases, APIs, files). This data may be in different formats, and it’s important to capture it accurately.
2. **Transform**: The extracted data is cleaned, enriched, and transformed into a usable format. This may involve filtering out irrelevant data, converting data types, aggregating data, or applying business rules.
3. **Load**: The transformed data is then loaded into a target system, such as a data warehouse or data lake, where it can be accessed for reporting and analysis.

**Example:**
- **Extract**: Pulling sales data from an online store database.
- **Transform**: Converting all currency values to USD and filtering out transactions below a certain value.
- **Load**: Storing the cleaned data in a data warehouse for monthly sales reports.

## 12. What Did You Use for Scheduling
In data engineering, scheduling refers to automating the execution of tasks, such as ETL processes, at specific times or in response to specific events.

**Common Scheduling Tools:**
- **Apache Airflow**: A popular tool that allows you to define, schedule, and monitor workflows using Directed Acyclic Graphs (DAG
