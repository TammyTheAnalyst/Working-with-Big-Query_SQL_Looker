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

3. **Specifying Location**
    I used a GROUP BY clause specifying location to group the results by each location     
   
  ![]()

  ---

  Task 4: Visualizing Our Data
Saving the Query as a View
After running the query, click Save and select View. A pop-up window will appear. Choose the dataset name and name your table (e.g., total_cases_by_location).

Screenshot:

Saved View in BigQuery
A saved view is a query result that you can reuse as a table. It’s different from a saved query, which you can re-run later but won’t directly serve as a table in other queries unless re-executed.

Naming Convention
The use of underscores in names (e.g., total_cases_by_location) is a common convention in programming and database design for readability. It makes names easier to read and understand.

Visualizing the Data
To visualize the data, select all columns in the view. Remove the GROUP BY, LIMIT, and specific clauses in the SELECT statement.

Creating Visualizations

I changed the name of the visualization.
Chose location as the dimension and new_cases as the metric.
Screenshot (after changing the visualization name):

Then, I created a pie chart.
Screenshot (pie chart):

I also created a bar chart.
Screenshot (bar chart):

Added a new dimension for new_deaths and changed the color of this metric to red.
Screenshot (color change for new_deaths):

Added new_cases and new_deaths as dimensions and updated the bar chart.
Screenshot (updated bar chart with new dimensions):

---

Task 5: Saving and Sharing Reports
Saving the Query
Before sharing, you must save the query. I saved the query for later use.

Second Screenshot (saved query):

Sharing the Report
Once saved, you can share the report with others.
