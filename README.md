# Kickstarting with Excel

## Overview of Project

### Background
Over the course of Module 1, we analyzed a dataset of crowdfunding campaigns to help the playwright Louise gain an understanding into the factors that made previous crowdfunding campaigns successful. With this understanding, Louise will be well equipped to fund her own upcoming play, "Fever". 

### Purpose
The purpose of this analysis is to visualize fundraiser outcomes based on launch date and the percentage of successful, failed, and canceled plays based on funding goal amount. Once completed, we'll be able to use our visualizations to draw useful conclusions about our crowdfunding campaign data.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To perform my analysis for the first deliverable, I created a pivot table from the Kickstarter data and placed the pivot table in a new sheet, "Theater Outcomes by Launch Date." Second, I filtered the pivot table by "Parent Category" and "Years" and assigned the specified table fields. After filtering the column labels to exclude "live" fundraisers, I filtered the "Parent Category" to include only "theater" data and sorted the campaign outcomes in descending order. Lastly, I created and labeled a line chart, using the data from the pivot table, to visualize the relationship between outcomes and launch date (specifically launch month). 

![Outcomes based on Launch Data](https://github.com/dharlerjr/kickstarter-analysis/blob/d84c52aafd62c1092b91a1d6cd850129f2987db3/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To perform my analysis for the second deliverable, I created a new sheet titled "Outcomes Based on Goals" and created 8 columns of data in the new sheet. In column 1, labeled "Goal", I used the suggested dollar-amount ranges to enable us to group projects based on goal amount. Next, to populate columns 2-4, I used the countifs() function to count the number of successful, number of failed, and number of canceled plays based on their goal amount. To populate column 5, I used the sum() function to calculate the "Total Projects" for each row. Lastly, in columns 6-8, I simply found the percentage of successful, failed, and canceled plays for each row (based on goal amount). Once the data was correctly organized, I created a line chart to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled plays. 

### Challenges and Difficulties Encountered
Overall, I only encountered one challenge in this assignment: figuring out how to correctly use the countifs() function for Deliverable 2. At first, I had trouble figuring out what arguments to pass into the function and how to split up the chain of inequalities found in Goal Ranges such as "1000 to 4999." Luckily, after some experimentation and research, I was able to figure out the proper countifs() syntax and usage.

## Results

What are two conclusions you can draw about the Outcomes based on Launch Date?
- First, the most successful Theater campaigns were launched in May, then June. Second, very few Theater campaigns were canceled. Thirdly, no matter the month, more Theater campaigns succeeded than failed, even in December, when 35 campaigns failed and only 37 campaigns succeeded.

What can you conclude about the Outcomes based on Goals?
- According to the line chart in the "Outcomes Based on Goals" sheet, the largest percentage of successful plays had a goal amount of either "Less Than 1000" or "1000 to 4999." Similarly, the largest percentage of failed plays had a goal amount of "45000 to 49999." However, no matter the outcome, there was only one play in all that had a goal amount of "45000 to 49999," and this one play failed. 


What are some limitations of this dataset?
- By examining the two sheets that we created in the past two deliverables, I noticed that there are very few canceled Theater campaigns and zero canceled Play campaigns. Consequently, we won't be able to draw as many conclusions about canceled campaigns as we drew about successful and failed campaigns. Similarly, there are plenty of Play campaigns with goal amounts of under 15000, but there are comparitively almost no campaigns with goal amounts of over 15000. Thus, our percentages for more expensive campaigns are not as meaningful as our percentages for less expensive campaigns. 


What are some other possible tables and/or graphs that we could create?
- First, I would love to see how successful campaigns for plays are compared to any other parent category, such as campaigns for film & video or technology. To perform this analysis, we could simply create a table that would tell us how many campaigns were successful, failed, or canceled based on parent category. Then, based on whatever trend we find in our copmarison, we could attempt to discover an underlying relationship between campaigns for plays and campaigns for technology. For instance, maybe campaigns for technology are more successful than campaigns for plays because campaigns for technology have a lower target goal than campaigns for plays. 
