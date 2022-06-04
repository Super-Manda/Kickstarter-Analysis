# Kickstarting with Excel
An analysis to uncover trends

## Overview of Project
This assignment began with an initial module that looked at 4115 Kickstarter campaigns.  The client, Louise, has asked us to break down, analyze, and compare other categories and subcategories and then zoom in on theater/plays that were most comparable to her play, and look at the average funding level of each.  

:cherry_blossom: **The older Excel file uploaded to Github contains those findings.**
[KICKSTARTER MODULE FILE](https://github.com/Super-Manda/Kickstarter-Analysis/blob/main/Amanda%20D%20-%20Module%201%20Excel%20Kickstarter.zip)

•	In the initial module, the subcategories needed to be separated from parent category and analyzed separately with a stacked bar chart showing outcomes.  In addition, dates needed to be converted, and then a year column was established.  A column was also made for average donation (rounded with an IfError function) and a color-coded column that reflects the percentage funded were added.  This made it easier to distinguish the failed from the successful, although, the successful and failed U.S. theater productions were also placed on their own tabs.

•	A Descriptive Statistics tab illustrates successful and failed U.S. play projects by goal and amount pledged.  Mean, median, standard deviation, and the quartiles of each are shown.  Most had small goals with a median of around $3,000 and met them with pledges totaling $3,168.

•	VLOOKUP was used to locate particular projects of interest to Louise from the Edinburgh Festival Fringe for a comparison of how they were funded, and they were in keeping with the expected medians.

•	A Box and Whisker Plot is used to demonstrate the mean and median funding goals of musical campaigns and outliers in the range.  The country could be filtered, such as to show only Great Britain.

•	The initial module has a tab for Outcomes based upon Launch Date, which forms the basis of the latest challenge assignment.  This tab uses a pivot chart that is filterable by parent category and year, which shows the monthly vagaries of theater funding outcomes when filtered by theater and broken down by month.  This concluded with a line graph that also looked at the seasonality of successful theater outcomes.  (I chose to put the number in the points on the graph to make it easier on the eye).

Louise then explained that she has particular interest in outcomes based upon launch date and outcomes based upon fundraising goal.  

:cherry_blossom: **The newer Excel file uploaded to Github contains those findings.**
[KICKSTARTER CHALLENGE FILE]( https://github.com/Super-Manda/Kickstarter-Analysis/blob/main/Amanda%20D%20-%20Module%201%20CHALLENGE%20Excel%20Kickstarter%20fewer%20tabs.xlsx)


### Purpose
Louise’s play, “Fever,” has been doing well with fundraising so far.  She wants to use a dataset pertaining to crowdfunding to continue analyzing comparable campaigns based upon debut and fundraising goals.  This report will help Louise to continue to manage her goals and expectations leading up to her launch and give her some pointers for how to meet with as much success as possible.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

•	A Pivot Table was inserted that is filterable by “theater” and “year” that shows how many theater projects were successful, failed, or canceled.  The rows use the “date created” field to isolate the months of the years and provide a total.

•	There were 1,369 theater projects, of which, 839 were successful (61%); 493 failed (36%); and 37 were canceled (3%).  

•	A Line Graph was inserted to display the results.  This Line Graph makes it is easier to see what the “lower success months” are, such as December, because the dots nearly intersect.
 
:cherry_blossom: **Here is the Line Graph based upon theater outcomes versus launch date:** 
![THEATER OUTCOMES VS LAUNCH DATE IMAGE](https://github.com/Super-Manda/Kickstarter-Analysis/blob/main/Theater_Outcomes_vs_Launch.png)


### Analysis of Outcomes Based on Goals

•	Louise has asked to see particular funding goal intervals that go up incrementally in blocks of $5,000.  These were placed on a table and broken down by successful/failed/canceled, as well as providing her with the total and percentages.

•	To fill in the table, the CountIf function is used to isolate the projects that fall into each interval.

•	From this table, a Line Graph was then created using the percentages in each interval.

•	Generally, the smaller the goal, the better the outcome, especially for goals under $5,000, which are about three-quarters successful.  From $5,000 to $24,999, about half are successful (give or take 5%).  Over $25,000, there are fewer projects that qualify at those levels, so the numbers tell a less stable story, but they suggest that there are risks involved overall that the goal will not be met.  Although the graph shows that $45,000 to $49,999 has a 0% success rate, only one project qualified at that funding goal level, compared to hundreds of projects at the lower levels.  So rather than conclude that the $35,000 to $44,999 intervals represent a sudden burst of hope for success amid the dismal failures in the two funding intervals above and the two funding intervals right below it, I would say that the $35,000 to $44,999 intervals combined only totaled 9 projects, and there were 1,047 play projects surveyed, so I would merely conclude that those may have been special projects.  There is not enough evidence because most of the projects are at the lower funding levels, so the few projects that there are at the higher levels may cause the whole percentage statistic of the financial interval to swing like a pendulum between reasonably successful or very unsuccessful.  

•	Nevertheless, I would recommend for Louise to set smaller goals for herself and build up (rather than to set a high expectation from the outset), until more data can be collected and included at the higher funding goal levels.  In this dataset, what would make more sense is to actually combine the final interval to $25,000 and up.  In that instance, there would have been 12 out of 42 successful projects.  Then the percentages would have shown a clearer digression, from 45% success at the $20,000 to $24,999 interval, down to 29% success at the $25,000 and over interval.     

:cherry_blossom: **Here is the graph based upon the outcomes and goal intervals that were requested:** 
![OUTCOMES VS GOALS IMAGE]( https://github.com/Super-Manda/Kickstarter-Analysis/blob/main/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered

•	The first time, I had a hard time isolating the months on the pivot chart regarding outcomes and launch date because I think I “over-tinkered” with it; however, I had no trouble with it the second time.  

•	I also accidentally selected the wrong Line Graph at first, and I couldn’t figure out where the numbers were being pulled from because it did not look like my table.  Eventually, I just started clicking on all of them, and that led me to get the proper chart, but then stylize it.

•	There was also a lot of logic going on in the formulas on the COUNTIFS for the outcomes versus goals chart, but I overcame it by thinking of it as a sentence like, “I need to pull from the Kickstarter tab all of the successful ones that had funding goals of greater than or equal to X but less than or equal to Y, and that were in the Play subcategory.  

•	Also, I find Github to be an extra step compared to writing this report on a Word document with embedded pictures.  I realized that I had to upload the PNG pictures first before I could really address the points in the report.


## Results

- **What are two conclusions you can draw about the Outcomes based on the Launch Date?**

1.	The best month for Louise to launch the theater campaign is May, but since May just passed, the next best choice would be June. The line for “Failed” on the graph is relatively stable, so it may suggest that the “Successful” line could be more affected by seasonality.  She should take advantage of the good weather.
2.	The worst month for Louise to launch would be December, and that may be because people are funding holiday shows or giving to other charities or perhaps not thinking about funding theater.


- **What can you conclude about the Outcomes based on Goals?**

•	Generally, the lower the fundraising goal, the more likely a campaign is going to be successful; however, there are also more of the small projects than the large ones.  Successful projects with under $10,000 funding goals constituted 622 of the 694 successful projects (90%), so it is hard to make comparisons to the successful plays with larger goals.  


- **What are some limitations of this dataset?**

•	There are outliers in fundraising, and we don’t know where they specifically needed to spend the money, such as on the venue, costumes, set design, better quality actors, etc.

•	We do not know true success or failure based upon funding alone.  For example, a play that “failed” in its fundraising goal may have made do with fewer resources and still entertained the masses, while a low-budget play that “succeeded” in its fundraising goal may not have been enjoyable to people on a shoestring budget.  They’re not giving us any “Siskel and Ebert ratings” for these plays.

•	This data set spans campaigns from 2009 to 2017, so, while it has historical value, we don’t know if people are frequenting plays as much anymore today.  Unless there is updated data, this doesn’t fully assure Louise of a success.  

•	Some of the categories and subcategories were separate, like plays, musicals, and drama.  There may have been a bigger picture if analyzed all together.


- **What are some other possible tables and/or graphs that we could create?**

•	As aforementioned, I would re-create the graph with the funding goals to instead interval “$25,000 and over” all together, so as to combine the number of projects in that statistic and get a more reliable understanding.  

:cherry_blossom: **Here is the Line Graph of my suggested adjusted intervals:** 
![ADJUSTED FUNDING INTERVALS GRAPH]( https://github.com/Super-Manda/Kickstarter-Analysis/blob/main/Adjusted_Intervals_Graph.png)

•	The Outcomes Based on Goals may make sense as a stacked bar chart, so that it can better compare to the previous stacked bar charts on Parent category and Subcategory Outcomes.

•	A Pie Chart may work to illustrate, out of all the Kickstarter campaigns, how much of the market is dedicated to plays.  Given that there are a lot of plays represented, it may also be interesting to figure out if some of the plays pose competition to any other plays.  For example, maybe the larger ones are not meeting their fundraising goals because people could just go to Broadway at that point!  This would be more of a qualitative review of the blurb to determine if plays with similar plotlines in the same country may pose competition to one another.

•	A table could be created that estimates how many donors Louise will need on average relative to average pledge amounts for comparable plays.  This will give Louise an idea of when she will hit her target.  Also, the deadline column is rather ignored in the dataset, so it may be helpful to see how long it takes to assemble the funds from each donor before the launch date.  For example, one play could have more generous donors, so it requires less time to meet the goal, whereas another play may have less generous donors, so it takes them more time to meet the goal.  Therefore, Louise needs to know what kind of donors she has now.  This will also help her tailor the marketing to meet their needs.  

•	Overall, if more data is collected, it may be interesting to see if more money is needed now compared to when this data was first collected, given that there may be hidden costs now, such as letting seats go vacant and/or lower viewership, PPE for ticket takers, cleaning of theater seat cushions, etc.   Once those costs are factored in to the budget, that may decrease success rate, or it may decrease the amount of plays that people want to get involved with producing.  The “Country” field may also be of interest to such a study as that, because the lockdowns affected each country differently in terms of theatergoing.
