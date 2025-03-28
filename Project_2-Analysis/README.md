# Project 2 Analysis

## Introduction

As a student who has completed this Excel-based data analysis course, I wanted to apply my skills to explore the data science job market. My goal was to analyze key job trends, salary distributions, and the most valuable skills for data professionals.

### Questions Analyzed

To better understand the data science job market, I explored the following questions:

1. **Do more skills result in higher salaries?**
2. **What are the salary trends for data jobs in different regions?**
3. **What are the top skills required for data professionals?**
4. **How does salary vary based on the top 10 skills?**

### Excel Skills Applied

For this analysis, I utilized the following Excel skills:

- **📊 Pivot Tables**
- **📈 Pivot Charts**
- **🧮 DAX (Data Analysis Expressions)**
- **🔍 Power Query**
- **💪 Power Pivot**

### Dataset Overview

The dataset used in this project includes real-world data science job postings from 2023. It provides insights into:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## 1️⃣ Do more skills get you better pay?

### 🔍 Skill: Power Query (ETL)

#### 📥 Extract

- I first used Power Query to extract the original data and create two queries:
    - 🗃️ First one with all the data jobs information.
    - 🔧 The second listing the skills for each job ID.

#### 🔄 Transform

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.
    - 📊 data_jobs_all

       ![image](https://github.com/user-attachments/assets/2a30ed2e-e870-4891-a55e-d96806ff4859)

    - 🛠️ data_job_skills

       ![image](https://github.com/user-attachments/assets/af84df98-7464-49ba-93bd-9322afac3450)

#### 🔗 Load

- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.
    - 📊 data_jobs_all

        ![image](https://github.com/user-attachments/assets/9d59a053-2cd7-42c7-a0f4-9ec46cd74340)

    - 🛠️ data_job_skills

        ![image](https://github.com/user-attachments/assets/3f8b26a7-9bb1-4ff1-a783-84616789024e)

### 📊 Analysis

#### 💡 Insights

- 📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.
- 💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

![image](https://github.com/user-attachments/assets/97f6185a-0a92-4ee1-8a31-0b8917c02f1b)

#### 🤔 So What

- This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.

## 2️⃣ What’s the salary for data jobs in different regions?

### 🧮 Skills: PivotTables & DAX

#### 📈Pivot Table

- 🔢 I created a PivotTable using the Data Model I created with Power Pivot.
- 📊 I moved the `job_title_short` to the rows area and `salary_year_avg` into the values area.
- 🧮 Then I added new measure to calculate the median salary for United States jobs.
    ```
    =CALCULATE(
        MEDIAN(data_jobs_all[salary_year_avg]),
        data_jobs_all[job_country] = "United States")
    ```

#### 🧮 DAX

- To calculate the median year salary I used DAX.

    ```
    Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
    ```

### 📊 Analysis

#### 💡 Insights

- 💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.
- 💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.

    ![image](https://github.com/user-attachments/assets/7cc900e0-7c36-4c70-b8bb-212825bd0d71)


#### **🤔 So What**

- These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.

## 3️⃣ What are the top skills of data professionals?

### 🔧 Skill: Power Pivot

#### 💪 Power Pivot

- 🔗 I created a data model by integrating the `data_jobs_all` and `data_jobs_skills` tables into one model.
- 🧹 Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

#### 🔗 Data Model

- I created a relationship between my two tables using the `job_id` column.

    ![image](https://github.com/user-attachments/assets/65b7024a-7d26-4814-860f-0026ec3e5be2)

#### 📃 Power Pivot Menu

- The Power Pivot menu was used to refine my data model and makes it easy to create measures.

   ![image](https://github.com/user-attachments/assets/f8aee630-1788-422d-973a-7206e9a325ed)

### 📊Analysis

#### 💡Insights

- 💻 SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.
- ☁️ Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

    ![image](https://github.com/user-attachments/assets/d1bace2b-6fae-42ef-b52f-35eb9c74e487)

#### 🤔So What

- Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.

## 4️⃣ What’s the pay of the top 10 skills?

### 📊 Skill: Advanced Charts (Pivot Chart)

#### 📈 PivotChart

- I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
    - 🪙 **Primary Axis:** Median Salary (as a Clustered Column)
    - 👍 **Secondary Axis:** Skill Likelihood (as a Line with Markers)
- To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.

### 📊 Analysis

#### 💡Insights

- 💰 Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.
- 📉 Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.

    ![image](https://github.com/user-attachments/assets/40b73623-d22a-4131-8094-a9b653614555)

### 🤔So What

- This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.

## Conclusion

Completing this project allowed me to apply my Excel skills in a real-world scenario, analyzing job trends in the data science industry. By using Power Query, PivotTables, DAX, and data visualization techniques, I gained valuable insights into the relationship between skills and salaries.

This analysis underscores the importance of technical skills like Python and SQL for professionals seeking higher-paying roles in the data field.  

Finally, I want to thank Luke Barousse for making this course a free resource on YouTube. He is an excellent teacher, and I was able to follow along very swiftly.    

### Here is his [Excel for Data Analysis Course](https://www.youtube.com/watch?v=pCJ15nGFgVg)


 
