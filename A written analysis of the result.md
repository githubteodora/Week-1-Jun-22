# An Analysis of Kickstarter Campaigns

## Overview of Project
- This project aims to reveal how different kickstarter campaigns fared in relation to their launch dates and their funding goals. The focus is on the "theater" parent category and "plays" subcategory of campaigns (1393 records).
- The "plays" subcategory alone includes more than 1k records. The projects took place globally between 2009 and 2017.

### Purpose
The purpose of the project is to demonstrate how standard excel functions, combined with simple line charts, can help reveal insights. By defining the methodology, challenges and describing the outcomes, the authors hopes to inspire readers to ask further questions and continue exploting the data.  

## Analysis and Challenges
The methodology for the analysis follows the below steps:
1. Convert the fundraisers' created dates to a readable format.
2. Find out which year and month a project was created in.
3. Analyze the outcomes based on launch dates.
4. Analyze the outcomes based on the goals (any currency). 

### Analysis of Outcomes Based on Launch Date 
- The analysis of outcomes based on launch dates required the creation of a pivot table where campaign start months are used as rows, the outcomes represenyt columns columns and the count of unique campaigns per outcome are added as values per row. Live campaigns are filtered out. The pivot table's filter was set to invluce only the "theater" parent category. No filtering on the year of the campaign was applied at this stage.
---
![Pivot table structure](https://github.com/githubteodora/Week-1-Jun-22/blob/main/Pivot%20months.PNG)
---
- Once the necessary pivot table was set up, a line chart was generated to uncover trends.
---
![Line chart](https://github.com/githubteodora/Week-1-Jun-22/blob/main/Theater_Outcomes_vs_Launch.png)
---
### Analysis of Outcomes Based on Goals
- The analysis of the outcomes based on goals required the creation of groups of campaigns depending on their goals, as well as the usage of the "COUNTIFS" excel function to aggregrate the campaigns data based on several conditions. Here is an example of a COUNTIFS function that was used to retrieve the count of campaigns with subcategory equal to "plays", that were successful and had a goals less than 1000 USD: "=COUNTIFS(source!$D:$D, "<1000", source!$F:$F, "successful", source!$R:$R, "plays")"
- The same formula structure was used to populate the number of successful, failed and cancelled campaigns per each defined range of campaign goals. 
- Next, additional columns that calculate the percentage successful, failed and cancelled campaigns per goal range were created to achieve the following table view:
---
![Goal ranges](https://github.com/githubteodora/Week-1-Jun-22/blob/main/Goal_ranges.PNG)
---
- The final step of the analysis was to generate a line graph and represents percenrage failed, successful and cancelled campaigns per goal range (image below).
---
![Outcomes vs Goals](https://github.com/githubteodora/Week-1-Jun-22/blob/main/Outcomes_vs_Goals.png)
---
### Challenges and Difficulties Encountered
A few challenges had to be overcome in order to complete the analysis.
1. Converting epoch timestamps to human-readable dates. The following excel formula was used to achieve this "=(((J2/60)/60)/24)+DATE(1970,1,1)"; further reference is available via ![this link](https://www.epochconverter.com/). 
2. Extracting the month name from a data field required some research, too. The standard "MONTH()" formula ins excel returns the month as a numeric value. However, the requirement for the analysis needed the full names of the months. The following formula was used to retrieve the month names as text strings "=TEXT(S2, "mmmm")".

## Results

1. The two main conclusions that can be drawn about the Outcomes based on Launch Date, are:
   - The 2nd quarter of the year is a popular time for launching theater-related campaigns.
   - Campaigns that start in December are few as compared to other months, and often fail.

2. Some of the conclusions that can be drawn about the Outcomes based on Goals, are:
   - The higher the goal of a campaign, the more likely it is that it fails to achieve its funding goal.
   - Campaigns with goal that is less than 5000 USD are most likely to reach their funding goal. 

3. Some limitations of the dataset include:
   - Informartion about how much time if took for a successful campaign to reach its goal might be useful to have an add as a layer onto the analysis.
   - When working with goal ranges, local currencies might skew the data. A local currency to USD concersion rate is needed, so that all goals can be measured in USD.

4. Some other possible tables and/or graphs that can be created:
   - A line graph that analyzes the outcomes based on launch dates, but this time aggregating the data per quarter and year; 
   - A pivot table that uses the parent categories as rows and the count of campaigns as values;
   - A table that reveals what is the total sum of successfully raised funds per year, with the ability to drill down to parent category and subcategory levels;

---
END
