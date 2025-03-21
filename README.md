# Working-with-Big-Query_SQL_Looker


## Working with COVID-19 Data
We are working with a COVID-19 data CSV file containing over 100,000 rows of cases, available at [data.humdata.org/event/covid-19](https://data.humdata.org/event/covid-19).

---

## Task 1: Project Overview and Navigating the Platform

---

## Task 2: Create a Project and Dataset
1. Create a new project in BigQuery.
2. Create a dataset for the project.
   
   **Screenshot:**
   ![]()

3. Create a table for the dataset to hold the data by uploading the CSV file. 
   - Name the table.
   - Select the box "Auto detect schema."
   - Keep all other settings as default.

   **Screenshot:**
   ![]()

---

## Task 3: Running SQL Queries for Our Data

1. **Selecting Columns**  
   In the SELECT section, choose the following columns: `location`, `date`, and `new_cases`. Then run the query.

   **Screenshot:**
   ![]()

2. **Filtering by Specific Date**  
   Add the WHERE clause to return only the data for the date "2020-02-24". Use quotation marks around the date to let BigQuery know it is a date and not a string. 
   
   ```sql
   SELECT location, date, new_cases 
   FROM `working-w-big-query-project.COVID_Dataset.covid_data`
   WHERE date = '2020-02-24'
