# Data Analyst Salary Estimator: Project Overview
I perform an analysis and prediction on the Data Analyst Jobs dataset which contains more than 1000 job listing for data analyst positions, with features such as Salary Estimate, Job Location, Company Rating, Industry and more.

Link to the dataset: https://www.kaggle.com/andrewmvd/data-analyst-jobs

# Code and Libraries Used
* Python Version: 3.9.5
* Packages: numpy, pandas, matplotlib, seaborn, sklearn

# Features 
* Job Title
* Salary Estimate
* Job Description
* Rating
* Company Name
* Location
* Headquarters
* Size
* Founded
* Type of ownership
* Industry 
* Sector
* Revenue
* Competitors
* Easy Apply

# Data Cleaning
After importing the data, I needed to clean it up by doing the following:
* Replaced the -1 (Which seems like a bug when the data was inputted or probably human error) with NaN 
* Dropped Competitors and Easy Apply 
* Removed rows with null values
then made the following changes and created the following variables:
* Parsed the seniority out of the Job Title 
* Calculated the average salary based on the Salary Estimate 
* Parsed rating out of company text
* Parsed the state code out of location 
* Parsed the headquarters state code out of headquarters 
