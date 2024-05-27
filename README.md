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
       - ![014](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/fbdcfa11-ce2e-46c0-b9b4-39ac9f7cbc76)
    
      
  I calculated revenue by multiplying riders by price and also calculated profit by taking revenue minus (riders*COGS).
  
  - ![018](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/3d0fdcf3-eeaf-46eb-a68e-ba3934808126)


3. Connecting Power BI to the Bicycles_Data Database

    Involves getting data from SQL Server and adding the final MSSMS query.
     -  ![0155](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/a950124b-e460-42e3-bccc-07fc6742361b)
     -  ![019](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/382febcd-dba2-433e-81f4-8358553aba05)
  
4. Building the dashboard in Power BI

    The various steps followed to conclusion.

     - I did use a blank query to create a Date table and create a relationship ON date.

         - ![029](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/79f05bda-9415-4324-8f73-3c479143a68f)
         - ![030](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/c69fdb8d-2dda-4135-9d4c-3325b4b76d99)
         - ![032](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/aeb1d653-e089-4d50-a329-016897625729)
      
     - The building of the dashboard to conclusion.      

         -  ![033](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/67e76a4b-b34a-4b40-94c0-72de8dd5d123)
         -  ![034](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/f963b17d-624b-4e0f-aeda-1b1d86388ff7)
         -  ![035](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/cb7b6e3b-5219-41d7-8a6a-a09bddfaa69d)
         -  ![036](https://github.com/karanja-Muiruri/Guohozug-Bikes-Analysis/assets/169806532/4cd3f61c-9d31-41b9-b9b5-9b15f4ffb984)



## Recommendation

  1. Conservative Increase;
       Considering the substantial increase last year, a more conservative increase might be prudent to avoid hitting a price ceiling where demand starts to drop. An increase in the   
       range of 10-15% could test the market's response without risking a significant loss of customers.

  3. Price Setting;
       - If the price in 2022 was $4.99, a 10% increase would make the new price about $5.49.
       - A 15% increase would set the price at approximately $5.74.

    Recommended Strategy:
      - Market Analysis; Conduct further market research to understand customer satisfaction, potential competitive changes, and to the overall economic environment. This can guide 
          whether leaning towards the lower or higher end of the suggested increase.
      - Segmented Pricing Strategy; consider different pricing for casual versus registered users, as they may have different price sensitivities.
      - Monitor and Adjust; Implement the new prices but be ready to adjust based on immediate customer feedback and sales data. monitoring closely will allow you to fine-tune your   
          pricing strategy without commiting fully to a price that might turn out to be too high. 
  
     
     


   


   


     





       


    







     






