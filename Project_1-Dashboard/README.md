# Excel Salary Dashboard

![image](https://github.com/user-attachments/assets/6dda92b9-5031-489b-8708-e94da5487eae)


## Introduction

This salary dashboard is a project I completed as part of an Excel course, designed to analyze job salaries and help professionals assess fair compensation.
The dataset used in this dashboard contains real-world salary information from 2023, covering job titles, salaries, locations, and essential skills. 
Through this project, I applied key Excel skills to organize, analyze, and visualize data effectively.

## Dashboard File
![1_Salary_Dashboard.png](/0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## Excel Skills Acquired
Throughout the project, I utilized the following Excel skills:
📉 Charts – for visualizing salary trends
🧮 Formulas and Functions – for calculating median salaries and filtering data
❎ Data Validation – for ensuring clean and structured inputs

## Dashboard Features
### 📊 Data Science Job Salaries – Bar Chart
![image](https://github.com/user-attachments/assets/0b0f08ca-3677-4c76-9200-7fb744542d6e)
- Excel Feature: Bar chart with formatted salary values
- Design Choice: Horizontal layout for easy comparison
- Data Organization: Sorted by descending salary for clarity
 -Insights Gained: Higher salaries for senior roles and engineering positions compared to analyst roles

### 🧮 Formulas and Functions
 Median Salary by Job Titles
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```
- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.
### 🍽️ Background Table
![image](https://github.com/user-attachments/assets/4b2593b5-0a38-476b-9ccc-c771eb766730)
###📉 Dashboard Implementation
![image](https://github.com/user-attachments/assets/f23fdf8b-ece0-4688-9976-32b17b2d9941)









#Skills acquired
#Talk about the data
#Dashboard build (step by step of ther final conclusion)
#Conclusion




