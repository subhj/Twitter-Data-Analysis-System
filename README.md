# POTATO - Twitter Data Analysis System

This project is a part of an open-ended assignment to analyze tweets related to Britney Spears and provide insights based on user-defined search terms. The project leverages SQL for querying tweet data and provides detailed instructions to set up and run the system on any local machine or Google Colab.

## Overview

This project aims to provide an easy-to-use system for ingesting tweet data from TSV files into a MySQL database, querying the data, and extracting insights based on various conditions (e.g., tweets containing specific terms like "music"). The system supports querying for daily tweet counts, unique users, average likes, and more.

Key Features:
- Ingestion of TSV data files.
- Flexible SQL querying for data analysis.
- Google Colab compatibility for ease of use.


---

## Technologies Used

- **Python**: The core programming language used.
- **MySQL**: For database storage and querying.
- **SQLAlchemy**: To handle database connections and interactions.
- **pandas**: For data manipulation and analysis.
- **Google Colab**: As an optional environment for running the project in the cloud.

---

## Setup Instructions

### Option 1: Local MySQL Setup

#### 1. Install Required Libraries
Make sure you have Python installed. Install the required libraries by running:
```bash
pip install sqlalchemy pymysql pandas

Step 2: Set Up MySQL Database
Install MySQL if you don't have it already on your system.
Create a new database for this project (e.g., twitter_data).
Update the db_user, db_password, db_host, and db_name fields in the ingest.py script to match your MySQL configuration.

Step 3: Ingest Tweet Data
Place the .tsv files (containing Britney Spears tweets) into the data/ folder. Then, run the ingest.py script to load this data into the MySQL database.

Step 4: Run SQL Queries
After the data is ingested, you can run the provided SQL queries from the queries.py script to extract insights. Each query is designed to answer specific questions such as:

How many tweets contain a specific term (e.g., "music")?
Which user posted the most tweets with that term?
The average number of likes on tweets containing the term.

How to Use the System?
Install Required Libraries: Run pip install sqlalchemy pymysql pandas.
Set Up MySQL: Create a database (twitter_data) in MySQL.
Ingest Data: Run the ingest.py script to load tweet data into MySQL.
Query the Data: Use the provided SQL queries in queries.py to analyze the data.


**Design Choices and Justifications
MySQL for Data Storage:

Reason: MySQL is a widely used relational database system. It’s fast, scalable, and provides structured data storage, which is perfect for handling large datasets like tweets.
Why it's Important: Using SQL enables you to write complex queries that can efficiently process large amounts of data and return results quickly.
Python for Data Ingestion and Querying:

Reason: Python is a flexible language with powerful libraries like pandas for data manipulation and SQLAlchemy for database interaction.
Why it's Important: Python simplifies the ingestion process and makes the interaction between the .tsv files and the MySQL database seamless. Additionally, it allows you to automate data analysis tasks.
Structured Approach to Data Analysis:

Reason: Breaking the system into different components—data ingestion, querying, and analysis—makes the system modular and easy to understand.
Why it's Important: This modular approach allows you to modify each part of the system independently, making it flexible for future extensions, such as adding more features or integrating additional datasets.
Avoiding Docker:

Reason: I didn’t use Docker as it was not necessary for this setup.
Why it's Important: Keeping the system simple ensures that users can run it without additional complexities like containerization, making it easier to set up and use.
**

By following the steps outlined above, you will be able to set up the system on your own computer, ingest the data, and run queries to analyze tweets. The system design is simple yet scalable, allowing flexibility for future extensions while focusing on efficient data analysis through SQL and Python.




