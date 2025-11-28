Power BI Mini Project: DAX Measures Practice


This is a mini project in Power BI demonstrating the use of various DAX functions to perform calculations on a sample dataset. The dataset contains dates, month names, and other sample fields to illustrate aggregation, filtering, and computation techniques.

Features / Measures Included
Aggregation Functions

Average Fun: Calculates the average of MonthNum.

AverageX Fuc: Calculates the average of MonthNum for filtered months (November and December).

Count Fuc: Counts all Month Short Name values.

COUNTX Fuc: Counts MonthNum for filtered months (January and December).

MAX Fun / MaxX Fuc: Calculates the maximum value of Length of characters with and without filters.

MIN Fun / MINX Fun: Calculates the minimum value of Length of characters with and without filters.

Product Fun / ProductX Fun: Calculates the product of MonthNum values with and without filters.

Sum Fun / SUMX Fun: Calculates the sum of Length of characters with and without filters.

Key Concepts Demonstrated

DAX Functions: AVERAGE, AVERAGEX, COUNT, COUNTX, MAX, MAXX, MIN, MINX, PRODUCT, PRODUCTX, SUM, SUMX.

Filtering in DAX: Using FILTER and logical conditions (OR) to calculate measures for specific months.

Iterators vs Scalar Functions: Understanding the difference between functions that iterate over a table (X functions) and those that operate on a column directly.


DAX Measures Included
Average Functions

Average Fun: AVERAGE('Dataset'[MonthNum])

AverageX Fuc: AVERAGEX(FILTER('Dataset', OR('Dataset'[Month Short Name] = "NOV", 'Dataset'[Month Short Name] = "DEC")), 'Dataset'[MonthNum])

Count Functions

Count Fuc: COUNT('Dataset'[Month Short Name])

COUNTX Fuc: COUNTX(FILTER('Dataset', OR('Dataset'[Month Short Name] = "JAN", 'Dataset'[Month Short Name] = "DEC")), 'Dataset'[MonthNum])

Maximum Functions

MAX Fun: MAX('Dataset'[Length of characters])

MaxX Fuc: MAXX(FILTER('Dataset', OR('Dataset'[Month Short Name] = "JAN", 'Dataset'[Month Short Name] = "DEC")), 'Dataset'[Length of characters])

Minimum Functions

MIN Fun: MIN('Dataset'[Length of characters])

MINX Fun: MINX(FILTER('Dataset', 'Dataset'[Month Short Name] = "DEC"), 'Dataset'[Length of characters])

Product Functions

Product Fun: PRODUCT('Dataset'[MonthNum])

ProductX Fun: PRODUCTX(FILTER('Dataset', 'Dataset'[Month Short Name] = "JAN"), 'Dataset'[MonthNum])

Sum Functions

Sum Fun: SUM('Dataset'[Length of characters])

SUMX Fun: SUMX(FILTER('Dataset', 'Dataset'[Month Short Name] = "DEC"), 'Dataset'[Length of characters])
