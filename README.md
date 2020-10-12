# School_District_Analysis

## Project Overview

Help a chief Data Scientist for a City School District to analyze data on student funding and student's standardize test scores by to agregating the data and show trends in school performance to the school board to make decisions regarding the school budget and priorities.

I was given with the following tasks to complete:
1. A high-level snapshot of the district's key metrics, presented in a table format.
2. An overview of the key metrics for each school, presented in a table format.
3. Tables presenting each of the following metrics:
- Top 5 and bottom 5 performing schools, based on the overall passing rate
- The average math score received by students in each grade level at each school
- The average reading score received by students in each grade level at each school
- School performance based on the budget per student
- School performance based on the school size 
- School performance based on the type of school

## Resources

- Data source: schools_complete.csv and students_complete.csv
- Software: Jupyter Notebook 6.1.4

## Results

Reading and math grades for Thomas High School ninth graders appeared to have been altered and I was asked to repeat the analysis once I replaced those scores with NaNs while keeping the rest of the data intact. See image below for reference:

![student_data_with_NaN](https://user-images.githubusercontent.com/70611325/95794965-0436d300-0c9e-11eb-9873-036ce1e1c6a6.png)

***How is the district summary affected?***

After replacing the scores, we noticed a significant decrease on the following variables:
- Average Math Score
- Passing Math Percentage
- Passing Reading Percentage
- Overaal Passing Percentage

The only variable that did not suffer any modification is the Averga Reading Score. See images below for reference:

![district_summary_df](https://user-images.githubusercontent.com/70611325/95795388-136a5080-0c9f-11eb-973a-21dcfa49dd36.png)
<img width="1084" alt="New_district_summary_df" src="https://user-images.githubusercontent.com/70611325/95795389-1402e700-0c9f-11eb-98fe-98488714ca67.png">

***How is the school summary affected?***

We can see that both the Average Math Score and Average Reading Score for Thomas High School slightly suffered any modification after the decimal point, but we see a decrease of more than 20% in the percetages of students passing Math, Reading and the Overall Passing percentage. See images below:

![per_school_summary](https://user-images.githubusercontent.com/70611325/95796440-bae88280-0ca1-11eb-8be6-fd0904071f40.png)
<img width="1008" alt="New_per_school_summary" src="https://user-images.githubusercontent.com/70611325/95796441-bb811900-0ca1-11eb-91b7-6b4d962f9a72.png">

***How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?***

Based on the new results, is clear that not counting the grades of the ninth graders from Thomas High School affected negatively their performance since they were second place in the top schools with and overall percentage of 90.95%.

I calculated the number of students from 10th grade to 12th from Thomas High School and recalculate the percentage of students who passed math, passed reading and passed both math and reading. Once I obtained the new figures for the passing percentages I replaced them in the School Summary DataFrame. After doing this I noticed the following:
- The math and Reading scores by grade remained the same.
- The scores by school spending figures slightly changed after the decimal point for the group that Thomas High School is in, which is "$630-644". See images below:

![spending_summary](https://user-images.githubusercontent.com/70611325/95798062-d5bcf600-0ca5-11eb-8373-fc312e3e7d9d.png)
<img width="836" alt="new_spending_summary" src="https://user-images.githubusercontent.com/70611325/95798067-d6ee2300-0ca5-11eb-978b-4ad45d472003.png">

- The scores by school size also had a slightly changed after the decimal point for the group that Thomas High School is in, which is "Medium (1000-2000)". See images below:

![size_summary](https://user-images.githubusercontent.com/70611325/95798893-fbe39580-0ca7-11eb-9c31-c5aee19e56f9.png)
<img width="758" alt="new_size_summary" src="https://user-images.githubusercontent.com/70611325/95798899-fd14c280-0ca7-11eb-94d0-575ea65c81ba.png">

- The scores by school type reflected a slightly changed after the decimal point for Charter School Type, see images below:

![type_summary](https://user-images.githubusercontent.com/70611325/95798920-0c940b80-0ca8-11eb-8d59-e10330795259.png)
<img width="722" alt="new_type_summary" src="https://user-images.githubusercontent.com/70611325/95798924-0d2ca200-0ca8-11eb-9569-3804149466d7.png">

## Summary

- The count of students that have scores was reduced.
- The averages of scores were decreased.
- The overall passing percentage was reduced.
- Before recalculating with only 10th to 12th graders, Thomas High Schools wasn't on the top 5 schools anymore.









