## Health Data Cleaning Sheet
This project involved the cleaning of an  healthcare dataset to ensure accuracy and consistency of the dataset. The datset contained patient records, medical test results, and other healthcare-related information. The cleaning process addressed missing values, duplicate records, incorrect data format and other forms of inconsistencies to ensure data quality and reliability.

## Steps Followed:
Step 1: To clean the Contact Information  
- select the contact information column
- Go to the split column by delimeter
- Select or enter the delimeter, click on custom and select "comma", which in this case, is the delimeter. OK
-  Rename the columns - Contact info and Email Address

step 2: To clean the age column
- Select the age column, go to replace values, enter "null" as"  as value to find" then "0" as "value to replace with".
- Go to Data Type (still in the home tab) and change from decimal number to whole number

Step 3: Height column of which the values are of two different units - the centimeter (cm) and meter (m), although meter is not outrightly stated. 
- Converting from meters(m) to centimeteter(cm) requires a multiplication by 100, and this can be achieved by:

- Selecting the height column. Seperate the values from the unit(cm)
- Go to split column by delimeter, select or enter delimeter, click on custom and select "space" which in this case is the delimeter. OK
- Rename the  columns as - Height and unit
- Select the Height column, go to Add Column, then Custom Column 
- In the formula box, type = if [unit]=" the [height] else [height] * 100 enter OK
- Drag the custom column to the Height Column.
- Select the unit column and fill down.
- Select both the Custom and Unit Columns, go to Merge Columns , use "space" as seperator. OK
- Delete the Height Column (select, right click and remove) then rename the merged column - Height 

step 4: To clean the Weight Column, apply all the steps taken in cleaning the height column. The conversion here is from kg to lbs

- Select the Weight column, go to Add Column , Custom column, the enter the formula
- In the formula box, type = if [unit]=" the [weight] else [weight] * 0.453592 enter OK

step 5: To clean the blood pressure column, select the column, replace the dash - with forward slash /

step 6: To clean the cholesterol level column,apply same steps used in cleaning the height and weight column.

- Use the custom column formula = if [unit]=" the [Cholesterol Level] else [Cholesterol Level ]/38.67 enter OK 
step 6: To clean the Diabetes Column;

- Select the column, replace values, enter "Diabetes" as value to find , replace with "Yes"
- Replace Values, enter "1" as value to find, replace with "Yes"
- Replace  Values, enter "0" as value to find, replace with "No"
- Replace values, enter "Non -daibetic" as value to find, replace with "No"

step 7: For the date of visit column;

- Replace the dash(-) with forwad slash (/)
- seperate the the year from the day and month
- Merge the three columns together by placing the day column first, the follwed by the month and year respectively
- Rename the column to reflect date of visit

step 8: Snapshot of the uncleaned dataset
![Image](https://github.com/user-attachments/assets/9f8892a9-59f4-4124-b1cb-1c1e1405ef38)

Step 9: Snapshot of the cleaned dataset
![Image](https://github.com/user-attachments/assets/3cf4e894-e487-424b-ad50-b330983b9eb3)





