# Customer Movement Analysis

For each reporting month, customers are grouped into 4 categories defined by the defition below

Status | Current |Previous |Before
------ | ----- |-----|----- |
Repeat | ✅ | ✅ | - |
Reactivated | ✅ | ❌ | ✅ |
New | ✅ | ❌ | ❌ |
Churn | ❌ | ✅ | - |

Current: made purchases this month (M)  
Previous: made purchases last month (M-1)  
Before: made purchase before last month (< M-1)

## Dataset
Supermarket, the same data as used in Customer Segmentation homework.  

## Data Preparation
using the SQL script to prepare the report.
SQL : [Customer Movement Analysis](https://github.com/Nasalinn/BADS7105-CM-Analytics/blob/main/Assignment06%20-%20Customer%20Movement%20Analysis/Customer%20Movement.sql)  

## Result
The visualization can be made right after executing the SQL using Power BI.
![image](https://user-images.githubusercontent.com/95351692/147640102-99882cb7-2d28-48e2-8b40-5b6fab772d1e.png)
