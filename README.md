# PrepInsta_Internship: Week-1

# Documentation: Bike Buyers Dashboard

## Introduction: 
                The detailed documentation guides the design the process of a Google Sheets dashboard focused on analysing bike buyers's datasets.
                The objective is to provide a deep understanding of purchasing patterns, demographics and effective marketing strategies...

## Dataset Overview: 
The dataset has details of 1000 users from different backgrounds and whether or not they buy a bike. This data can be used to build the dashboard in Google Sheets. There are some NA (Null / Empty) values injected in the dataset.

## Columns -
●	ID 
●	Marital Status 
●	Gender 
●	Income 
●	Children 
●	Education 
●	Occupation 
●	Home Owner 
●	Cars 
●	Commute Distance 
●	Region 
●	Age 
●	Purchased Bike

## ● Source: 
https://docs.google.com/spreadsheets/d/15rtfkctYEUU0VVQdsjE_7ZoIOJVJmcORopNWLe7pRv4/edit#gid=1654503070
## ● Scope:  
To analyse purchasing behaviour, demographics and marketing impacts.

## Data Cleaning and Sorting: Approach

### 1. Data Cleaning

#### a. Handling Missing Values

- *Identify Null Fields:*
  - Use Google Sheets functions like COUNTBLANK or ISBLANK to identify cells with missing values.

- *Evaluate Null Fields Reason:*
  - Understand if null values in the income column are due to data entry errors or genuinely missing information.

- *Handle Income Null Values:*
  - If data entry error, manually correct if possible.
  - If genuinely missing, consider imputation methods (mean, median) based on the nature of the dataset.

#### b. Removing Duplicates

- *Identify Duplicate Rows:*
  - Utilize functions like COUNTIF or conditional formatting to identify and highlight duplicates.

- *Eliminate Duplicate Rows:*
  - Remove duplicate rows while preserving the most relevant data.

### 2. Sorting Fields with Different Values

#### a. Identify Fields for Sorting

- *Understand Data Types:*
  - Identify categorical and numerical fields for sorting.

- *Prioritize Key Fields:*
  - Prioritize fields that contribute significantly to insights, e.g., age, gender, purchase frequency.

#### b. Sort Data

- *Categorical Sorting:*
  - Utilize the 'Sort Range' or 'Data > Sort sheet by column' functionality for categorical fields.

- *Numerical Sorting:*
  - For numerical fields like income, use 'Sort Range' and choose sorting options based on the nature of the analysis (ascending or descending).

### 3. Replace Null Fields in the Income Column

#### a. Imputation Methods

- *Consider Mean/Median:*
  - If the income distribution is relatively normal, replace null values with the mean or median of the income column.

- *Conditional Imputation:*
  - If there's a correlation between income and other variables, consider imputing null values based on these relationships.

#### b. Google Sheets Functions

- *IF or IFERROR:*
  - Use IF or IFERROR functions to conditionally replace null values in the income column.

- *VLOOKUP/MATCH:*
  - If applicable, use VLOOKUP or MATCH functions to retrieve missing income values from related data.

### 4. Document Changes

- *Record Changes:*
  - Create a separate sheet to document data cleaning steps, including changes made, reasons, and any imputation methods applied.

- *Version Control:*
  - Implement version control or timestamps to keep track of iterations and changes made during the cleaning process.

## Dashboard Components:
- To design a dashboard, I took some questions that will help me summarize the tables and charts for analyzing the purchasing behavior, demographics, and marketing impacts.

  # Question: How does the count of bike purchases vary among different marital statuses? Are married individuals more likely to purchase bikes?
   
![Marital Status   Bike Purchased](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/88c09ae9-5b02-494c-915a-dac4ec1bae93)

Conclusion: Yes, married individuals are more likely to purchase the bike as can be seen from the chart.

# Question: Build a bar graph to compare the count of male and female customers. Does gender influence bike purchases, and if so, to what extent?
![Gender   Bike Purchasing](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/33428582-351c-4596-bcf2-caa4013932e6)

Conclusion: Gender doesn't influence bike purchasing much, but as we can see through the chart we can males are likely to purchase more than females.

# Question: What is the distribution of income among bike buyers? Are there specific income brackets that show a higher likelihood of bike purchases?

![Income   Bike Purchased](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/cdfb9a20-79c9-40ce-9e9e-7358b3cd65c7)

	COUNTA of Purchased Bike	Purchased Bike	
	Grouped Income	No	Yes                                
	10000 - 19999	45	29
	20000 - 29999	43	34
	30000 - 39999	81	53
	40000 - 49999	64	89
	50000 - 59999	20	20
	60000 - 69999	84	82
	70000 - 79999	58	65
	80000 - 89999	56	35
	90000 - 99999	14	24
	100000 - 109999	18	11
	110000 - 119999	8	8
	120000 - 129999	8	9
	130000 - 139999	17	15
	150000 - 159999	1	3
	160000 - 170000	2	4

Conclusion: People whose incomes are in the range of 40-50k show a higher likelihood of purchasing a bike.

# Question: Create a histogram to understand the age distribution of bike buyers. Are certain age groups more inclined to purchase bikes?

![Age   Bike Purchasing](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/a2a1b8f3-b968-4f9e-a37d-608ac39fae62)

Conclusion: People who belong to the age group of 35 to 54 are more inclined to purchase a bike.

# Identify outliers in the income distribution of bike buyers. Are there any extreme income values, and how might they impact purchasing behavior?

![image](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/11e4f565-e8c8-47ba-a822-38c8a5fd8862)

		DIFFERENCES
MIN	10000	10000
Q1	47500	37500
MEDIAN	85000	37500
Q3	122500	37500
MAX	170000	47500

# Question: Represent the distribution of bike purchases by region using a pie chart. Are there regions where bike purchases are notably higher?

![Regions](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/c0d66b4b-4278-44db-b839-f23a77f0062b)

Conclusion: As per the chart, the North America region has a higher bike purchasing distribution than others.

# Question: Create a scatter plot to investigate the relationship between income and age. Do individuals with higher incomes tend to be in specific age groups?

![Age Vs Income](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/e57bbe21-07f1-4ef7-ae8e-25947187fd35)

Conclusion: As per the chart, we can observe the age group of 35-54 has higher income than others.


# Question: How does the distribution of bike purchases differ when considering both marital status and gender simultaneously? Are there notable patterns?

![Martial Status Vs Gender](https://github.com/Skyshalini/PrepInsta_Internship/assets/98145111/54a460aa-1bad-47e6-b0c1-08c53c5965be)

Conclusion: As per the chart, we can observe Single Females and Married Men are more likely to purchase a bike.


