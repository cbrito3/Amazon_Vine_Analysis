# Amazon_Vine_Analysis_Report

## Overview of the analysis: 

The purpose of this analysis is to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
For this project, I selected the following dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Shoes_v1_00.tsv.gz . After selecting the dataset and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. For the second part of the project, I used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. 

## Deliverables include the following:
* Deliverable 1: Perform ETL on Amazon Product Reviews
* Deliverable 2: Determine Bias of Vine Reviews
* Deliverable 3: A Written Report on the Analysis (README.md)

  # Perform ETL on Amazon Product Reviews 
  * The Amazon_Reviews_ETL.ipynb file does the following:
    - An Amazon Review dataset is extracted as a DataFrame
    - The extracted dataset is transformed into four DataFrames with the correct columns 
    - All four DataFrames are loaded into their respective tables in pgAdmin 

  # Determine Bias of Vine Reviews
  * The analysis and Vine_Review_Analysis.ipynb fil do the following:
    - There is a DataFrame or table for the vine_table data using one of three methods above 
    - The data is filtered to create a DataFrame or table where there are 20 or more total votes 
    - The data is filtered to create a DataFrame or table where the percentage of helpful_votes is equal to or greater than 50% 
    - The data is filtered to create a DataFrame or table where there is a Vine review 
    - The data is filtered to create a DataFrame or table where there isn’t a Vine review 
    - The total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews

## Results: Using bulleted lists and images of DataFrames as support, address the following questions:
* How many Vine reviews and non-Vine reviews were there?
  
  There were a total of 27,009 reviews of which 22 were Vine reviews and 26,987 were non-Vine reviews.

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  
  There were a total of 14,488 reviews that were 5 stars, 13 were Vine reviews and 14,475 non-Vine reviews. 
  
* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  
  Based on there results 59.09% of paid (Vine) reviews were 5-stars and 53.64% of unpaid (non-Vine) reviews were 5-stars.

## Summary: 
  Based on the results there is bias and is supported by the results. From a total of 27,009 reviews, 22 were Vine reviews and the rest were non-Vine reviews, this is a very small number to sample. One additional analysis step that could help support my statement is to add another filter and see if the result of any bias changes.
  
