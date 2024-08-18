# Table of Contents

1. [Data Lake](#1-data-lake)
2. [Data Warehouse](#2-data-warehouse)
3. [PySpark vs Pandas](#3-pyspark-vs-pandas)
4. [Python OOP (Object-Oriented Programming)](#4-python-oop-object-oriented-programming)
5. [CI/CD Pipelines](#5-cicd-pipelines)
6. [Medallion Architecture](#6-medallion-architecture)
7. [SQL Theory](#7-sql-theory)
8. [Python Theory](#8-python-theory)
9. [ACID vs CAP](#9-acid-vs-cap)
10. [Data Modeling](#10-data-modeling)
11. [Explain One ETL Process](#11-explain-one-etl-process)
12. [What Did You Use for Scheduling](#12-what-did-you-use-for-scheduling)
13. [Normalization](#13-normalization)
14. [SQL Order (Explain Command)](#14-sql-order-explain-command)
15. [Partitioning](#15-partitioning)
16. [Data Lineage](#16-data-lineage)
17. [Data Governance](#17-data-governance)
18. [Data Masking](#18-data-masking)
19. [Data Warehousing Concepts](#19-data-warehousing-concepts)
20. [Data Quality Metrics](#20-data-quality-metrics)
21. [Data Security](#21-data-security)

# 1. Data Lake
A Data Lake is a large storage repository that holds vast amounts of raw data in its native format until it is needed. The data can come from various sources like logs, social media, IoT devices, or traditional databases. Unlike a data warehouse, which requires data to be processed before storage, a data lake stores data as-is and processes it only when it’s time to use it. This makes data lakes very flexible and scalable, but they require good governance to avoid turning into a disorganized "data swamp."

### Key Points:
- Stores raw data in any format (structured, semi-structured, unstructured).
- Used for big data and analytics.
- Highly scalable and cost-effective.
- Needs proper management to maintain data quality and accessibility.

# 2. Data Warehouse
A Data Warehouse is a centralized repository that stores processed and structured data, often organized into tables and schemas, optimized for querying and reporting. Data in a warehouse is typically cleaned, transformed, and integrated from various sources before storage, making it ideal for business intelligence and analysis.

### Key Points:
- Stores processed, structured data.
- Optimized for complex queries and reporting.
- Supports decision-making processes.
- Typically more expensive due to storage and processing costs.

# 3. PySpark vs Pandas
PySpark and Pandas are both data processing tools, but they serve different purposes:

**Pandas** is a Python library used for data manipulation and analysis. It’s great for small to medium-sized datasets that can fit into memory. Pandas is user-friendly, with a rich set of functionalities for cleaning, transforming, and analyzing data.

**PySpark** is the Python API for Apache Spark, a distributed computing framework. PySpark is designed for processing large-scale datasets that are too big to fit into memory on a single machine. It can handle massive data across a cluster of computers, making it ideal for big data applications.

### Key Differences:
- **Scale**: Pandas for smaller datasets; PySpark for big data.
- **Speed**: PySpark can be faster for large-scale data due to distributed processing.
- **Complexity**: Pandas is simpler to use for beginners; PySpark requires understanding of distributed computing.

# 4. Python OOP (Object-Oriented Programming)
Object-Oriented Programming (OOP) in Python is a programming paradigm that uses "objects" to model real-world entities. These objects are instances of "classes," which define the properties (attributes) and behaviors (methods) of the object.

### Key Concepts:
- **Class**: A blueprint for creating objects (e.g., a class `Car` that defines attributes like color and model, and methods like `drive`).
- **Object**: An instance of a class (e.g., `my_car` is an object of the class `Car`).
- **Inheritance**: Allows a class to inherit properties and methods from another class (e.g., `ElectricCar` inherits from `Car`).
- **Encapsulation**: Restricts access to certain components, protecting the internal state of the object.
- **Polymorphism**: Allows different classes to be treated as instances of the same class through a common interface.

# 5. CI/CD Pipelines
Continuous Integration (CI) and Continuous Deployment/Delivery (CD) pipelines are automated workflows that help in the development and deployment of software.

**CI (Continuous Integration)**: Developers frequently integrate code into a shared repository, triggering automated builds and tests to detect issues early.

**CD (Continuous Deployment/Delivery)**: After CI, the pipeline continues to automatically deploy the application to production (Continuous Deployment) or to a staging environment for manual review (Continuous Delivery).

### Benefits:
- Faster development cycles.
- Reduced manual errors.
- Early detection of bugs.
- Consistent and reliable deployments.

# 6. Medallion Architecture
Medallion Architecture is a data architecture pattern used in data lakes to organize data into different layers for better management and processing. It typically consists of three layers:

- **Bronze Layer**: Raw data ingested from various sources, stored in its original format.
- **Silver Layer**: Cleaned and enriched data, often aggregated or joined with other datasets.
- **Gold Layer**: Highly curated, business-ready data that is ready for reporting and analytics.

### Key Points:
- Improves data quality and reliability.
- Facilitates data governance.
- Simplifies the data pipeline and enhances performance.

# 7. SQL Theory
SQL (Structured Query Language) is the standard language used to communicate with relational databases. SQL allows you to perform operations like querying data, updating records, and managing database structures.

### Key Concepts:
- **SELECT**: Retrieves data from a database.
- **INSERT**: Adds new data to a table.
- **UPDATE**: Modifies existing data in a table.
- **DELETE**: Removes data from a table.
- **JOIN**: Combines rows from two or more tables based on a related column.
- **WHERE**: Filters records that meet specific conditions.

SQL is essential for interacting with relational databases, and understanding its theory helps in efficiently querying and managing data.

# 8. Python Theory
Python is a high-level, interpreted programming language known for its simplicity and readability. It’s widely used for web development, data analysis, artificial intelligence, automation, and more.

### Key Concepts:
- **Variables**: Store data values (e.g., `x = 10`).
- **Data Types**: Different kinds of data (e.g., integers, strings, lists).
- **Control Flow**: Decision-making structures (e.g., `if`, `else`, `for`, `while`).
- **Functions**: Reusable blocks of code that perform specific tasks (e.g., `def my_function()`).
- **Modules**: Collections of functions and variables that can be imported and used (e.g., `import math`).

Understanding Python theory provides a foundation for writing efficient and maintainable code.

# 9. ACID vs CAP
**ACID (Atomicity, Consistency, Isolation, Durability)**
ACID is a set of properties that ensure reliable processing in relational database transactions.

### ACID Properties:
- **Atomicity**: Ensures that a transaction is all-or-nothing. If any part of the transaction fails, the entire transaction is rolled back, so no partial updates are made.
- **Consistency**: Guarantees that a transaction will bring the database from one valid state to another, maintaining database integrity.
- **Isolation**: Ensures that transactions are executed in isolation from one another, so intermediate states are not visible to other transactions.
- **Durability**: Once a transaction is committed, it is permanently recorded in the database, even if there’s a system failure.

ACID properties are crucial for applications where accuracy and data integrity are critical, such as banking systems.

**CAP (Consistency, Availability, Partition Tolerance)**
CAP theorem applies to distributed systems and states that it is impossible to achieve all three properties simultaneously:

### CAP Properties:
- **Consistency**: Every read receives the most recent write or an error. The system always returns a consistent view of the data.
- **Availability**: Every request receives a response, without guaranteeing that it contains the most recent data.
- **Partition Tolerance**: The system continues to operate despite network partitions, where parts of the system cannot communicate with each other.

CAP forces trade-offs; for example, in a partitioned system, you must choose between consistency and availability.

# 10. Data Modeling
Data Modeling is the process of creating a visual representation of a complex system's data structure. It’s a way to organize and structure data to ensure that it’s stored, managed, and retrieved efficiently.

### Key Components:
- **Entities**: Objects or concepts that have data stored about them (e.g., Customer, Order).
- **Attributes**: Details about entities (e.g., Customer Name, Order Date).
- **Relationships**: Connections between entities (e.g., a Customer can place multiple Orders).

### Types of Data Models:
- **Conceptual Model**: High-level, abstract design that shows entities and their relationships.
- **Logical Model**: More detailed, includes specific attributes, primary keys, and relationships.
- **Physical Model**: The actual implementation in a database, including tables, columns, and data types.

Data modeling ensures that data is structured logically and efficiently, facilitating easy access and manipulation.

# 11. Explain One ETL Process
ETL (Extract, Transform, Load) is a data integration process used to prepare data for analysis:

### ETL Steps:
- **Extract**: Data is collected from various source systems (e.g., databases, APIs, files). This data may be in different formats, and it’s important to capture it accurately.
- **Transform**: The extracted data is cleaned, enriched, and transformed into a usable format. This may involve filtering out irrelevant data, converting data types, aggregating data, or applying business rules.
- **Load**: The transformed data is then loaded into a target system, such as a data warehouse or data lake, where it can be accessed for reporting and analysis.

### Example:
- **Extract**: Pulling sales data from an online store database.
- **Transform**: Converting all currency values to USD and filtering out transactions below a certain value.
- **Load**: Storing the cleaned data in a data warehouse for monthly sales reports.

# 12. What Did You Use for Scheduling
In data engineering, scheduling refers to automating the execution of tasks, such as ETL processes, at specific times or in response to specific events.

### Common Scheduling Tools:
- **Apache Airflow**: A popular tool that allows you to define, schedule, and monitor workflows using Directed Acyclic Graphs (DAGs). It’s highly flexible and suitable for complex workflows.
- **Cron Jobs**: A Unix-based scheduler that runs scripts or commands at specified times or intervals. Simple and lightweight, it’s often used for straightforward, periodic tasks.
- **Luigi**: A Python package used for building complex pipelines of batch jobs, ensuring that tasks are executed in order and handling dependencies.

Scheduling ensures that tasks are performed automatically, on time, and in the correct sequence.

## 13. Normalization
Normalization is a process in database design that organizes data to minimize redundancy and improve data integrity. It involves structuring tables and their relationships to eliminate repetitive data and ensure logical data dependencies.

### Normalization Forms:
- **1NF (First Normal Form)**: Ensures that each column contains atomic, indivisible values and that each record is unique.
- **2NF (Second Normal Form)**: Builds on 1NF by ensuring that each non-primary key column is fully dependent on the primary key.
- **3NF (Third Normal Form)**: Builds on 2NF by ensuring that non-primary key columns are only dependent on the primary key, eliminating transitive dependencies.

Normalization helps in maintaining data consistency and efficiency, though sometimes at the cost of more complex queries.

## 14. SQL Order (Explain Command)
When writing SQL queries, there’s an implicit order in which the commands are executed, known as the SQL execution order:

### SQL Execution Order:
1. **FROM**: The table(s) from which data is to be retrieved.
2. **WHERE**: Filters the rows based on specified conditions.
3. **GROUP BY**: Groups rows that have the same values in specified columns into aggregated data.
4. **HAVING**: Filters groups based on specified conditions, usually used with aggregate functions.
5. **SELECT**: Specifies which columns or expressions to return in the final result.
6. **ORDER BY**: Sorts the result set by one or more columns.
7. **LIMIT/OFFSET**: Limits the number of rows returned or specifies the starting point for the result set.

## 15. Partitioning
Partitioning is a database management technique where large tables are divided into smaller, more manageable pieces, yet still treated as a single table. This improves performance and makes it easier to manage large datasets.

### Types of Partitioning:
- **Range Partitioning**: Divides data based on ranges of values (e.g., dates, numeric ranges).
- **List Partitioning**: Divides data based on a list of discrete values (e.g., region names).
- **Hash Partitioning**: Distributes data based on a hash function applied to one or more columns, ensuring even distribution.
- **Composite Partitioning**: Combines two or more partitioning methods (e.g., range-hash).

### Benefits:
- **Improves Query Performance**: Allows the database to scan only relevant partitions.
- **Facilitates Maintenance**: Makes it easier to manage subsets of data (e.g., archiving old partitions).
- **Enhances Parallel Processing**: Enables concurrent operations on different partitions.

Partitioning is particularly useful in large databases where performance and manageability are critical.

# Data Engineering Cheat Sheet

## 16. Data Lineage
Data lineage refers to the tracking and visualization of the flow of data through various stages of its lifecycle, from its origin to its final destination. It provides a detailed view of data transformations, movements, and dependencies, which is crucial for understanding data quality and for auditing and compliance purposes.

### Key Aspects:
- **Source Tracking**: Identifies the original source of the data.
- **Transformation Details**: Shows how the data has been modified or transformed.
- **Destination**: Indicates where the data is stored or used after processing.
- **Data Flow**: Maps out the path data takes through different systems and processes.

### Benefits:
- **Improves Data Quality**: Helps in identifying and resolving data quality issues by providing visibility into data transformations.
- **Enhances Compliance**: Facilitates auditing and regulatory compliance by tracking data provenance.
- **Facilitates Troubleshooting**: Assists in debugging and resolving issues by showing how data flows and transforms.

## 17. Data Governance
Data governance involves the management of data availability, usability, integrity, and security across an organization. It encompasses policies, processes, and standards for managing data effectively.

### Key Components:
- **Data Quality**: Ensures data is accurate, consistent, and reliable.
- **Data Security**: Protects data from unauthorized access and breaches.
- **Data Stewardship**: Assigns responsibilities for managing and maintaining data.
- **Compliance**: Adheres to regulatory requirements and industry standards.

### Benefits:
- **Consistency**: Promotes uniform data management practices across the organization.
- **Risk Management**: Reduces risks related to data misuse and breaches.
- **Operational Efficiency**: Streamlines data management processes and improves data accessibility.

## 18. Data Masking
Data masking involves obscuring or hiding specific data within a database to protect it from unauthorized access, while retaining its usability for testing or analysis purposes.

### Techniques:
- **Substitution**: Replaces sensitive data with fictitious but realistic values.
- **Shuffling**: Randomly rearranges data within a column.
- **Nulling Out**: Replaces sensitive data with NULL values.
- **Encryption**: Converts data into a secure format that requires decryption.

### Benefits:
- **Protects Sensitive Data**: Safeguards personal or confidential information.
- **Maintains Data Usability**: Allows for testing and analysis without exposing real data.
- **Complies with Regulations**: Meets data protection requirements and standards.

## 19. Data Warehousing Concepts
Data warehousing involves collecting, storing, and managing large volumes of data from various sources to facilitate reporting and analysis.

### Key Concepts:
- **ETL (Extract, Transform, Load)**: The process of extracting data from sources, transforming it into a suitable format, and loading it into the warehouse.
- **Data Mart**: A subset of a data warehouse, focused on a specific business area or department.
- **OLAP (Online Analytical Processing)**: Tools that allow users to interactively analyze multidimensional data from multiple perspectives.

### Benefits:
- **Centralized Data Storage**: Provides a single source of truth for business data.
- **Enhanced Reporting and Analysis**: Facilitates complex queries and detailed reporting.
- **Improved Decision-Making**: Supports strategic planning and business decisions through comprehensive data insights.

## 20. Data Quality Metrics
Data quality metrics are used to evaluate the accuracy, completeness, consistency, and reliability of data. These metrics help ensure that data meets the required standards for effective decision-making and operational efficiency.

### Common Metrics:
- **Accuracy**: Measures how closely data matches the actual values.
- **Completeness**: Assesses whether all required data is present.
- **Consistency**: Evaluates whether data is consistent across different datasets and systems.
- **Timeliness**: Determines whether data is up-to-date and available when needed.

### Benefits:
- **Improves Data Reliability**: Ensures that data used for decision-making is accurate and dependable.
- **Enhances Business Operations**: Facilitates better business processes by maintaining high-quality data.
- **Supports Compliance**: Helps in meeting regulatory and industry standards for data quality.

## 21. Data Security
Data security involves protecting data from unauthorized access, breaches, and other threats. It encompasses various practices and technologies designed to safeguard data throughout its lifecycle.

### Key Components:
- **Access Controls**: Restricts access to data based on user roles and permissions.
- **Encryption**: Secures data by converting it into a format that is unreadable without the appropriate decryption key.
- **Backup and Recovery**: Ensures data can be restored in the event of a loss or corruption.
- **Monitoring and Auditing**: Tracks and records data access and usage to detect and respond to security incidents.

### Benefits:
- **Protects Confidential Information**: Safeguards sensitive and personal data from unauthorized access.
- **Ensures Compliance**: Helps meet regulatory requirements for data protection.


