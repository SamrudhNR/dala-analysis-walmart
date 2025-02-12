Walmart Sales Data Analysis
About
This project aims to explore the Walmart Sales data to understand top-performing branches and products, sales trends for different products, and customer behavior. The goal is to study how sales strategies can be improved and optimized. The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition.

Purposes Of The Project
The major aim of this project is to gain insight into Walmart's sales data to understand the different factors that affect sales across different branches.

About Data
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition. This dataset contains sales transactions from three different Walmart branches, respectively located in Mandalay, Yangon, and Naypyitaw. The data contains 17 columns and 1000 rows:

Analysis List
    Product Analysis
    Conduct analysis to understand the different product lines, the best-performing product lines, and those that need improvement.

    Sales Analysis
    Analyze sales trends for different products. This helps in measuring the effectiveness of sales strategies and identifying areas for improvement.

    Customer Analysis
    Uncover customer segments, purchase trends, and the profitability of each customer segment.


Approach Used
Data Wrangling

    1.This is the first step where inspection of the data is done to ensure NULL values and missing values are detected, and data replacement methods are applied.
    2.Build a database.
    3.Create tables and insert the data.
    4.Identify columns with null values. Since NOT NULL is specified for each field, null values are filtered out during table creation.

Feature Engineering
This step helps in generating new columns from existing data.

    1.Add a new column time_of_day to give insights on sales during the Morning, Afternoon, and Evening.
    2.Add a new column day_name that contains the extracted days of the week (Mon, Tue, Wed, etc.).
    3.Add a new column month_name that contains the extracted months of the year (Jan, Feb, Mar, etc.).

Exploratory Data Analysis (EDA)
   Conduct EDA to answer the listed questions and to achieve the objectives of this project.

Conclusion
   Summarize the findings and insights gathered from the analysis.

SQL Script
    -- Create database
            CREATE DATABASE IF NOT EXISTS walmartSales;

    -- Create table
            CREATE TABLE IF NOT EXISTS sales(
                invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
                branch VARCHAR(5) NOT NULL,
                city VARCHAR(30) NOT NULL,
                customer_type VARCHAR(30) NOT NULL,
                gender VARCHAR(30) NOT NULL,
                product_line VARCHAR(100) NOT NULL,
                unit_price DECIMAL(10,2) NOT NULL,
                quantity INT NOT NULL,
                tax_pct FLOAT(6,4) NOT NULL,
                total DECIMAL(12, 4) NOT NULL,
                date DATETIME NOT NULL,
                time TIME NOT NULL,
                payment VARCHAR(15) NOT NULL,
                cogs DECIMAL(10,2) NOT NULL,
                gross_margin_pct FLOAT(11,9),
                gross_income DECIMAL(12, 4),
                rating FLOAT(2, 1)
            );

