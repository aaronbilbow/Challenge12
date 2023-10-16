# UK Food Standards Agency Data Analysis

The UK Food Standards Agency evaluates various food establishments across the United Kingdom and assigns them food hygiene ratings. This project involves working with the data from the Food Standards Agency to help the editors of the food magazine "Eat Safe, Love" evaluate and analyze the ratings data for future articles.

## Part 1: Database and Jupyter Notebook Set Up

### Data Import and MongoDB Setup

1. Open a terminal and navigate to the project directory.
2. Use the following command to import the provided data from the `establishments.json` file into a MongoDB database named `uk_food` and a collection named `establishments`:

   ```bash
   #mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json


## Part 2: Update the Database
In Part 2, we make various modifications to the database as requested by the magazine editors. We document each modification in the Jupyter Notebook.

## 1. Find and Update BusinessTypeID for "Restaurant/Cafe/Canteen"
We find the BusinessTypeID for "Restaurant/Cafe/Canteen" and update the new restaurant with the found BusinessTypeID.

## 2. Remove Establishments in Dover Local Authority
We remove establishments within the Dover Local Authority and ensure they are deleted from the database.

## 3. Convert Number Values to Correct Data Types
We convert latitude and longitude to decimal numbers and RatingValue to integer numbers.

## Part 3: Exploratory Analysis
In Part 3, we explore the database to answer specific questions from the magazine editors. We use the Jupyter Notebook named NoSQL_analysis_starter.ipynb for this analysis.

## 1. Establishments with Hygiene Score Equal to 20
We find establishments with a hygiene score equal to 20, convert the result to a Pandas DataFrame, and display the first 10 rows.

## 2. London Establishments with RatingValue Greater than or Equal to 4
We find establishments in London with a RatingValue greater than or equal to 4 using $regex, convert the result to a Pandas DataFrame, and display the first 10 rows.

## 3. Top 5 Establishments with RatingValue 5, Sorted by Hygiene Score
We find the top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score and nearest to the new restaurant "Penang Flavours."

## 4. Establishments in Each Local Authority with Hygiene Score of 0
We find the number of establishments in each Local Authority area with a hygiene score of 0, sorted from highest to lowest, and print out the top ten local authority areas using aggregation.

