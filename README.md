# INCUBATOR HUB CAPSTONE PROJECT FOR CUSTOMER DATA ANALYSIS
This is where I documented my final project with Ladies in Tech Africa (LITA)

## ANALYSIS OF CAPSTONE CUSTOMER DATA

## PROJECT OVERVIEW

To determine the subscription trend in the four regions of Nigeria.
## DATA SOURCES
- [Microsoft Excel](Download Here)

- Incubator Hub Customer Data

- Capstone Project Customer Data

## DATA CLEANING AND PREPARATION

- Microsoft Excel

   1. Data cleaning

   2. For Data Analysis

   3. For visualization

- SQL Structured Query Language...For Querying Data

- Git Hub for Portfolio Building

- Power BI...for building visualizations based on data received.

## DATA ANALYSIS

The variables used are

- Customer ID

- Customer Name

- Region

- Subscription Type

- Subscription Start

- Subscription End

- Cancelled

- Revenue

- Subscription Duration

##### The following Analysis were carried out on excel

- Subscription Duration
```
= F2- E2
```
- Total Revenue
```
= Sum (H2:H33788)
```
- Average Revenue
```
= Average (H2:H33788)
```
- Total Revenue per Revenue Region
```
= Sumif (C2:C33788,"North",H2:H33788)
```
-  Average Revene per Revenue
```
= Sumif (C2:C33788,"North", H2:H33788)
```
![customer data pivot 1](https://github.com/user-attachments/assets/313010ee-8ab6-4f7a-979f-5e11326d8836)
![customer data pivot 2](https://github.com/user-attachments/assets/309094b6-0766-463e-9422-504c86427e82)
![customer data pivot 3](https://github.com/user-attachments/assets/38decd76-71d6-4463-b87c-2dde18d34e5c)
![customer data pivot 4](https://github.com/user-attachments/assets/b5014431-dc73-4e15-981e-dfe63864c5c6)
![customer data pivot 5](https://github.com/user-attachments/assets/d3dc43ee-b00e-4897-8dfc-dc74ec82d13f)

## ANALYSIS ON SQL
- Retrieve the total number of customers from each Region
```
SELECT Region, COUNT(CustomerID) AS Total_No_of_Customers
FROM [dbo].[CUSTOMER_DATA_CSV01]
GROUP BY Region
```
- Find customers with subscriptions longer than 12 months
```
SELECT CustomerName,SubscriptionType,SubscriptionStart,SubscriptionEnd
FROM [dbo].[CUSTOMER_DATA_CSV01]
WHERE DATEDIFF(MONTH,SubscriptionStart,SubscriptionEnd) >=12
```
- Find the total number of active and cancelled subscription
```
SELECT SUM(CASE WHEN Canceled = 0 THEN 1 ELSE 0  END) AS ActiveSubscriptions,
SUM (CASE WHEN Canceled = 1 THEN 1 ELSE 0 END) AS CanceledSubscriptions
FROM [dbo].[CUSTOMER_DATA_CSV01]
GROUP BY CANCELED
```
## ANALYSIS ON POWER BI

- Below are the visuals obtained from the Power BI
 
![Screenshot 2024-11-06 032803 customer data power bi 1](https://github.com/user-attachments/assets/a4138100-d5e0-4376-9efb-e343834ed567)
![Screenshot 2024-11-06 032910 power bi customer data 2](https://github.com/user-attachments/assets/cbc93395-8a4f-4e53-8c74-32e738a2ea69)

  


