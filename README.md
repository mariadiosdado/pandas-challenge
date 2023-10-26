# pandas-challenge
In this assignment, you’ll create and manipulate Pandas DataFrames to analyze school and standardized test data.

## Background
You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

## Before You Begin
  1. Create a new repository for this project called pandas-challenge. Do not add this homework to an existing repository.
  
  2. Clone the new repository to your computer.
  
  3. Inside your local Git repository, create a folder for this homework assignment and name it PyCitySchools.
  
  4. Add your Jupyter notebook to this folder. This will be the main script to run for analysis.
  
  5. Push these changes to GitHub or GitLab.

## Files
Download the following files to help you get started:

[Module 4 Challenge files](https://static.bc-edx.com/data/dl-1-2/m4/lms/starter/Starter_Code.zip)

## Instructions
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

**Hint:** Check out the sample solution called PyCitySchools_starter.ipynb located in the .zip file to review the desired format for this assignment.

### District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:

  * Total number of unique schools
  
  * Total students
  
  * Total budget
  
  * Average math score
  
  * Average reading score
  
  * % passing math (the percentage of students who passed math)
  
  * % passing reading (the percentage of students who passed reading)
  
  * % overall passing (the percentage of students who passed math AND reading)

### School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:

  * School name
  
  * School type
  
  * Total students
  
  * Total school budget
  
  * Per student budget
  
  * Average math score
  
  * Average reading score
  
  * % passing math (the percentage of students who passed math)
  
  * % passing reading (the percentage of students who passed reading)
  
  * % overall passing (the percentage of students who passed math AND reading)

### Highest-Performing Schools (by % Overall Passing)
Sort the schools by `% Overall Passing` in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools".

### Lowest-Performing Schools (by % Overall Passing)
Sort the schools by `% Overall Passing` in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools".

### Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.
<img width="337" alt="image" src="https://github.com/mariadiosdado/pandas-challenge/assets/136658866/135e467e-0d8f-491a-aaca-a7db5d18a84a">

Use `pd.cut` to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.
<img width="646" alt="image" src="https://github.com/mariadiosdado/pandas-challenge/assets/136658866/0797c261-42c8-4bba-b53f-e527b70162b8">

Use the scores above to create a DataFrame called `spending_summary`.

Include the following metrics in the table:

  * Average math score
  
  * Average reading score
  
  * % passing math (the percentage of students who passed math)
  
  * % passing reading (the percentage of students who passed reading)
  
  * % overall passing (the percentage of students who passed math AND reading)

### Scores by School Size
Use the following code to bin the `per_school_summary`.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use `pd.cut` on the "Total Students" column of the `per_school_summary` DataFrame.
Create a DataFrame called `size_summary` that breaks down school performance based on school size (small, medium, or large).

### Scores by School Type
Use the `per_school_summary` DataFrame from the previous step to create a new DataFrame called `type_summary`.
This new DataFrame should show school performance based on the "School Type".

## Credits

For the PyCitySchool_Analysis, I used the starter code provided and the two csv files. I went over the lecture notes. I attended office hours and Joseph the TA helped me correct some errors in my code. One of my class mates also helped calculate the per capital budget because I accidentally deleted that code line and couldn't figure it out anymore. The error was in my per school budget. Google also helped.

## Analysis

In this pandas challanged we used two csv files and then merged them together into one dataset that included school information, student information and scores for both reading and math. Then we summarized district information and displayed the information in a Data Frame called district_summary. It gave us the total number of schools and students in the district, the total budget and average scores as well as percentages. Then we further broke down the information by schools and displayed our findings in another data frame called per_school_summary. This dataframe displayed information for each of the 15 schools in the district. The information included the school type, number of students, budget for the school , budget per student, scores and percentages and overall passing. After we were asked to organize the schools by Overall Passing % from descending order. After, we sorted bottom performing schools by Overall Passing %. Then, we analyzed both reading and math scores by grades (9-12) and displayed the information according to each school. We followed the money, and investigated if school spending has any effects on scores. In trying to determine what affects scores, we organized the school data by size and finally, by school type.

From the data we can conclude that schools in the district and therefore the district as a whole performs better in reading than in math. From the district summary we can see that it has an 85.81% passing rate in reading vs a 74.98 in math. The overall passing is not great by 65.17% (at least 70% would be better in my opinion).

Also, I could not help but notice the discrepancy in performance between charter schools and district schools. All of the top 5 performers are from charter schools with the number one school(Cabrera) achieving an overall passing of 91.33%. In comparison, the bottom performing school, Rodriguez H.S., is a disctrict school with only 52.99% overall passing (hardly more than half of its student population). Money does not seem to affect performance since the bottom-performing schools have student budget the same (if not slightly bigger) than the top-performing schools.


