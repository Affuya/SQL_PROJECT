# Final-Project-Transforming-and-Analyzing-Data-with-SQL

## Project/Goals
(fill in your description and goals here)
The purpose of this project was to analyze the provided database in order to gain insights and extract valuable information. The project aimed to demonstrate the process of data exploration, cleaning, analysis, and quality assurance (QA) using SQL queries.

## Process
### (your step 1)
### (your step 2)
-- STEP 1: Created all_sessions_excel table directly from pgadmin
-- STEP 2: Created products-excel table using code below

CREATE TABLE IF NOT EXISTS products(
	SKU VARCHAR(50),
	name VARCHAR(300),
	orderedQuantity INT DEFAULT 0,
	stockLevel INT DEFAULT 0,
	restockingLeadTime INT DEFAULT 0,
	sentimentScore FLOAT,
	sentimentMagnitude FLOAT);
	
-- STEP 3: Creating sales_by_sku_excel table with code below
CREATE TABLE IF NOT EXISTS sales_by_sku(
	productSKU VARCHAR(100),
	total_ordered INT DEFAULT 0);
	
-- STEP 4: Creating analytics-excel table using below code
CREATE TABLE IF NOT EXISTS "analytics"(
	visitNumber	INT DEFAULT 0,
	visitId INT PRIMARY KEY,
	visitStartTime TIME,
	date DATE,
	fullvisitorId INT DEFAULT 0,
	userid INT,
	channelGrouping VARCHAR(300),
	socialEngagementType VARCHAR(300),
	units_sold INT DEFAULT 0,
	pageviews INT DEFAULT 0,
	timeonsite TIMESTAMP,
	bounces INT DEFAULT 0,
	revenue INT DEFAULT 0,
	unit_price INT DEFAULT 0);
	
-- STEP 5 Creating sales_report-excel table using below code
CREATE TABLE IF NOT EXISTS "sales_report"(
	productSKU VARCHAR(50),
	total_ordered INT DEFAULT 0,
	name VARCHAR(100),
	stockLevel INT DEFAULT 0,
	restockingLeadTime INT DEFAULT 0,
	sentimentScore FLOAT,
	sentimentMagnitude FLOAT,
	ratio FLOAT);

## Results
(fill in what you discovered this data could tell you and how you used the data to answer those questions)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
