# SheSharp Competition - Job Description Analysis

This repository contains code and data analysis for the SheSharp competition. The goal of this project is to extract skills from job descriptions. Below are the steps followed in the analysis:

## Read the Data
We start by reading the data from two datasets: `<data-global>` and `<data-NL>`. These datasets contain job descriptions that we will analyze to extract skills.

## Clean the Data
### Data Normalization
In this step, we normalize the data by performing the following actions:
- Convert all text to lowercase to ensure consistency.
- Remove dashes and spaces to clean up the text.

### Date Filtering
In this step, we further clean the data by removing specific job titles that are not relevant to our analysis. For example, we removed "security officer" and "security engineer" in job titles.

## Categorization
To simplify the analysis, we create 11 job categories based on specific job titles. For example:
```python
data_engineer_nl = df_NL[df_NL['job_name'].str.contains("data engineer")] 
```
This code filters the dataset to select only job descriptions related to data engineers. We repeat this process for other job categories as well.

## Wordcloud Visualization
To visualize the extracted skills, we employ the Wordcloud technique. This technique generates a visual representation of the most frequently occurring words in the job descriptions, providing insights into the key skills sought by employers.


