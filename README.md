# Diversity and Inclusion-Dashboard

### Dashboard Link :https://app.powerbi.com/view?r=eyJrIjoiNDY0ZTg0OWEtODkxZC00ODFiLTllNWQtMjZmYThiY2UzNTQ4IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9




## Problem Statement

This dashboard helps the company understand their Diversity and Inclusion better. Human Resources at our telecom client is highly into diversity and inclusion. They’ve been working hard to improve gender balance at the executive management level, but they’re not seeing any progress.

Here we are going to identify and discuss potential root causes for the slow progress in achieving gender balance at the executive management level.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : The data is all set to create the reports.
- Step 5 : We are asked to create the following measures could help to define proper KPIs:

  - No. of men
  - No. of women
  - No. of leavers
  - % employees promoted (FY21)
  - % of women promoted
  - % of hires men
  - % of hires women
  - % turnover 
  - Average performance rating: men
  - Average Performance rating: women
- Step 6 : Calculated the count of Employees working in the company.

                        Employees = DISTINCTCOUNT(Sheet1[Employee ID])

- Step 7 : Calculated the count of Male, Female and Leavers in the company.

                        Male = COUNTX(FILTER(Sheet1,Sheet1[Gender] = "Male"),Sheet1[Employee ID])

                        Female = COUNTX(FILTER(Sheet1,Sheet1[Gender] = "Female"),Sheet1[Employee ID])

                        Leavers = COUNTX(FILTER(Sheet1,Sheet1[FY20 leaver?] = "Yes"),Sheet1[Employee ID])


- Step 8 : Visual filters (Slicers) were added for four fields named "Age group", "Gender", "Nationality", "Department" & "Job level".
- Step 9 : Six card visuals were added to the canvas, representing Total Employees, Male employees, Female employees, Leavers,  Percentage of turnover and percentage of employee promotion.
- Step 10 : A bar chart was also added to the report design area representing the number of employees working in different departments. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of employees are also seggregated according the gender. 
- Step 11 : A bar chart was also added to the report design area representing the number of employees and their job levels. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of employees are also seggregated according the gender and added female column to line y axis.
- Step 12 : - Step 10 : A bar chart was also added to the report design area representing the number of employees belonging to different age groups.
- Step 13 : Two donut chart visuals were added to the canvas, one representing percentage of employees hired according to gender and another one representing percentage of employees promoted in FY21.
- Step 14 : A stacked bar chart was added to the visual representing the rating given to the employees based on their gender.
- Step 15 : A filled map was added to the report where a field "Nationality" was added to the location and "Gender" was added to the legend
- Step 16 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area.             
 - Step 17 : New measure was created to find  average rating given to male and female employees,

                        Average Rating Male = AVERAGEX(FILTER(Sheet1,Sheet1[Gender] = "Male"),Sheet1[FY20 Performance Rating])

                        Average Rating Female = AVERAGEX(FILTER(Sheet1,Sheet1[Gender] = "Female"),Sheet1[FY20 Performance Rating])

# Insights

A report consisting of two pages was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Employees = 500

Number of Male Employees = 295

  Number of Female Employees = 205

  Number of Leavers = 47

  Percentage of Employees promoted = 10.2%

  Percentage of Turnover = 86.8%

           
### [2] Average Ratings

Average performance rating of Male Employees = 2.41 / 5 
  
  Average performance rating of Male Employees = 2.42 / 5 
  
  ### [3] Hiring Percentage
  
Hiring of Male Employees = 59%

 Hiring of Female Employees = 41%

### [4] Promotion Percentage

Promotion of Male Employees = 64.71%

Promotion of Female Employees = 35.29%


