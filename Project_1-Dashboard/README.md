# Excel Salary Dashboard

![image](https://github.com/user-attachments/assets/6dda92b9-5031-489b-8708-e94da5487eae)

## Introduction

This salary dashboard is a project I completed as part of an Excel course, designed to analyze job salaries and help professionals assess fair compensation.
The dataset used in this dashboard contains real-world salary information from 2023, covering job titles, salaries, locations, and essential skills. 
I applied key Excel skills to organize, analyze, and visualize data effectively through this project.

## Dashboard File
My final dashboard is in [Data Salary Calculator](https://github.com/KevinHoyos96/Excel_Project-Data_Analytics/blob/main/Project_1-Dashboard/Data%20Salary%20Calculator.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

<img src="https://github.com/user-attachments/assets/3adcd776-6871-4137-bcec-2e39c0b3856c" width="500">


- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

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

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

![image](https://github.com/user-attachments/assets/cec7f988-e3dd-4636-98b3-ca75615e8e48)

📉 Dashboard Implementation

<img src="https://github.com/user-attachments/assets/3980cadc-5297-453b-b606-13c62f9cf1bb" width="500">

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

![image](https://github.com/user-attachments/assets/07d0087e-5cc5-47ab-bac7-b8c5e56f672d)

📉 Dashboard Implementation:

<img src="https://github.com/user-attachments/assets/b103901b-9eec-4e78-befc-ab26c30cd637" width="400">

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![image](https://github.com/user-attachments/assets/33f7096e-0ee5-4c3e-a18c-a5e7351a43f4)

## Conclusion

Completing this project allowed me to reinforce my Excel skills and gain hands-on experience in data analysis. By building this salary dashboard, I developed a better understanding of how job titles, locations, and work types influence salaries.
This project demonstrates my ability to clean, analyze, and visualize real-world datasets using Excel.

Finally, I want to thank Luke Barousse for making this course a free resource on YouTube. He is an excellent teacher, and I was able to follow along very swiftly.    

### Here is his [Excel for Data Analysis Course](https://www.youtube.com/watch?v=pCJ15nGFgVg)







