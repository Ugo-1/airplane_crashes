# Airplane Crashes from 1908 to 2009

This is a solution to the airplane crashes project of the [Data Analysis in Power BI track]( https://aka.ms/30DLDATLandingPage) of NG 30 Days of Learning.

## Table of contents

- [Overview](#overview)
- [Data Source](#data-source)
- [Data Preparation and Processing](#data-preparation-and-processing)
   - [Python Processing](#python-processing)
   - [Excel Processing](#excel-processing)
   - [Power BI](#power-bi)
-[Findings](#findings)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview
The goal of analyzing this data is to get insights into airplane crashes that occurred between 1908 and 2009

## Data Source
The data used was obtained from this [github repository]( https://github.com/theoyinbooke/30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students).

## Data Preparation and Processing
The data had 13 columns which are:
•	Date
•	Time
•	Location
•	Operator
•	Flight #
•	Route
•	Type
•	Registration
•	cn/In
•	Aboard
•	Fatalities
•	Ground
•	Summary
Of these columns only the date column had non-null values. The data was cleaned using python, excel before modelling with power bi.
### Python Processing
The data was loaded into python and the following was done:
-	A column was created to store the country code for the location of the crash
-	Text clustering was done on the summary column to understand the causes of the crash. 6 clusters were obtained.
-	The null values of the data were replaced with unknown.
-	The data was saved.

### Excel Processing
The data was opened in excel and the following was done:
-	Due to the separation of some countries like USSR, Yugoslavia etc., the api used to obtain the country code from the location returned a lot of unknown. These were manually checked and the current country code of such places replaced the unknown values.

### Power BI
Further cleaning and modelling were done in power bi. 
-	The unknown in the numeric columns were replaced with 0.
-	Year and month columns were also added.
![](./images/model.png)

## Findings
-  Total number of crashes between 1908 and 2009 is 5,236.
-  Compared to the previous year-till-date; the total number of fatality (this includes the ground and fatalities column) and fatality rate increased while the number of crashes decreased.
-	1972 is the year with the highest number of crashes (104). 
-	The 9/11 attack is the only one that resulted in more ground casualties.
-	Most crashes occur in December, closely followed by January and August.

## Recommendations
1.	Weather forecast should be properly done before flights take off.
2.	Airline operators should make necessary checks to ensure the plane is in good shape so as to prevent crashes due to engine failure.

## Limitations
The summary column which contains a description about the crash didn’t contain uniform data. Some had more descriptions, others little or nothing.

## Dashboard
Two dashboards were created using the 5W approach; a static and interactive one. Both are in the images folder

## Author

- Ugochukwu
- Twitter - [@_EightKing](https://www.twitter.com/_EightKing)

