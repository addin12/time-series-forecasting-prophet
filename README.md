# Time Series Forecasting for Sales Projection using Retail Store Data

## Why Projecting Sales ?
- Projecting includes as an important business activity for evaluating the expected performance of alternative business plans, especially in order to predict sales, margin or market shares.
- By knowing the near future estimated value of sales based on the value we define, we could determine the best action of maintaining the outcome of our sales performance.

## Project Overview

### Background
>Client wants to know how their retail store sales performance in the future. Is it match their expectation ?

### Objectives
>Determine their sales projection for next 3 months.
 
### Scope
> - Metrics used on this project : Sales, Member, Quantity, and COGS
> - Customers who buys products in BEVERAGES department
> - Data Period : 01 May 2018 - 26 November 2022 (Approximately 5 Years).

## Project Workflow
There are some steps that needs to build forecasting model :

![image](https://user-images.githubusercontent.com/25638454/233004428-b4cd348c-38ac-4f2c-8cf4-6aeb2fc52976.png)

### 1. Collecting Data
Summarize our retail data for 5 years into one dataset (Data Period : 1 May 2018 - 26 Nov 2022)

![image](https://user-images.githubusercontent.com/25638454/233005034-a20235d5-b91f-46f3-b697-79055bbf76a5.png)

### 2. Exploratory Data Analysis
Check their daily sales performance for past 5 years
> Overall Performance for past 5 years

![image](https://user-images.githubusercontent.com/25638454/233005723-c93ca7bd-17cd-4161-bb5e-400bd87a2603.png)

> Beverages Department Daily Sales Performance

![image](https://user-images.githubusercontent.com/25638454/233021623-d8a42cd4-3510-4278-9202-c0e53c96143d.png)

### 3. Data Preprocessing
On this project, i did some data preprocessing before modelling.
- Data Selection, Remove unnecessary features and group data by determined departement.

![image](https://user-images.githubusercontent.com/25638454/233008846-978353a7-09ef-4457-80e9-8863b841892a.png)

- Data Checking, Make sure the data type is well suited by the tools and methods that we used.
>1. Check Data Type

![image](https://user-images.githubusercontent.com/25638454/233011414-b65a55cb-afcb-4199-a4c5-a969cf5124d0.png)

>2. Check Chronological Order and Equidistant Timestamp

![image](https://user-images.githubusercontent.com/25638454/233011763-1ea6e967-0479-443e-ba9d-3b69852572b7.png)

- Handling Outliers, Replace outliers with another values
>1. Dropping down outliers values for each feature

![image](https://user-images.githubusercontent.com/25638454/233013196-b0ef0017-1dd1-4ef2-8a3a-fcf93153f397.png)

>2. Fill replacement with various values from zero, mean, median, and interpolate

![image](https://user-images.githubusercontent.com/25638454/233013020-f2461569-ac74-4388-ac07-f47a9ee5414f.png)

>3. Features after being replaced with interpolate values

![image](https://user-images.githubusercontent.com/25638454/233013314-9e335163-b131-44d7-b6e4-eb5965affc19.png)

- Splitting Data, Divide data into training and test data

![image](https://user-images.githubusercontent.com/25638454/233015369-382c68cd-634d-4caa-8701-963ddaa1f24f.png)

### 4. Modelling
On this repo, i'm only explain how i modelling time-series forecasting using Prophet by Facebook Meta. i'm also using LSTM model for comparison but for the details it should be explained in another repository.

![image](https://user-images.githubusercontent.com/25638454/233016387-b10b1b3c-9666-43e6-8f9d-6a517497134b.png)

What i did to improve my model is to add Holiday Effect and Parameter Tuning to find the best results.
- Holiday Dataframe
- Parameter Tuning

![image](https://user-images.githubusercontent.com/25638454/233017223-381a5f83-b503-4556-9525-3085c2425dee.png)
![image](https://user-images.githubusercontent.com/25638454/233017490-6a831fdf-d434-4c95-afb3-4a7f389e4f82.png)

### 5. Evaluate Model
Based on our modelling methods, now we evaluate the result of our model using our test data

![image](https://user-images.githubusercontent.com/25638454/233018148-815c760c-cddb-4461-8194-a9a9bb873663.png)

Based on Evaluation Result, with metrics :
> - RMSE : 260 Jt
> - MAE : 386 Jt
> - MAPE : 8.72 %

### 6. Result
And now we can forecast our sales projection for the next 3 months

![image](https://user-images.githubusercontent.com/25638454/233018274-5df5cecb-0d64-4b07-865e-da9aae4f4a7b.png)

On business-wise, i hope this project can be implemented into their company.

![image](https://user-images.githubusercontent.com/25638454/233020263-6bed3ad0-ac73-442f-9cb7-8a04317d4db5.png)

### THANK YOU
