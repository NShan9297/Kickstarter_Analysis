# **Crowfunding_kickstarter_data_analysis_** #



## **Overview** ## 
“Louise”, an up-and-coming playwright, is looking to start her first play. She has decided to use crowdfunding as a resource to raise money for it. Louise has asked us for help! She needs insight on what a successful crowdfunding campaigns look like from start to finish, to model hers from.



## **Purpose** ## 

The Purpose of this project is to analyze campaigns to find what models are most successful. Data included money the campaingers were looking to raise(goal), number of backer/donors, and money raised (charted as "Pleged" on Kickstarter worksheet). Success was measured by whether the campaigns reached/exceeded their fundraising goal. This analysis was achieved by creating Pivot tables and corresponding line charts to allow the visualization of the effects, if any, that launch dates and the overall goal have on a campaign. The data was collected across 21 countries, from 2009 to 2017.


## **Analysis and Challenges** ##
Analysis began by using the Kickstarter_analysis workbook, to filter only the "Parent Categorys" of all the campaigns' figures collected. From the figures a Pivot Table was created to show/compare the total number of campaigns. This includes successful, failed, live, and canceled campaigns. Pivot then visualized using a Graph Charts:

### Parent Categories ###

![Parent_Outcomes](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Parent%20Outcomes.png)


Here , we see that Louise has provided us with quite a bit of data which should hopefully be reflective of the popultion in an effort to allow for her success. 

The Theater Category was then further analyzed by looking at the Outcomes based on when the Campaigns Launched:

To accomplish this, first, the launched_at column values had to be converted from Unox Epoch time by using the =YEAR(Serial_number) function. After the years were converted, a pivot table was created to show all Theater campaigns from '09 to '17. This is charted as Date Created Conversion in the Kickstarter worksheet. Below is the visualization of the outcomes


![Theater_Outcomes_vs_Launch](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Sub Categories ##

From the "Theater" Parent Category, we then parsed through the numbers and created a Pivot Chart with a filter option to include all subcategories. 

Below we ar showing all subcategories for all campaigns.

![sub_stats](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Sub_stats.png)


From here, I went on to show the Subcategory of Plays which visualizes how plays stack up to other Theater sub categories:
![Theater_Subs_Only](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Sub_Only.png)


The deep dive for the subcategory Plays was analyzed by looking at the outcomes based on the goals, showing overall success. This was acheived by Creating a scale for the goal. The rows were set up to show when the goals were less than $1,000 to $50,000 or more, incrementally increasing by $5,000 for every row.

Successful and Failed campaings with similar goals were added to get the total number and the Percetage successful was calculated over the total number of projects. 

