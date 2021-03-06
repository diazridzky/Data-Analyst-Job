# Data Analyst Job Research: Project Overview
This project is an analysis on the US data analyst jobs data with the hopes of providing an insight to data analysts when they're looking for a job and also predict the job's salary to help data analysts negotiate their income when they get a job.

Link to the dataset: https://www.kaggle.com/andrewmvd/data-analyst-jobs

# Code and Libraries Used
* Python Version: 3.9.5
* Packages: NumPy, pandas, Matplotlib, seaborn, scikit-learn

# Columns 
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

After cleaning the data, I made the following changes:
* Parsed seniority out of Job Title 
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

![seniority](https://user-images.githubusercontent.com/60106788/140320054-5ee8057f-3015-489e-9680-22a16bd51183.PNG)
![ownership](https://user-images.githubusercontent.com/60106788/141471187-6b28e4c6-6e90-4645-82b3-c5e85cd6ccb9.PNG)
![Jobs_loc_states](https://user-images.githubusercontent.com/60106788/136734186-be18259b-958c-48b6-ab4e-8bec6f683f86.png)
![rating_sector](https://user-images.githubusercontent.com/60106788/136734436-31550a69-88b7-42fa-b402-b69c52e7734b.PNG)
![revenue_age](https://user-images.githubusercontent.com/60106788/136734435-ca288452-fde0-4e99-af05-f2d951bf5b1f.PNG)
![tools](https://user-images.githubusercontent.com/60106788/136734586-cb298892-2a77-41de-8cce-66ee4594431f.PNG)

# Model Building
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%.

I tested three different models (I tried linear regression but then I get an overfit model that's worse for predicting future data, this happened because there are many categorical variables) and evaluated them using MAE, MSE, and RMSE. I picked MAE, MSE, and RMSE because I could compare each metrics for each models. Here are the three models I tried:
* Decision Tree - Just a test to see if it's better than linear regression (I only used cross validation because it doesn't have an estimator)
* Random Forest - Because many trees is better than a single tree (I used GridSearchCV to reach the best model)
* Gradient Boost - I thought that this would be a good fit, since it builds on weak learners (I used GridSearchCV to reach the best model)

# Model Performance
The Gradient Boost model surpassed other algorithms on the test sets.

![eval](https://user-images.githubusercontent.com/60106788/136768877-c923b9af-ecf1-4647-95c7-ababa8917847.PNG)
