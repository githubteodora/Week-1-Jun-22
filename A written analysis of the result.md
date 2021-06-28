# An Analysis of Kickstarter Campaigns

## Overview of Project
- This project aims to reveal how different kickstarter campaigns fared in relation to their launch dates and their funding goals. The focus is on the "plays" subcategory.
- The analysis is based on a dataset that contains information about more than 4k kickstarter projects globally, spanning 9 genres and 41 subcategories. The "plays" subcategory alone includes more than 1k projects. The projects took place between 2009 and 2017.

### Purpose
The purpose of the project is to demonstrate how standard excel functions, combined with simple line charts, can help reveal insights. By defining the methodology, challenges and describing the outcomes, the authors hopes to inspire readers to ask further questions and continue exploting the data.  

## Analysis and Challenges
The methodology for the analysis follows the below steps:
1. Convert the fundraisers' created dates to a readable format.
2. Find out which year and month a project was created in.
3. Analyze the outcomes based on launch dates.
4. Analyze the outcomes based on the goals in USD. 

A few challenges had to be overcome in order to complete the analysis.
1. Converting epoch timestamps to human-readable dates. The following excel formula was used to achieve this "=(((J2/60)/60)/24)+DATE(1970,1,1)"; further reference is available via ![this link](https://www.epochconverter.com/). 
2. Extracting the month name from a data field required some research, too. The standard "MONTH()" formula ins excel returns the month as a numeric value. However, the requirement for the analysis needed the full names of the months. The following formula was used to retrieve the month names as text strings "=TEXT(S2, "mmmm")".

### Analysis of Outcomes Based on Launch Date
The analysis of outcomes based on launch dates required the creation of a pivot table where campaign start months are used as rows, the outcomes are grouped into columns and the count of unique campaigns per outcome represent the values used. Live campaigns are filtered out. 



### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?

## Overview of the Project
- This project aims to reveal how different kickstarter campaigns fared in relation to their launch dates and their funding goals. The focus is on the "plays" subcategory.
- The analysis is based on a dataset that contains data about more than 4k kickstarter projects globally, spanning 9 genres and 41 subcategories. The "plays" subcategory alone includes more than 1k projects. The projects took place between 2009 and 2017. 
---
## Analysis and Challenges: 

Headers are signified with a #. The number of hashtags indicates the level of the header. For example, ### is a third-level header.
Bullets are added in three ways: a typical bullet with an asterisk, a numbered bullet with numbers, or a hyphenated bullet with a hyphen.
Images can be added with the following syntax: ![image_name](path/to/image_name.png).
Hyperlinks to relevant files are  added in a similar manner: [filename](path/to/filename.xlxs).
Line breaks are added by using three consecutive hyphens: ---.
---
Hyperlink to the help page: ![help](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
---


Overview of Project: Explain the purpose of this analysis.
Analysis and Challenges: Explain how you performed your analysis using images and links to code, as well as any challenges you encountered and how you overcame them. If you had no challenges, describe any possible challenges or difficulties that could be encountered.
Results: Answer the following questions in complete and coherent sentences.
What are two conclusions you can draw about the Theater Outcomes by Launch Date?
What can you conclude about the Outcomes based on Goals?
What are some limitations of this dataset?
What are some other possible tables and/or graphs that we could create?

hints
Overview of Project
The purpose and background are well defined (2 pt).
Analysis and Challenges
The overview of the analysis is well described with screenshots (2 pt).
Challenges or difficulties that were encountered, and how they were overcome, are well explained. If there were no difficulties, describe any possible challenges or difficulties that could be encountered (2 pt).
Results
Two conclusions are made about the Theater Outcomes by Launch Date (2 pt).
One conclusion is made about the Outcomes based on Goals (2 pt).
There is a summary of the limitations of the dataset, and there is a recommendation for additional tables or graphs (2 pt).
