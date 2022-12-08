# Contracts Dashboard Code
SQL code for my contracts dashboard

## Introduction
**The Situation**

The Contracts team currently uses a Sharepoint List to track contracts in the pipeline. These contracts have various statuses, dollar amounts, requestors, properties, vendors, and dates. Your supervisor would like to see useful metrics that could help her make decisions in improving the team's performance and efficiency. 

**The Objective**

You are tasked with creating a dashboard in Power BI that will provide insight into the historical and current performance of the team. You will need to display important metrics such as days in processing, YoY performance and the number of contracts processed each year, and the amount of requests submitted by every requestor. 

**Important Note**

This dashboard was originally created by connecting directly to the Sharepoint List. However, for the sake of confidentiality and simplicity, I've recreated this dashboard and its sources in SQL. I've populated an SQL table with sample data, and used that data to create an almost identical dashboard in Power BI. 

## The Code and Source
```sql
CREATE TABLE Residential (
Status varchar(20),
ID int,
Property varchar(200),
Requestor varchar(200),
Date date,
CA varchar(20),
Scope varchar(200),
UrgentRequest varchar(20),
DateExecutedContractEmailed date,
DollarAmount int,
)

INSERT INTO Residential
VALUES ('COMPLETE', 2, 'Baldwin Park', 'Charlie Cox', '2020-1-5', 'Jimmy John', 'Bathroom Sink Repairs', 'Yes', '2020-1-20', 4000), 
('COMPLETE', 1, 'Arcadia', 'Bob Bill', '2020-1-1', 'Jimmy John', 'Replace Lights', 'Yes', '2020-1-14', 5000),
('COMPLETE', 3, 'Temple City', 'Danny Dan', '2020-1-10', 'George Gar', 'Door Replacement', 'No', '2020-1-21', 2000),
('RECEIVED', 4, 'Monrovia', 'Edward Eddy', '2020-3-11', 'George Gar', 'Kitchen Sink Repairs', 'No', '2020-3-21', 5000),
('IN PROGRESS', 5, 'Monrovia', 'Edward Eddy', '2020-3-12', 'Yolanda Yee', 'Tree Trimming', 'No', '2020-3-22', 5000),
('CANCELLED', 6, 'El Monte', 'Fred Fair', '2020-2-12', 'Yolanda Yee', 'New Carts', 'No', '2020-2-20', 5000),
('PRE-APPROVAL', 7, 'Arcadia', 'Bob Bill', '2020-2-1', 'George Gar', 'CO Detectors', 'Yes', '2020-2-12', 1000)
```

<img width="1000" img height="200" alt="image" src="https://user-images.githubusercontent.com/120063554/206329438-31f8ff94-df0c-43a8-96dd-58e164e908b6.png">
