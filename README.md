# Power BI Data Cleaning and Transformation Task Documentation

## Introduction

This documentation outlines the data cleaning and transformation tasks in Power BI Desktop for the Employee, Salary, and Department datasets. These tasks are essential to prepare the data for analysis and reporting. Below are the step-by-step instructions for performing these tasks.

### Step 1: Open Power BI Desktop

1. Launch Power BI Desktop.
![](desktop.png)

### Step 2: Load CSV Files

1. Go to "Home" in the Power BI Desktop.

2. Click on "Get Data" and select "CSV."

3. Load the following CSV files: 
   - Employee.csv
   - Salary.csv
   - Department.csv
![](csv.png)
### Step 3: Transform Data

1. After loading the data, click on "Edit Queries" to open the Power Query Editor in a new window.
![image](transform.png)

### Employee Data Cleaning and Transformation

#### Step 4: Cleaning Employee Table

6. Start by working on the Employee table.

7. Check column names and ensure they are meaningful:
   - Change `empID` to "Employee ID."
   - Change `name` to "Last Name."
   - Change `fname` to "First Name."
   - Change `deptID` to "Department ID."
   - Change `dob` to "Date of Birth."
   - Convert `aadhar`, `city`, `pincode`, `phone`, and `email` to proper case.

8. Examine data types for each column:
   - Change data types to "Text" for `Employee ID`, `Aadhar`, `Pincode`, `Phone`, and `Department ID`.

9. Remove the `Aadhar` column as it is not useful for analysis.

### Salary Data Cleaning and Transformation

#### Step 5: Cleaning Salary Table

10. Move on to the Salary table.

11. Check column names and ensure they are meaningful:
    - Change `empID` to "Employee ID."
    - Change `Base` to "Salary."
    - Change `yearly increament` to "Yearly Increment."

12. Analyze data quality indicators:
    - Note that 50% of the data is empty, and there are a total of 199 rows.

13. Use "Keep Top Rows" to retain the top 100 rows containing data.

14. Change the data type of `Employee ID` to "Text" (if not already).

### Department Data Cleaning and Transformation

#### Step 6: Cleaning Department Table

15. Proceed to the Department table.

16. Check column names and ensure they are meaningful:
    - Change `deptID` to "Department ID."
    - Write `education` in proper case.

17. Analyze data quality indicators:
    - Note that 94% of the data is empty, and there are a total of 199 rows.

18. Keep the top 6% of data that is not empty.

### Merging the Tables

#### Step 7: Merging Employee and Salary Tables

19. To merge the Employee and Salary tables, use the "Merge Queries" function in Power Query Editor.

20. Merge on `Employee ID` as the common column using an outer join.

21. After merging, open the new `Salary` column added, and expand it. Select the columns you want to merge and uncheck "Use original table name as prefix."

#### Step 8: Merging Resultant Table with Department Table

22. To merge the resultant table with the Department table, use the "Merge Queries" function again.

23. Merge on `Department ID` as the common column using an outer join.

24. The merged table is now ready for further analysis and reporting.

### Conclusion

25. Close the Power Query Editor and load the cleaned and transformed data into Power BI Desktop.

26. You can now create visualizations, perform analysis, and build reports based on the cleaned data.

This completes the data cleaning and transformation process in Power BI Desktop for the Employee, Salary, and Department datasets. Ensure that you save your work and update the data as needed for ongoing analysis and reporting tasks.
