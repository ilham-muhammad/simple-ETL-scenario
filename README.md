# Simple ETL (Extract, Transform, & Load) Scenario

## About
This repository is to simulate simple data engineering, an end-to-end ETL pipeline scenario.

## Stakeholder's Problems
In a relatively new company having some teams consist of Sales, Product, and Data Scientist. The company's data are scattered and each teams are having issues as follows:
- Sales Team : already record their sales data in a PostgreSQL database within a Docker containers, but with unproper format & some missing values.
- Product Team : already record their product & pricing data stored in .csv format within local server/storage, but having same issues as Sales Team.
- Data Scientist Team : a new team that just formed, they need to gather text data from an existing website to do some NLP research.

## Proposed Solutions
Based on stated problems, we proposed a solutions : *A Centralized Data Warehouse*. The solutions can be breakdown as a simple ETL :
1. Extract, taking data from each scattered source
   - Sales Team : load the PostgreSQL DB within a Docker containers
   - Product Team : load the .csv data within a local server/storage
   - Data Scientist Team : create a web scrapping program then store the data in any format
   All extracted data will be processed using Python, Pandas DataFrame 
2. Transform, modifiying data into a proper & consistent formating
   - Checking the proper data types in each columns
   - Handling missing values
   - Handling duplicated, inconsistent, & mismatched data
3. Load, all of cleaned data will be saved as separated columns for each teams, stored as PostgreSQL DB format
4. ETL Pipelining, make the process automated & scheduled

## ETL Pipeline Design
The solutions above are visualized as follows :




# ETL Implementation
   
