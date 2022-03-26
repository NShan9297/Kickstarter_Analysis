# **Crowfunding_kickstarter_data_analysis_** #



## **Overview** ## 
“Louise”, an up-and-coming playwright, is looking to start her first play. She has decided to use crowdfunding as a resource to raise money for it. Louise has asked us for insight on what a successful crowdfunding campaign looks like to model hers from. Louise is looking for about $10,000 to fund her play. 



## **Purpose** ## 

The Purpose of this project is to analyze campaigns to find what models are most successful and which failed. Successful campaigns were determined by whether the campaigns reached/exceeded their fundraising goal based on funds/money pledged. While Failed campaigns were those that did not reach their goal based on funds/money pledged. From this data, Louise will have some statistical support to help her tackle her crowdfunding journey. 

## **Analysis and Challenges** ##

The main focus of this analysis will be on Successful Campaings, Failed Campaigns, their Launch Dates and their Pledged and Goal amounts. This analysis was achieved by creating Pivot tables and corresponding line charts and graphs, to allow the visualization of the effects, if any, that those Launch Dates and the Outcomes based Goals have on a campaign. The data was collected across 21 countries, from 2009 to 2017, then compiled in an Excel Worksheet called Kickstarter Analysis. Analysis began by using the Kickstarter Analysis worksheet, to filter only the "Parent Categories" or Classifications of all the campaign figures that were collected. From the figures, a Pivot Table was created to show/compare the total number of campaigns which included all successful, failed, live, and canceled campaigns, regardless of their categories.

The Pivot table visualizing this is shown in the Bar Graph below:


### Parent Categories ###

![Parent_Outcomes](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Parent%20Outcomes.png)


Here, we see that Louise has provided us with what appears to be sufficient data to be reflective of the popultion.

From this, we then begin to take a closer look at the Parent Category, Theater which is the parent for Louise's subcategory, "Plays".

### **Analysis of Outcomes Based on Launch Date** ###

The Theater Category was analyzed by looking at the Outcomes based on when the Campaigns Launched:

To accomplish this, first, the launched_at column values had to be converted from Unix Epoch time by using the =YEAR(Serial_number) function. This yielded the day, date and year each theater campaign was launched. After this conversion, I then used the year to create a pivot tableto show all Theater campaigns launched from '09 to '17. This is charted as Date Created Conversion and Years in the Kickstarter worksheet and visualized below:



![Theater_Outcomes_vs_Launch](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)


### **Sub Categories** ###

From the "Theater" Parent Category, we then parsed through the numbers and created a Pivot Chart with a filter option to include all subcategories. 

Below we are showing all subcategories for all campaigns.

![sub_stats](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Sub_stats.png)


From here, I went on to show the Subcategory of Plays which visualizes how plays stack up to other Theater sub categories:
![Theater_Subs_Only](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Theater_Sub_Only.png)

### **Analysis of Outcomes Based on Goals** ###

The subcategory Plays was further analyzed by looking at the outcomes based on the goals, showing overall success. This was acheived by creating a scale for the goals. The rows were set up to show when the goals were less than $1,000  up to $50,000 or more, incrementally increasing by $5,000 for every row.

Successful and Failed campaings with similar goal ranges were added together for the total number of campaigns. The Percentage successful/failed/canceled was then calculated by taking the total number of the respective campaigns over the total number of all campaigns in that range. Visualized by creating a Line Chart using the outcomes shown below:

![Outcomes_vs_Goals](https://github.com/NShan9297/kickstarter_analysis/blob/main/Resources/Outcomes_vs_Goals.png)


As expected, as the values were calculated from the total number of campaigns, the failed and successful campaigns are inversely related. As success goes up, fails go down and vice versa.

Here we see that, on average, the higher the goal, the lower the success rate after about $15,000.


### **Challenges and Difficulties Encountered** ###

The most challenging aspect of this project was creating the outcomes based on goals Line Chart. The COUNTIFS function was required to sequester the correct data. The references were pulled from another worksheet and quite specific. The formula was very lengthy and required 3 separate and unique formulas to yield to correct values in the ranges. I was not able to find a shortcut for getting the correct values in each cell. I overcame this challenge by first copying the longest formula which was for the 'X' to 'X' goals (e.g. 1000 to 4999). I used this for the full row inputting the incremental ranges and I went and then used this for the next column by just swapping out the data. Classmates also helped.



## **Results** ##

**Outcomes Based on Launch Date**

By looking at this specific data set, we are able to conclude when Louise should and shouldn't start her project.

May has the highest number of overall campaigns; this could be due to May launches being an industry norm or perhaps the weather. May also has the highest success rate for campaigns. If Louise is not able to launch in May, it is best for her to start before the end of June because the numbers begin to trail off and look more like the remainging months.

October is also a good contender because there are more successful campaigns than failed, and over the 8 years tracked, no campaigns were canceled but evey other month has canceled campaigns

She should not start in December because the number of failed and successful campaigns becomes almost equal. This decreases her chances of having a successful campaign as her chances of failing are about 50%. Also, December is the only month that consistenly reaches this point. 


**Outcomes Based on Goals**

The chart shows that Louise **_may_** not reach her campaign goal. The most succces is seen with campaigns that are $1,000 or less, with almost 80% of them reaching their goal. A goal of $1,000 to $4,999 is about the same. The numbers steadily decrease from this point until a goal of about $35,000. However, at this goal point, the fundraising pool is **_very_** low. From the $25,000 goal mark and on, the campaign totals are mostly in the single digits. Those that are double digits are lower double digits and mostly failed camapigns. At the $35,000 goal mark we see some success, but the data suggests that there is some special circumstance or factor that has allowed for those successes. Maybe the playwright has made a name for themselves? Maybe it is a popular/awaited play. As Louise is just starting out, she may have to source a lot of backers to meet her goal. Louise's goal of $10,000 is possible, but it is safer for her to choose a maximum of $5,000 to begin with. 


**Data Limitations**

The analysis of the data provided is somewhat broad. A deeper look into the number of backers would have shone a light on how many people are donating and at what goal range. This could show how many people are potentially needed to meet said goal. We also took a look at average donations which could have been even more illuminating. For example, if your goal of $15,000 requires on average, 300 backers, you may not have the time or resources to source from this large number of people. Ultimately, this seems to be a critical missing piece of this project.
