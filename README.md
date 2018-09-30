#Data Science, HW2
###Instructions

####Context
This assignment reinforces ideas in Data Wrangling I.

####Due date
Due: October 4 at 5:00pm.

####Points
Problem 0: 10 points  
Problem 1: 30 points  
Problem 2: 30 points  
Problem 3: 30 points  

####Problem 0  
This “problem” focuses on structure of your submission, especially the use git and GitHub for reproducibility, R Projects to organize your work, R Markdown to write reproducible reports, relative paths to load data from local files, and reasonable naming structures for your files.

To that end:

create a public GitHub repo + local R Project; we suggest naming this repo / directory p8105_hw2_YOURUNI (e.g.  p8105_hw2_ajg2202 for Jeff), but that’s not required
create a single .Rmd file named p8105_hw2_YOURUNI.Rmd that renders to github_document
create a subdirectory to store the local data files used in Problems 1 and 2, and use relative paths to access these data files
Your solutions to Problems 1, 2, and 3 should be implemented in your .Rmd file, and your git commit history should reflect the process you used to solve these Problems.

For this Problem, we will assess adherence to the instructions above regarding repo structure, git commit history, and whether we are able to knit your .Rmd to ensure that your work is reproducible. Adherence to appropriate styling and clarity of code will be assessed in Problems 1+.

####Problem 1  
This problem focuses on NYC Transit data; in particular, this CSV file contains information related to each entrance and exit for each subway station in NYC.

Read and clean the data; retain line, station, name, station latitude / longitude, routes served, entry, vending, entrance type, and ADA compliance. Convert the entry variable from character (YES vs NO) to a logical variable (the ifelse or recode function may be useful).

Write a short paragraph about this dataset – explain briefly what variables the dataset contains, describe your data cleaning steps so far, and give the dimension (rows x columns) of the resulting dataset. Are these data tidy?  

Answer the following questions using these data:  

How many distinct stations are there? Note that stations are identified both by name and by line (e.g. 125th St A/B/C/D; 125st 1; 125st 4/5); the distinct function may be useful here.  

How many stations are ADA compliant?
What proportion of station entrances / exits without vending allow entrance?
Reformat data so that route number and route name are distinct variables. How many distinct stations serve the A train? Of the stations that serve the A train, how many are ADA compliant?

####Problem 2  
This problem uses the Mr. Trash Wheel dataset, available as an Excel file on the course website. Please use the  HealthyHarborWaterWheelTotals2017-9-26.xlsx version.

Read and clean the Mr. Trash Wheel sheet:  

specify the sheet in the Excel file and to omit columns containing notes (using the range argument and cell_cols() function)
use reasonable variable names
omit rows that do not include dumpster-specific data
rounds the number of sports balls to the nearest integer and converts the result to an integer variable (using as.integer)
Read and clean precipitation data for 2016 and 2017. For each, omit rows without precipitation data and add a variable year. Next, combine datasets and convert month to a character variable (the variable month.name is built into R and should be useful).  

Write a paragraph about these data; you are encouraged to use inline R. Be sure to note the number of observations in both resulting datasets, and give examples of key variables. For available data, what was the total precipitation in 2017? What was the median number of sports balls in a dumpster in 2016?

####Problem 3  
This problem uses the BRFSS data. DO NOT include this dataset in your local data directory; instead, load the data from the  p8105.datasets package.  

For this question:  

format the data to use appropriate variable names;
focus on the “Overall Health” topic
exclude variables for class, topic, question, sample size, and everything from lower confidence limit to GeoLocation
structure data so that values for Response (“Excellent” to “Poor”) are column names / variables which indicate the proportion of subjects with each response (which are values of Data_value in the original dataset)
create a new variable showing the proportion of responses that were “Excellent” or “Very Good”
Using this dataset, do or answer the following:

How many unique locations are included in the dataset? Is every state represented? What state is observed the most?
In 2002, what is the median of the “Excellent” response value?
Make a histogram of “Excellent” response values in the year 2002.
Make a scatterplot showing the proportion of “Excellent” response values in New York County and Queens County (both in NY State) in each year from 2002 to 2010.