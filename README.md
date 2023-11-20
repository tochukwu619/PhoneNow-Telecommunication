# PhoneNow-Telecommunication

---
### TABLE OF CONTENT
1. [PROJECT OVERVIEW](#project-overview)
2. [DATA SOURCE](#data-source)
3. [TOOLS](#tools)
4. [DATA PREPARATION](#data-preparation)
5. [EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)
6. [DATA ANALYSIS](#data-analysis)
7. [RESULTS](#results)
8. [RECOMMENDATION](#recommendation)
9. [LIMITATION](#limitation)
10. [REFERENCE](#reference)
---

### PROJECT OVERVIEW

The project is on the analysis of data gotten from a Telecommunication. Some of their customers churned after the end of their contract. The analysis is to understand the churning of customers in the last one month.
![Telecommunication Dashboard](https://github.com/tochukwu619/PhoneNow-Telecommunication/assets/125865918/0c4c3491-27e6-4572-98f2-bb745bb9975f)

### DATA SOURCE

The dataset used for this project is labelled as ’02 Churn-Dataset.xlsx’.

### TOOLS

-	Microsoft Excel
-	Microsoft power BI

### DATA PREPARATION

Using Microsoft Excel, the data was cleaned by ensuring that there were no duplicates. Spelling checks were also performed on the fields for consistency. Blank-value check was done to ensure that there was no inappropriate blank cell.

### EXPLORATORY DATA ANALYSIS

The following were the KPIs asked during this project:
•	Total number of customers
•	Number of customers that churned
•	Number of customers signed up for each service
•	Customers account information
•	Customers demographic information

### DATA ANALYSIS

Using Microsoft Power BI, measures were developed for the analysis. The total number of customers was gotten as a measure using:
```
Total Customers = COUNTA('01 Churn-Dataset'[customerID]) 
```

The total number present after some customers churned is calculated as a measure using:
```
Total Present = CALCULATE(COUNTROWS('01 Churn-Dataset'),'01 Churn-Dataset'[Churn]="No")
```

The percentage of customers present is calculated as:
```
Present = DIVIDE([Total Present], [Total Customers])
```

The number of senior citizens is calculated as:
```
Senior = CALCULATE(COUNTROWS('01 Churn-Dataset'), '01 Churn-Dataset'[SeniorCitizen]=1) 
```

The number of young citizens is calculated as:
```
Young = CALCULATE(COUNTROWS('01 Churn-Dataset'), '01 Churn-Dataset'[SeniorCitizen]=0) 
```

The number of customers that signed up for phone services is calculated as:
```
Phone Service = CALCULATE(COUNTROWS('01 Churn-Dataset'), '01 Churn-Dataset'[PhoneService]="Yes")
```

The number of customers that signed up for internet service is calculated as:
```
Internet = CALCULATE(COUNTROWS('01 Churn-Dataset'), '01 Churn-Dataset'[InternetService] <> "No")
```

The number of customers that signed up for multiple line service is calculated as:
```
Multiple Lines = CALCULATE(COUNTROWS('01 Churn-Dataset'), '01 Churn-Dataset'[MultipleLines]="Yes") 
```
 

### RESULTS

It was observed that:
-	Total number of customers in the dataset is 7043.
-	The number of customers that churned is 1869.
-	The number of people that signed up for phone service is 6361, internet is 5517 and multiple line is 2971.
-	The number of males is 3555, female is 3488, senior male is 574, senior female is 568, young male is 2981 and young female is 2920.
-	The customers’ account information is as below:
  
![Account Info](https://github.com/tochukwu619/PhoneNow-Telecommunication/assets/125865918/d824ee3e-394b-421a-aa45-4d38a8f94741)


### RECOMMENDATION

The trend needs to be studied over time to understand why the customers churned.

### LIMITATION

More data over different time needs to be studied to deeply understand the trend.

### REFERENCE

[Forage](www.theforage.com)


