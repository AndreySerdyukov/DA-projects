# Client Retention Analysis

This project focuses on analyzing customer retention based on activity in a mobile application. Using key metrics such as the number of logins, transactions, and operations over the past 30 days, we aim to identify and visualize different levels of customer engagement. The analysis categorizes customers into four groups based on their activity status.

## Data Overview

The dataset contains the following key columns:

- **CLIENT_ID**: Unique identifier for the customer.
- **VALUE_DAY**: Reporting date.
- **DIGITAL_30_CNT**: The number of logins to the mobile app in the past 30 days before the reporting date.
- **TRAN_ACTIVE_30_CNT**: The number of transactions (purchases, transfers, etc.) in the mobile app during the last 30 days.
- **OPER_ACTIVE_30_CNT**: The number of operations (including financial and non-financial actions) in the app during the last 30 days.

## Customer Activity Categories

We have defined the following categories based on customer engagement:

- **Active Clients**: Customers who have data entries for the reporting date (i.e., they are present in the dataset).
- **Digitally Active**: Customers who have logged into the mobile application at least once in the last 30 days.
- **Operationally Active**: Customers who have performed at least one operation (financial or non-financial) in the app in the past 30 days.
- **Transactionally Active**: Customers who have made at least one transaction in the mobile application in the last 30 days.

## Analysis and Visualization

This project includes a visual representation of customer retention across these different categories. The data is analyzed and displayed to show the overlap and trends in customer behavior, helping to understand which group of customers are most engaged and which may require additional attention.

### Key Visual Insights

- **Retention Over Time**: A visualization that tracks the retention of customers in each of the defined categories across the reporting period.
- **Engagement Patterns**: A breakdown of customer behavior by activity type, identifying trends in digital logins, operations, and transactions.
- **Customer Segmentation**: An analysis of how many customers belong to each category and the overlap between the groups.

## Conclusions

Based on the analysis, we draw insights into customer retention trends, highlighting areas where engagement is strong and where improvements can be made. The findings will help in making data-driven decisions to enhance customer experience and retention strategies.
