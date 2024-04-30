# Retail-Store-Data-Modeling-and-Analysis-using-DataStage
# Retail Store Data Modeling and Analysis using DataStage

## Project Overview
The project implements a star-schema data warehousing flow, then utilizes IBM InfoSphere DataStage to develop efficient ETL (Extract, Transform, Load) pipelines to create data marts and perform some analysis on them.

The objective is to store and analyze data from a fictional retail store in a star-schema-based analysis data warehouse while ensuring all changes in the dimensions are preserved.

## Problem Statement
A fictitious national department store decided to build a star-schema-based sales analysis data warehouse with the dimensions of customer, store, and product. Over time, dimension attributes are expected to change.

The requirement is to preserve versions of all changes in the star-schema data warehouse to deliver accurate results with queries that relate to prior versions of dimension attributes.

## Data Source
The data source for populating the star schema is the store's online transaction processing (OLTP) system.

[![Data Source Screenshot](https://link.to.screenshot)](https://link.to.screenshot)

## Project Steps
The IBM InfoSphere DataStage tool is mainly used as an ETL tool to solve the problem.

1. **Building the Physical Data Model:** A star schema is built with three dimensions: product, retail, and customer. And a fact table: transactions.

   ![ERD with colored entities (UML notation)](https://link.to.ERD)

2. **Extraction:** Extract the data from the data warehouse, ensuring the inclusion of relevant customer, store, and product information.

3. **Transformation:** Perform some transformations on the extracted data to align it with the business needs. This includes converting customer name columns to uppercase.

4. **Data Mart Creation:** A data mart named RETAIL_DATA_MART is developed. It contains each transaction for each customer, categorized by customer type ("citizen" or "foreign"), information about the product, and the stock purchased.

5. **Loading:** The transformed data will be loaded into the data mart RETAIL_DATA_MART.

6. **Data Mart Analysis:** The data mart RETAIL_DATA_MART is used to answer some business needs:

   - Display the count of all transactions for each employee in each store.
   - Identify the customer type ("citizen" or "foreign") that generates the highest profit. For example, if "foreign" customers make 5 transactions and citizen "customers" make 3 transactions, the maximum profit would be attributed to foreign customers.
   - A bonus is given to the customer(s) who contribute the most to the profit.

## Project Files
- **DataStage Jobs:** Contains the dsx files for the DataStage jobs.
- **Dataset:** Contains the data after it is modeled in a star schema data warehouse model.
- **MetaData:** Contains the metadata of the table to be used in the DataStage jobs.
- **Output_Data:** Contains samples of the data after analyzing it.

## DataStage Jobs
- **Q1**
- **Q2 P1**
- **Q2 P2**
- **Q2 P3** *(Description missing)*
