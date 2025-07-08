# Sales Insights - Data Analysis using Tableau and SQL

This repository contains a Data Analysis project focused on providing Sales Insights for an India-based hardware company. The project utilizes SQL for data extraction and transformation, and Tableau for advanced data visualization and dashboarding.

### About Project

- Performed sales insights analysis for an India-based hardware company.
- Developed ETL mappings using SQL to extract data from unstructured sources and transformed it into a staging area for data cleaning.
- Designed a star schema data model within Tableau.
- Developed a Tableau dashboard to perform quantitative analysis, producing visualizations to draw valuable insights based on parameters affecting company performance.
- Provided data-driven business solutions based on year-over-year performance trends.

## Technologies Used

- Advanced Excel: Used for initial data exploration and visualization.
- MySQL / SQL Server: Used for data storage, extraction, and transformation.
- Tableau / Power BI: Used for creating interactive dashboards and performing deep-dive analysis.
- Statistics: Applied statistical methods to interpret data trends and patterns.

## Certifications

- Data Visualization with Tableau - by Simplilearn
- Databases and SQL for Data Science with Python - by IBM
- Statistics for Data Science with Python - by IBM
- Data Visualization with Advanced Excel - by PWC

## Project - India based Hardware company Sales Insights

### Problem Statements

The Sales Director requires a clear view of company performance across various Indian states to make informed decisions regarding regional discounts and promotions.

- Q1. Revenue breakdown by cities.
- Q2. Revenue breakdown by years and months.
- Q3. Top 5 customers by revenue and sales quantity.
- Q4. Top 5 Products by revenue.
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid

#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that were previously hidden from the sales team to support decision-making and automate data gathering processes.

#### 2. Stakeholders: Who will be involved?
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick and up-to-date sales insights to support data-driven decision-making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with the latest available data.
- Sales team enabled to make better decisions, aiming for a 10% cost saving of total spend.
- Sales analysts save 20% of their business time by eliminating manual data gathering.

### Data Analysis - Approach

The project follows a structured flow from data discovery to data cleaning, followed by data modeling and finally dashboard creation.

### Setup Process

Step 1: Download the database files (db_dump.sql or db_dump.xlsx).

Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) as required.

Step 3: Use Tableau Public or Tableau Desktop to perform the data analysis.

Step 4: Connect Tableau to the MySQL database or Excel file.

Step 5: Save the analysis file as a .twb or .twbx format.

## Data Analysis Using SQL

1. Show all customer records
    `SELECT * FROM customers;`

2. Show total number of customers
    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for Chennai is Mark001)
    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distinct product codes that were sold in Chennai
    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars
    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 joined by date table
    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`

8. Show total revenue in year 2020, January Month
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";`

## Data Analysis Using Tableau

The analysis includes a Star Schema design to optimize data relationships and two primary dashboards:

1. Revenue Analysis Dashboard: Focuses on top-line growth, city-wise breakdown, and customer performance.
2. Profit Analysis Dashboard: Focuses on net profit, profit margins by market, and product profitability.

## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. MySQL Installation Guides
3. OLTP and OLAP Documentation
4. Star Schema: Fact Table and Dimension Table Documentation

## Related Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Lessons and Libraries for Data Science

## Maintainer

### Aryan Khokhar
Marketing Analyst with nearly 4 years of experience supporting campaign performance, customer engagement, and marketing reporting across digital marketing initiatives. Experienced in using SQL, Tableau, Power BI, and Google Analytics to analyze campaign data, monitor KPIs, and support data-driven marketing decisions.

- Email: khokhar.aryan13@gmail.com
- Role: Marketing Analyst
- Expertise: SQL, Tableau, Data Visualization, Campaign Analysis