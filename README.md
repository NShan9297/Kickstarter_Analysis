# **Crowfunding_kickstarter_data_analysis_** #



## **Overview** ## 
“Louise”, an up-and-coming playwright, is looking to start her first play. She has decided to use crowdfunding as a resource to raise money for it. Louise has asked us for help! She needs insight on what a successful crowdfunding campaign looks like from start to finish, to model hers from.



## **Purpose** ## 

The Purpose of this project is to analyze campaigns to find what models are most successful. Data included money the campaingers were looking to raise(goal), number of backers and donors, and money raised (charted as "Pleged" on Kickstarter worksheet). Successful campaigns were determined by whether the campaigns reached/exceeded their fundraising goal. While Failed campaigns were those that did not reach their goal. This analysis was achieved by creating Pivot tables and corresponding line charts and graphs, to allow the visualization of the effects, if any, that the Launch Dates and the Outcomes based Goals have on a campaign. The data was collected across 21 countries, from 2009 to 2017, then compiled in an Excel Worksheet called Kickstarter Analysis. 


## **Analysis and Challenges** ##
Analysis began by using the Kickstarter Analysis worksheet, to filter only the "Parent Categories" or Classifications of all the campaign figures that were collected. From the figures, a Pivot Table was created to show/compare the total number of campaigns which included all successful, failed, live, and canceled campaigns, regardless of their categories.

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
