# **Crowfunding_kickstarter_data_analysis_** #



## **Overview** ## 
“Louise”, an up-and-coming playwright, is looking to start her first play. She has decided to use crowdfunding as a resource to raise money for it. Louise has asked us for help! She needs insight on what a successful crowdfunding campaigns look like from start to finish, to model hers from.



## **Purpose** ## 

The Purpose of this project is to analyze campaigns to find what models are most successful. Data included money the campaingers were looking to raise(goal), number of backer/donors, and money raised (charted as "Pleged" on Kickstarter worksheet). Success was measured by whether the campaigns reached/exceeded their fundraising goal. This analysis was achieved by creating Pivot tables and corresponding line charts to allow the visualization of the effects, if any, that launch dates and the overall goal have on a campaign. The data was collected across 21 countries, from 2009 to 2017.


## **Analysis and Challenges** ##
Analysis began by using the Kickstarter_analysis workbook, to filter only the "Parent Categories" or Classifications of all the campaign figures collected. From the figures, a Pivot Table was then created to show/compare the total number of campaigns to include successful, failed, live, and canceled campaigns, regardless of their categories. The Pivot table is visualized using a Bar Graph below:

### Parent Categories ###

![Parent_Outcomes](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Parent%20Outcomes.png)


Here , we see that Louise has provided us with quite a bit of data which should hopefully be reflective of the popultion in an effort to allow for her success. 

### Analysis of Outcomes Based on Launch Date ##

The Theater Category was then further analyzed by looking at the Outcomes based on when the Campaigns Launched:

To accomplish this, first, the launched_at column values had to be converted from Unix Epoch time by using the =YEAR(Serial_number) function. This yieled the day, date and year each campaign launched. After this conversion, I then used the year to create a pivot table was to show all Theater campaigns launched from '09 to '17. This is charted as Date Created Conversion and Years in the Kickstarter worksheet. 

Below is the visualization of the outcomes


![Theater_Outcomes_vs_Launch](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)


### Sub Categories ##

From the "Theater" Parent Category, we then parsed through the numbers and created a Pivot Chart with a filter option to include all subcategories. 

Below we ar showing all subcategories for all campaigns.

![sub_stats](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Sub_stats.png)


From here, I went on to show the Subcategory of Plays which visualizes how plays stack up to other Theater sub categories:
![Theater_Subs_Only](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Sub_Only.png)


The subcategory Plays was further analyzed by looking at the outcomes based on the goals, showing overall success. This was acheived by Creating a scale for the goal. The rows were set up to show when the goals were less than $1,000 to $50,000 or more, incrementally increasing by $5,000 for every row.

Successful and Failed campaings with similar goals were added together for the total number of Campaigns. The Percentage successful/failed/canceled was then calculated by taking the total number of the respective campaigns  over the total number of all campaigns in that range. Visualized by creating a Line Chart using the outcomes:

![Outcomes_vs_Goals](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Outcomes_vs_Goals.png)


As expected, as the values were calculated from the total number of campaigns, the failed and successful campaigns are inversely related. As success goes up, fails go down and vice versa.



