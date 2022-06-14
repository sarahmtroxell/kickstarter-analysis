# An Analysis of Kickstarter Campaigns

## Overview of Project
A fictional playwright named Louise is looking to raise over $10,000 to fund a play she wrote. She asked for advice on how campaigns work and what makes them successful. This project will analyze data from Kickstarter, a crowdfunding platform, to give Louise insight to trends of successful, failed, cancelled, and ongoing historical campaigns.

### Purpose
The purpose of this Kickstarter Challenge was to use Excel techniques to analyze a medium sized data set and provide a data-driven recommendation. Our course included self-paced learning, exercises, and in class instruction to teach various Excel features. 

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
The campaign goal, or overall amount of money that a funder wants to raise, is also a key characteristic of why a campaign may fail or succeed. If a campaign is seeking an extremely low amount of money, one may predict it will likely be successful. To test this theory and uncover additional insight, I created an Excel table with ____. I built a PivotChart to display the _______. 

![Outcomes vs Goals](../main/resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
One part of the assignment included creating an Excel table that counted the outcomes of projects based on their target funding goal. Categories of funding goal ranges were listed in rows, then I needed to use the COUNTIFS function to count each outcome with a goal between the category range. I felt this opened the results up to risk of manual error because I had to manually type in all 12 categories into the COUNTIFS statement. I overcame this challenge by instead using the Excel RIGHT and LEFT functions to directly reference and parse the upper and lower bound for each goal category. 

![LEFT_RIGHT_fuctions](../main/resources/EXCEL_Left_Right.png)

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
    - Remove outliers
    - Length of campaign
    - Campaigns per year
