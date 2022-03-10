# Kickstarter_Analysis

## Overview
An active Kickstarter campaign that raised much of its funding goal in a short amount of time is being compared to others in the same industry. With the given Kickstarter data set, we examine the relationship between launch dates and funding goals. In this study, successful, fails, and cancelled campaigns are examined for specific categories and subcategories. By the end of the review, the report will identify the most optimal date and funding goals for the campaign to have the greatest chance of success and compare them to the current status of the campaign.

## Analysis and Challenges
In one of the reviews, the success rates are charted based on which quarter and which month garnered the highest success rates. A pivot table is created from the Kickstarter data to isolate the specific population.  In order to gather only the "Theatre" population, the Parent Category and Years are used as filters. In the next section are the Outcomes set on the column and value sections. Finally, Date Created Conversion is placed in the rows portion of the pivot table. With these steps in mind, an adequate pivot table is created that highlights the relationship between the months of the year and its success, fails, and cancelled rates. Additionally, a line graph illustrating trends over time is plotted against the pivot table.

###### Outcomes Based on Goals
The second analysis examines trends within the different funding goals and their success rates. First of all, the funding goals are divided into 12 subcategories of $1000 to $50000 in increments of $5000. By doing so, all the variations can be broken down into funding goals. The campaigns are then divided by success rate; successful, fails, and cancelled. Each success rate percentage is also calculated by dividing the number of each cell by the total number of projects. The COUNTIFS function allows us to filter through different types of success rates and their respective objectives. For example, this function allows us to find the number of successful campaigns between 10000 and 14999.
```
=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays")
```
As a result, a line chart is used to show the trends. It shows the ratios of success, failure, and cancellation in relation to its goals.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/99752443/157615382-d38cd636-4389-4e50-9a59-b9c4bb9e21f1.png)


###### Challenges
As part of the challenge, there are two particular areas of difficulty. The first would be while creating a pivot table for the **Outcomes Based On Launch Dates** analysis. Choosing which criteria to include in the rows, columns, and value sections could be challenging to some. You can overcome this problem by determining the type of table that makes the most sense for the question being asked. Considering the question is asking for the trend of success rates throughout the year, it would make sense to display the Date of Creation on the rows and the Results on the columns of the pivot table.
Another and perhaps the final challenge with *Outcomes Based on Goals* would be to distinguish between COUNTIF and COUNTIFS. It is a minor difference in functionality, but it becomes an issue when COUNTIF would only let you set one range and one condition. If you read through the modules thoroughly, you will find that this is the functionality that is being requested.

## Results
###### Conclusion
Based on the research, the client's campaign's launch date and fund goals were determined to be optimum. Launches in the second quarter of the year tend to have increased success rates beginning in April and peaked in May. Even though campaign success rates throughout the year are typically above 50%, December stands at 49% when it comes to launching campaigns.
In general, funding success is best with lower goals, as shown by the launch dates. However, there are two important areas to avoid when setting up these goal. Within these ranges, the success rates fall significantly well below half of campaigns and more so in the latter. Therefore, it is best to avoid goals between $19999 and $35999 as well as goals above $44999.

###### Dataset Limitations
Despite the fact that the data set provided contains a variety of useful information, the samples cover a span of 8 years, which means that it is outdated since the latest year to be recorded is only 2017. Considering the popularity of Kickstarter, it would be helpful to include the conversion percentage for each campaign. Therefore, it would also include the number of people who viewed the campaign since the set already includes how many people donated to the cause.

###### Further Research
Still, in order to design an optimized marketing campaign for the client, further research is required to find the trends. The following trends could be found:
* To determine the popularity of the **Theatre/Plays** segment on Kickstarter, we have to determine the number of successful plays / failed plays / canceled plays during each year. By doing so, we can determine if Kickstarter is still a viable platform for raising funds or should we opt for another.
* By finding the relationship between the length of the campaign and the success / failure / cancellation rate of each, usually divided by the number of days a campaign is active, you can calculate the optimal campaign length.
* A key aspect of the campaign is finding checkpoints along its length that will indicate if the funds are raised successfully. This is most likely done if more detail is provided as to which part of the campaign is successful. As an indication of the likelihood of success, not only can the campaign be designed effectively but can also be evaluated.
* 
Conclusion: The analysis with the provided data has met the client's needs, however there are more details left on the table that can benefit the client's Kickstarter campaign.
