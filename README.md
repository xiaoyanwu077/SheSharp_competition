# SheSharp Competition - Job Description Analysis

This repository contains code and data analysis for the SheSharp competition. The goal of this project is to extract skills from job descriptions. Below are the steps followed in the analysis:

## project idea: 
For new graduates and starters, job seeking are always confusing. The skills required at job market are not taught in school. Therefore, we want to come up with a wordcloud (most frequently wanted skills/tech stack) for each type of IT job. Having this as a reference, job seekers can have a more targeted preparation for the market. For those whose skill sets have already some overlapping with the market need, they can feed our wordcloud and their original cover letter to gpt to write a cover letter that has higher chance to pass the Application Tracking System. For the future, we can train a Generative AI to facilitate the experienced job seaker in tailoring their cover letter to the IT sector they are applying to.


## Read the Data
We start by reading the data from two datasets: `<data-global>` and `<data-NL>`. These datasets contain job descriptions that we will analyze to extract skills.

## Clean the Data
To do fuzzy matching for job name, we normalize the job name column by converting to lower case, removing tabulation, punctuation, and special characters.
### Data Normalization
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
