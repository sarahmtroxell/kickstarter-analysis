# An Analysis of Kickstarter Campaigns

## Overview of Project
A fictional playwright named Louise is looking to raise over $10,000 to fund a play she wrote. She asked for advice on how campaigns work and what makes them successful. This project will analyze data from Kickstarter, a crowdfunding platform, to give Louise insight to trends of successful, failed, cancelled, and ongoing historical campaigns.

### Purpose
The purpose of this Kickstarter Challenge was to use Excel techniques to analyze a medium sized data set and provide data-driven advice to help her campaign succeed. Our course included self-paced learning, exercises, and in class instruction to master various Excel features.

The main areas of focus were: 

1. Pivot Tables
2. Pivot Charts 
3. Built in Formulas (SUM, IF, COUNTIF, ROUND, IFERROR)
4. Static and Conditional Formatting

## Analysis and Challenges


### Analysis of Outcomes Based on Launch Date
To identify if the launch date had an effect on a campaign's outcome, I created an Excel PivotChart and PivotTable to organize and visualize the data. Louise can start her campaign in any month, but not in any year, so I decided to view monthly trends for this data. I set my PivotTable rows to Months, columns for each possible outcome, a count of the outcomes for values, and added two additional filters for the campaign parent category and launch year. I then filtered to show data only related to Theater campaigns so it would be the most relevant. To visualize the data, I created a linked PivotChart that displayed the outcome counts by type and launch date month in a stacked line graph (shown below).

![Theater Outcomes vs Launch](../main/resources/Theater_Outcomes_vs_Launch.png)

Campaigns beginning in December were the only month where more campaigns failed than succeeded. This may be due to holiday gift giving and other donations, so there are more competing places for people to spend extra money, hurting the campaigns launch. People are often busier around the holidays, so they may not have heard or found the campaign in their free time. We can conclude December is likely the worst time to launch a campaign. 

When filtered to Louise's category of theater, successful campaigns significantly spike in May, June and July. The amount of failed campaigns stays around its typical value, but the spike in successful campaigns makes the proportion of successful campaigns much higher. Therefore, we can conclude that the best time for Louise to launch her campaign is between May through June. 

### Analysis of Outcomes Based on Goals
The campaign goal, or overall amount of money that a funder wants to raise, is also a key characteristic of why a campaign may fail or succeed. If a campaign is seeking an extremely low amount of money, one may predict it will likely be successful. To test this theory and uncover additional insight, I created an Excel table to display the outcomes based on total campaign goal. The rows broke the campaign goals into categories in increments of $5,000 and the colums had the total number of each outcome type and corresponding percetage of successful, failed, or cancelled campaigns. I used a COUNTIF function in Excel to populate the total number of each campaign type and the SUM function to calcuate the total number of projectes for each goal category. Using both of these calculated metrics, I found the percentage of successful, failed, and cancelled campaigns in each cateogry by dividing the count of each outcome type by the total campaigns for each row.  I built a PivotChart to display the percentages in a stacked line chart. Each outcome type was given its own line on the graph to display the outcome percentage by goal amount. 

![Outcomes vs Goals](../main/resources/Outcomes_vs_Goals.png)

Based on the PivotChart, campaigns with a funding goal of $45,000 or more have the highest failure percetage. This is shown on the orange line, where it spikes up to 100% failed campaigns between $45,000 to$49,999 and 83% for campaigns over $50,000. This aligns with my intital prediction that higher campaign goals would be harder to reach due to the large amount or size of donations needed. The campaign goal amount and the failure percentage did not always follow a positive linear relation though; for campaigns with a goal between $35,000 to $49,999 they were actually more likley to succeed than fail in our data set, which does not follow the trend of the other categoires. 

### Challenges and Difficulties Encountered
The assignment included creating an Excel table that counted the outcomes of projects based on their target funding goal. Categories of funding goal amounts were listed in rows and the count of each outcome needed to be calculated for each goal category range and outcome type. I needed to use the COUNTIFS function to count each outcome with a goal between the category range. I felt this opened the results up to risk of manual error because I had to manually type in all 12 categories into the COUNTIFS statement and it would take a great deal of time to manually edit the code for each row. I overcame this challenge by instead using the Excel RIGHT and LEFT functions to directly reference and parse the upper and lower bound for each goal category, shown in the screenshot below. 

![LEFT_RIGHT_fuctions](../main/resources/Excel_LEFT_RIGHT.png)

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    - Campaigns beginning in December were the only month where more campaigns failed than succeeded, therefore December is the worst time to launch a campaign. 
    - The best time to launch a theater campaign in hopes of success is between May through June.

- What can you conclude about the Outcomes based on Goals?
    - Campaigns with a target goal with $45,000 or more failed more than they succeeded.
    - Campaigns with a target goal of less than $1,000 were the most successful.

- What are some limitations of this dataset?
    
    - We were given no data on the Kickstarter campaign leaders. If we had their age, gender, number of previous successful projects, funds raised outside of Kickstarter, etc. we could tailer a more specific recommendation to Louise.
    - Kickstarter was created in 2009. Our data set includes campaigns from their first year launched, which might impact the data when we view trends based on time.
    - Campaigns could be successful for reasons beyond their target goal, launch date, and category. A main influencer could be if the campaign had external marketing (TV, radio, flyers) or was only spread by work of mouth and Kickstarter. Campaigns that had external marketing could look inflated in this data set. 

- What are some other possible tables and/or graphs that we could create?
    - To remove outliers that may skew data, we could add a column to the main data sheet called "Outlier" and use statistical forumulas nested in an If statement to signify if the value is an outlier ("Yes") or not ("No"). Then a filter can be added to each PivotTable and PivotChart allowing us to filter out the "Yes" outlier values to see if the trends are impacted.
    - I would also be interested to see what relationship the length of a campaign has with its success and its funding goal. We have the start and end date of the campaigns, so a a new column could be added to calculate the campaign length. Then a a Pivot Table could be added with the campaign length divided into segmented intervals as rows, the outcome types as columns, and the count of outcomes as values. Additonally, a Pivot Table could be inserted to visualize the data using a stacked line chart, graphing the length of campaign on the x-axis and count of outcome type on the y-axis.
