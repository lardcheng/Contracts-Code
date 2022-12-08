# Contracts Dashboard Code
SQL code for my contracts dashboard

## Introduction
**The Situation**

The Contracts team currently uses a Sharepoint List to track contracts in the pipeline. These contracts have various statuses, dollar amounts, requestors, properties, vendors, and dates. Your supervisor would like to see useful metrics that could help her make decisions in improving the team's performance and efficiency. 

**The Objective**

You are tasked with creating a dashboard in Power BI that will provide insight into the historical and current performance of the team. You will need to display important metrics such as days in processing, YoY performance and the number of contracts processed each year, and the amount of requests submitted by every requestor. 

**Important Note**

This dashboard was originally created by connecting directly to the Sharepoint List. However, for the sake of confidentiality and simplicity, I've recreated this dashboard and its sources in SQL. I've populated an SQL table with sample data, and used that data to create an almost identical dashboard in Power BI. This version is extremely simplified, and admittedly, does not look as polished as the actual dashboard. 

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
VALUES ('COMPLETE', 1, 'Baldwin Park', 'Charlie Cox', '2020-1-5', 'Jimmy John', 'Bathroom Sink Repairs', 'Yes', '2020-1-20', 4000, 'A Company'), 
('COMPLETE', 2, 'Arcadia', 'Bob Bill', '2020-1-1', 'Jimmy John', 'Replace Lights', 'Yes', '2020-1-14', 5000, 'C Company'),
('COMPLETE', 3, 'Temple City', 'Danny Dan', '2020-1-10', 'George Gar', 'Door Replacement', 'No', '2020-1-21', 2000, 'B Company'),
('RECEIVED', 4, 'Monrovia', 'Edward Eddy', '2022-3-11', 'George Gar', 'Kitchen Sink Repairs', 'No', NULL, 5000, 'A Company'),
('IN PROGRESS', 5, 'Monrovia', 'Edward Eddy', '2022-3-12', 'Yolanda Yee', 'Tree Trimming', 'No', NULL, 5000, 'C Company'),
('CANCELLED', 6, 'El Monte', 'Fred Fair', '2020-2-12', 'Yolanda Yee', 'New Carts', 'No', NULL, 5000, 'B Company'),
('PRE-APPROVAL', 7, 'Arcadia', 'Bob Bill', '2022-2-1', 'George Gar', 'CO Detectors', 'Yes', NULL, 1000, 'A Company'),
('COMPLETE', 8, 'Baldwin Park', 'Charlie Cox', '2019-5-6', 'Jimmy John', 'HVAC Repairs', 'No', '2019-5-14', 2000, 'D Company'),
('COMPLETE', 9, 'Temple City', 'Danny Dan', '2019-10-20', 'Yolanda Yee', 'Hot Water Heaters', 'No', '2019-10-30', 2000, 'E Company'),
('COMPLETE', 10, 'Arcadia', 'Bob Bill', '2021-8-11', 'Yolanda Yee', 'Sidewalk Repairs', 'Yes', '2021-8-22', 3000, 'Z Company')
```

<img width="1000" img height="200" alt="image" src="https://user-images.githubusercontent.com/120063554/206403007-5fc58308-332c-4975-97cf-85fb517ba6cb.png">
