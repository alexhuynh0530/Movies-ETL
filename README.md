# An Analysis of Movies using ETL (Extract, Transform, Load)

## Overview of Project

### Purpose

This is an analysis using the data pipeline process: ETL (extract, transform, load). There are 2 data sources we use, a scrape of Wikipedia and rating data from MovieLens website using Kaggle data. We extract data from the two sources, transform it into one clean dataset, and then load into SQL.

## Results

### Write an ETL Function to Read Three Data Files

Using Python, Pandas, the ETL process, and code refactoring, we write a function that reads in the three data files and creates three separate DataFrames.

![ETL_function_test.ipynb](https://github.com/alexhuynh0530/Movies-ETL/blob/main/ETL_function_test.ipynb)

### Extract and Transform the Wikipedia Data 

Using Python, Pandas, the ETL process, and code refactoring, we extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, we use a try-except block to catch errors.

![ETL_clean_wiki_movies.ipynb](https://github.com/alexhuynh0530/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb)

### Extract and Transform the Kaggle Data

Using Python, Pandas, the ETL process, and code refactoring, we extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, we merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, we merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

![ETL_clean_kaggle_data.ipynb](https://github.com/alexhuynh0530/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb)

### Create the Movie Database

Useing Python, Pandas, the ETL process, code refactoring, and PostgreSQL, we add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.

![ETL_create_database.ipynb](https://github.com/alexhuynh0530/Movies-ETL/blob/main/ETL_create_database.ipynb)

#### Confirmation of Movie Table Count 

![movies_query.png](https://github.com/alexhuynh0530/Movies-ETL/blob/main/Resources/movies_query.png)

#### Confirmation of Ratings Table Count 

![ratings_query.png](https://github.com/alexhuynh0530/Movies-ETL/blob/main/Resources/ratings_query.png)

## Summary

In summary, we learn the process of extracting data, transforming it to one clean dataset, and loading it to a SQL table.
