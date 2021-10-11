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
* Replaced -1 (Which seems like a bug when the data was inputted or probably human error) with NaN 
* Dropped Competitors and Easy Apply 
* Removed rows with null values

# Feature Engineering
After cleaning the data, I made the following changes and created the following variables:
* Parsed the seniority out of the Job Title 
* Calculated the average salary based on the Salary Estimate 
* Parsed rating out of company text
* Made a new column for company state
* Added a column for if the job was at the company’s headquarters
* Transformed founded date into age of company
* Made columns for if different skills were listed in the job description:
  * Python
  * Tableau
  * Excel
  * SQL
  * Spark
  * Power BI

# Exploratory Data Analysis
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from my analysis.

![salary_state](https://user-images.githubusercontent.com/60106788/136734584-363f1586-d42b-401a-a209-5b4777d6d23b.PNG)
![Jobs_loc_states](https://user-images.githubusercontent.com/60106788/136734186-be18259b-958c-48b6-ab4e-8bec6f683f86.png)
![rating_sector](https://user-images.githubusercontent.com/60106788/136734436-31550a69-88b7-42fa-b402-b69c52e7734b.PNG)
![revenue_age](https://user-images.githubusercontent.com/60106788/136734435-ca288452-fde0-4e99-af05-f2d951bf5b1f.PNG)
![tools](https://user-images.githubusercontent.com/60106788/136734586-cb298892-2a77-41de-8cce-66ee4594431f.PNG)

