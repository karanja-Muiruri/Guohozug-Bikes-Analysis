# Guohozug-Bikes-Analysis

# Table of Contents
  - [Project Overview](#project-overview)
  - [Data Sources](#data-sources)
  - [Tools](#tools)
  - [Data Preparation](#data-preparation)
  - [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Data Analysis](#data-analysis)

## Project Overview

This data analysis project aims to highlight key performance metrics for Guohozug Bikes that is geared towards informed decision making.

## Data Sources

The Primary dataset used in this analysis includes; 
  - bike_share_yr_0.csv
  - bike_share_yr_1.csv
  - cost_table.csv

## Tools

- MySQL (SQL Server Management Studio) - Data Analysis
- PowerBI - Creating a report

## Data Preparation

Tasks involved;
1. Data loading and Inspection.
2. Data cleaning and formatting.

## Exploratory Data Analysis

EDA involved exploring the csv data to answer the following;
  - Hourly Revenue Analysis
  - Profit and Revenue Trends
  - Seasonal Revenue
  - Rider Demographics

## Data Analysis

  1. Creating a Database;
     I created a new database in Microsoft SQL Server Management Studio called Bicycles_Data;
     
      - ![002](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/ac91a1ac-fd29-4e3a-af4d-81164afc33ef)

     Followed by uploading the bike_share csv files into the database;
     
      -  ![003](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/f2a397fb-b9c9-4226-b132-b00c557635fe)
      -  ![004](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/5b6061de-fec1-499c-82e5-748a30f57c5d)
      -  ![007](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/f8c38568-5bc5-48e2-a41c-27995f4ad9f7)
      -  ![008](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/5bda62ea-6716-4d17-a34d-1c88c9183bdb)
      -  ![009](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/a51b52c4-c859-4bea-86cb-98c2307fd2db)
    
  2. Developing SQL Queries;

      Both 'bike_share_yr_0' and 'bike_share_yr_1' files have similar number of columns and names; thus I performed a UNION on the two data sets.
       - ![011](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/cc4ba493-677f-4860-971f-2d88ccdc5a91)
    
      However, the 'cost_table' data set is completely different, having only three columns. The 'yr' columns from both the UNION and 'cost_table' do match. I did a LEFT JOIN, where the UNION table is on the LEFT (thus ensuring all data from the LEFT table is included) and the much needed 'price' and 'COGS' columns from 'cost_table' are included. I also did a WITH query to name the UNION table AS Common_Table_Expression to aid in writing the LEFT JOIN query.

       - ![012](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/9a019401-66f4-4664-9fe8-aad6e7a841bd)
       - ![013](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/5a927a6b-fb67-4c44-90af-dae02098d099)



     





       


    







     






