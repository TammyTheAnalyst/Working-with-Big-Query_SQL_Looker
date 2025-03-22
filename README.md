# Working-with-Big-Query_SQL_Looker

---

![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4431).png)

## Working with COVID-19 Data
We are working with a COVID-19 data CSV file containing over 100,000 rows of cases

---

## Task 1: Project Overview and Navigating the Platform

---

## Task 2: Create a Project and Dataset
1. Create a new project in BigQuery.
2. Create a dataset for the project.
   
   ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4414).png)
   

3. Create a table for the dataset to hold the data by uploading the CSV file. 
   - Name the table.
   - Select the box "Auto detect schema."
   - Keep all other settings as default.

   
   ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4415).png)

---

## Task 3: Running SQL Queries for Our Data

1. **Selecting Columns**  
   In the SELECT section, choose the following columns: `location`, `date`, and `new_cases`. Then run the query.

   **Screenshot:**
   ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4416).png)

2. **Filtering by Specific Date**  
   Add the WHERE clause to return only the data for the date "2020-02-24". Use quotation marks around the date to let BigQuery know it is a date and not a string.

   ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4419).png)

4. **Specifying Location**
    I used a GROUP BY clause specifying location to group the results by each location     
   
  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4421).png)

  ---

##  Task 4: Visualizing Our Data

1. **Saving the Query as a View**

  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4422).png)

A saved view is a query result that you can reuse as a table. It’s different from a saved query, which you can re-run later but won’t directly serve as a table in other queries unless re-executed.


3. **Visualizing the Data**
To visualize the data, select all columns in the view. Remove the GROUP BY, LIMIT, and specific clauses in the SELECT statement.

4. I changed the name of the visualization.
  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4423).png)

6. I chose location as the dimension and new_cases as the metric.


7. Then, I created a pie chart.

  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4424).png)

8. I also created a bar chart.

  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4425).png)

9. Created a Line Graph and added data

  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4426).png)

10. Added new_cases and new_deaths as dimensions and updated the bar chart colors.

  ![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4428).png)

---

## Task 5: Saving and Sharing Reports
Saving the Query

![](https://github.com/TammyTheAnalyst/Working-with-Big-Query_SQL_Looker/blob/main/Screenshot%20(4429).png)
Before sharing, you must save the query. I saved the query for later use.


