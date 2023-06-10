# SheSharp Competition - Job Description Analysis

This repository contains code and data analysis for the SheSharp competition. The goal of this project is to extract skills from job descriptions. Below are the steps followed in the analysis:

## project idea: 
For new graduates and starters, job seeking are always confusing. The skills required at job market are not taught in school. Therefore, we want to come up with a wordcloud (most frequently wanted skills/tech stack) for each type of IT job. Having this as a reference, job seekers can have a more targeted preparation for the market. For those whose skill sets have already some overlapping with the market need, they can feed our wordcloud and their original cover letter to gpt to write a cover letter that has higher chance to pass the Application Tracking System. For the future, we can train a Generative AI to facilitate the experienced job seaker in tailoring their cover letter to the IT sector they are applying to.


## Read the Data
We start by reading the data from two datasets: `<data-global>` and `<data-NL>`. These datasets contain job descriptions that we will analyze to extract skills.

## Data Cleaning and Normalization
In this step, we normalize the data by performing the following actions:
- Convert all text to lowercase to ensure consistency.
- Remove dashes and spaces to clean up the text.

### Filter the Data
In this step, we further clean the data by removing specific job titles that are not relevant to our analysis. For example, we didn't count "security officer" in job titles.

### Categorize 
To simplify the analysis, we create 12 job categories based on specific job titles. For example:
```python
data_engineer_nl = df_NL[df_NL['job_name'].str.contains("data engineer")] 
```
This code filters the dataset to select only job descriptions related to data engineers. We repeat this process for other job categories as well.

## Wordcloud Visualization
To visualize the extracted skills, we employ the Wordcloud technique. This technique generates a visual representation of the most frequently occurring words in the job descriptions, providing insights into the key skills sought by employers.

For Wordcloud Visualization for global dataset, check https://github.com/xiaoyanwu077/SheSharp_competition/blob/main/job_posting_analysis-global.ipynb

For the Netherlands dataset, check https://github.com/xiaoyanwu077/SheSharp_competition/blob/main/data-analysis-ela-nl.ipynb

Data_engineer:

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/0118b9d3-0709-441e-b40f-17d0d0b51843)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/50feeef4-928b-4f6a-bb61-14a4903d6087)


Data Scientist

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/e20435ac-38a5-466d-8e16-dbb09c637328)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/6a8d8f2a-08db-424d-ae30-bf97e6e3691a)


Front-End Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/dc0fafed-8dfe-45d5-815d-a60071df4a20)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/7597756d-5d29-4ffe-b53d-6216c2ef2e12)


Back-End Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/dcfaa8e3-65c1-414c-b023-61403ab9bcb3)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/9293aef3-37f9-48cf-afe6-76f925de2791)


Data Analyst

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/b45412e0-77af-4dc5-8631-67e9c85dd142)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/3392b7d7-d35d-484c-8780-3bd29056df62)


Full Stack Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/9d5e2d7e-53fc-4ef9-b4b2-f14693ffbd1f)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/078f9630-92c1-4364-891c-e8a57c618443)


Product Manager

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/f39bf800-5990-485f-86e8-00819b826225)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/5338406b-ddcc-43a6-b85d-d99c2552b67a)


Product Owner

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/4146adb5-e860-49b4-8a82-c6865299a777)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/8b30c9d8-0ae5-4d7a-b3cf-3b01b0987c0b)


Quality Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/fd43b1b7-4f72-4c49-ab1c-bf39b814d7f4)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/286789de-bf10-434e-b931-66ecbeca6bb4)


Support Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/cecdb3fc-c332-479d-8060-781d0cb7d0fb)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/7c2104e8-cd61-451b-915a-a35590aa13ff)


Devops Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/56379fcc-6331-4339-ba0f-459e1d9fd759)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/276e6e0f-4924-4ff7-bfbd-55b4b035eb4e)


Security Engineer

![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/6e6d0452-e36d-41b3-acce-cf2f02d5da9e)
![image](https://github.com/xiaoyanwu077/SheSharp_competition/assets/56236129/23a40f0b-7071-4860-95b4-bdb2818038ce)

