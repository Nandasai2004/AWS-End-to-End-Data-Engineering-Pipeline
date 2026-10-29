# AWS End-to-End Data Engineering Pipeline

## 📌 Project Overview

This project demonstrates an end-to-end data engineering workflow using Amazon Web Services (AWS). It focuses on storing raw employee data in Amazon S3, configuring secure access using AWS IAM, discovering data schemas with AWS Glue Crawlers, managing metadata through the AWS Glue Data Catalog, and processing data using AWS Glue Visual ETL.

The project also includes hands-on practice with SQL using a Bank Management System and essential Linux commands.

## 🎯 Aim

To build and understand an end-to-end cloud data engineering pipeline using AWS services to store, discover, transform, and prepare structured data for analytics and reporting.

## 🎯 Objectives

- Understand Amazon S3 for cloud-based data storage.
- Configure IAM roles and permissions for secure AWS service access.
- Create an AWS Glue database and Data Catalog.
- Use AWS Glue Crawlers to discover schemas and metadata.
- Understand data transformation using AWS Glue Visual ETL.
- Organize raw and processed data using S3 folders.
- Practice SQL queries and Linux commands.

## 🛠️ Technologies Used

- **Cloud Platform:** Amazon Web Services (AWS)
- **Storage:** Amazon S3
- **Data Integration:** AWS Glue
- **Metadata Management:** AWS Glue Data Catalog
- **Security:** AWS IAM
- **Query Language:** SQL / MySQL
- **Operating System Commands:** Linux
- **Data Format:** CSV

## 🏗️ Architecture

```text
Employee CSV Dataset
        |
        v
Amazon S3 (raw/)
        |
        v
AWS IAM Role
        |
        v
AWS Glue Crawler
        |
        v
AWS Glue Data Catalog
(glue_training_db)
        |
        v
AWS Glue Visual ETL
        |
        v
Data Cleaning and Transformation
        |
        v
Amazon S3 (curated/)
        |
        v
Amazon Athena
(Analytics and Reporting)
```

## ⚙️ Implementation Steps

### 1. Create an Amazon S3 Bucket
- Create an S3 bucket to store the employee dataset.
- Create a `raw/` folder.
- Upload the `employees.csv` file into the raw data folder.

### 2. Configure AWS IAM
- Create or configure an IAM role for AWS Glue.
- Grant the required permissions to access the source data in S3.
- Follow the principle of least privilege when assigning permissions.

### 3. Create an AWS Glue Database
- Open the AWS Glue console.
- Create a database named `glue_training_db`.
- Use the database to organize the metadata discovered from the dataset.

### 4. Configure the AWS Glue Crawler
- Create a Glue Crawler.
- Configure Amazon S3 as the data source.
- Select the appropriate IAM role.
- Choose `glue_training_db` as the target database.
- Run the crawler to discover the CSV schema and create a Data Catalog table.

### 5. Transform Data Using AWS Glue Visual ETL
- Open AWS Glue Studio.
- Create a Visual ETL job.
- Select the employee table from the Data Catalog.
- Configure transformations as required.
- Prepare the output for storage in the curated data location.

Possible transformations include:
- Handling missing values.
- Removing duplicate records.
- Selecting required columns.
- Cleaning and organizing employee data.

### 6. Store Processed Data in Amazon S3
- Configure the output destination as the `curated/` folder.
- Select the appropriate output format and job settings.
- Run the ETL job and verify the generated output.

### 7. Analytics and Reporting
The curated dataset can be queried using Amazon Athena after the appropriate table metadata and output format are configured.

## 📊 Sample Dataset

The project uses an employee dataset with fields such as:

| Column | Description |
|---|---|
| `employee_id` | Unique employee identifier |
| `name` | Employee name |
| `department` | Employee department |
| `salary` | Employee salary |
| `city` | Employee city |

Example:

```csv
employee_id,name,department,salary,city
101,Rahul,IT,60000,Bangalore
102,Priya,HR,50000,Hyderabad
103,Arjun,IT,75000,Chennai
104,Sneha,Finance,65000,Bangalore
105,Kiran,IT,55000,Hyderabad
```

## 🗄️ SQL Practice: Bank Management System

The project documentation also includes SQL practice using a Bank Management System.

Topics covered:

- Database and table creation.
- Inserting records into tables.
- Displaying and verifying table data.
- Filtering customers by city.
- Sorting accounts by balance.
- Calculating total and average account balances.
- Finding minimum and maximum account balances.
- Counting customers and grouping accounts by type.
- Joining transaction details with customer information.
- Filtering deposit transactions.
- Calculating employee salary expenditure.
- Grouping employees by designation.

Tables include:
- Customers
- Accounts
- Transactions
- Employees
- Branches

## 🐧 Linux Command Practice

The project includes basic Linux terminal commands:

| Command | Purpose |
|---|---|
| `pwd` | Display the current working directory |
| `ls` | List files and directories |
| `ls -l` | Display detailed file information |
| `ls -a` | Show hidden files and directories |
| `whoami` | Display the current username |
| `date` | Display the system date and time |
| `clear` | Clear the terminal screen |
| `mkdir` | Create a directory |
| `touch` | Create an empty file |
| `cat` | Display file contents |
| `cp` | Copy files |
| `rm` | Remove files |
| `nano` | Create or edit text files |

## ✅ Key Learnings

- Understanding cloud-based data storage with Amazon S3.
- Managing AWS service permissions using IAM.
- Discovering schemas and registering metadata with AWS Glue.
- Understanding the role of the Glue Data Catalog in data management.
- Learning the stages of an ETL pipeline.
- Understanding raw and curated data organization.
- Practicing SQL queries for data retrieval and reporting.
- Developing Linux command-line skills.

## 🚀 Future Enhancements

- Automate pipeline execution using AWS Glue Workflows or scheduled triggers.
- Add Amazon S3 event notifications for event-driven processing.
- Implement data quality checks and validation.
- Integrate Amazon Athena for SQL-based analytics.
- Build dashboards using Amazon QuickSight.
- Add logging, monitoring, and error-handling mechanisms.

## 👨‍💻 Author

**Gorlamandala Nanda Sai**

- Degree: B.Tech – Artificial Intelligence and Machine Learning
- University: JAIN Deemed-to-be University
- Batch: 2023–2027

## 📄 Documentation

The project documentation contains screenshots of the AWS console configuration, SQL practice, Linux commands, Glue Data Catalog setup, crawler configuration, and the data processing workflow.

---

⭐ If you find this project useful, feel free to explore the repository and provide feedback.
