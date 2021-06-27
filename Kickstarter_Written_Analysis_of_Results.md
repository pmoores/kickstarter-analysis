# Kickstarting with Excel

## Overview of Project
Louise’s play Fever came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals.

### Purpose
The purpose of this project is to demonstrate how different campaigns fared in relation to their launch dates and their funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I first created a new column within the Kickstarter_Challenge.xlsx workbook to display the Year each Kickstarter campaign was created. Used YEAR() function to pull the year each Kickstarter was created from the 'Date Created Conversion' column. Next, I created a pivot table to display 'Theatre Outcomes by Launch Date". This table displays the month a Kickstarter campaign began and whether or not the campaign was successful, failed or was canceled. A filter was applied to "Parent Category" to display only data for 'theatre'.
[Pivot Table - Theater Outcomes by Launch Date](https://github.com/pmoores/kickstarter-analysis/blob/main/Resources/Pivot_Table_Outcomes_by_Launch_Date.png)

Finally, a line chart was created to display Theatre Outcomes by Launch Date. This table allows us to understand what months of the year had the most successful campaigns, what months had the most failed campaigns and and what months had the most canceled campaigns.


### Analysis of Outcomes Based on Goals
First, I created a table in a new sheet titled "Outcomes Based on Goals". Ranges of dollar amounts were created to perform an analysis of the number and percentage of campaigns that were successful, failed, or were canceled. Next, the COUNTIFS() function was used to populate each goal range within the table. For example, the formula used to display the number of successful plays campaigns with a goal range of $10000 to $14999 is =COUNTIFS(Kickstarter!F:F, "successful",Kickstarter!D:D,">=10000",Kickstarter!D:D,"<=14999", Kickstarter!R:R, "plays"). This formula only counts 'successful' campaigns in column F of the Kickstarter sheet, within a range of $10000 to $14999 in column D, and only those labelled as 'plays' in column R. The SUM() function was then used to display the "Total Projects" under each goal range. A basic equation was used to find the percentage of 'plays' campaigns that were successful, failed or were canceled. For example, to find the percentage of successful plays with a goal of less than $1000, the number successful was divided by the total projects in that goal range. The new cells were then formatted to display percentages.

[Pivot Table - Outcomes Based on Goals](https://github.com/pmoores/kickstarter-analysis/blob/main/Resources/Pivot_Table_Outcomes_Based_on_Goals.png)

Finally, a pivot line chart was created to display the percentage of plays that were successful, failed or canceled based on the campaigns goal range.


### Challenges and Difficulties Encountered
- The most significant challenge that was encountered was creating the long COUNTIFS() equations and then transposing the formula to other cells. Also, there were no plays that were cancelled, so all of the Percentage Cancelled cells showed 0%. I went back to the Kickstarter sheet and used filters to verify that there were no canceled 'plays' campaigns.


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

[Line Chart - Theater Outcomes vs. Launch Date](https://github.com/pmoores/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

Theatre campaigns launched in May have the most success. April, June and July also had higher numbers of successful theatre campaigns. Failed campaigns were highest from May to August and then October. Cancelled campaigns were relatively constant across the year.

Conclusion 1: No matter what month, there are always a higher number of successful campaigns than failed or canceled campaigns. Theatre campaigns have a higher probability for success than failure or cancellation.

Conclusion 2: May is the best month to launch a campaign as the frequency of successful campaigns is highest in this month. Also, the ratio of successful campaigns to failed campaigns is highest in this month (111 successful:52 failed).


- What can you conclude about the Outcomes based on Goals?

[Line Chart - Theater Outcomes Based on Goals](https://github.com/pmoores/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

Conclusion 1: The best goal ranges to launch a 'plays' Kickstarter campaign are: $1 to $4999 (72.66% successful), $35000 to $39999 (66.67% successful) and $40000 to $44999 (66.67% successful). Campaigns within these goal ranges have the highest percentage of success.

Conclusion 2: The worst goal ranges to launch a Kickstarter campaign are: $25000 to $29999 (80% failed) and $45000 to $49999 (100% failed). Campaigns within these goal ranges have the highest percentage of failure.

- What are some limitations of this dataset?
The major limitation of a dataset this large is the potential for missing data. Any missing data would skew the analysis. This dataset also contains outlier data (as demonstrated in the Box and Whisker exercise). This outlier data can skew analysis, especially the mean.

- What are some other possible tables and/or graphs that we could create?
- Theatre Outcomes by Country - to determine what countries have the most successful theatre Kickstarter campaigns.
- Theatre Outcomes by Backers - to determine if a campaign should target a larger group or a more focused interest group.



