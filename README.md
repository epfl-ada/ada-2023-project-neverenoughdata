# Report

**Title: Evolution of beer preferences**

**Abstract**

Beer is one of the most used alcoholic beverages in the world. It’s consumptions has exceeded more that 185 million kiloliters in recent years. As beverage which hundred millions of people drink, its taste and styles has experienced considerable evolution. As any business understanding consumer preferences of beer styles is crucial for producers, distributors, and enthusiasts alike. This report digs into a comprehensive beer dataset, aiming to show the history of beer preferences over time. We are going to investigate what variables are contributing in beer preferences and how does they evolve through time.

Our dataset comprises a collection of beer ratings and their associated beers and users, providing a good overview through which we can observe the preferences of beer enthusiasts. We are particularly interested in exploring how the popularity of specific beer styles has shifted over different temporal intervals.

**Research Questions?**

RQ1: How does beer preferences evolve? How does different beer styles become more popular by the time? Do they experience a decay in their popularity as time goes?

RQ2: Which aspects of beers are associated with the popularity of beer the most? Does the importance of these aspects change during the time?

RQ3: What is the estimated lag time between introducing a new beer and the gain of popularity on average?

RQ4: Are there any difference geographically between the trends of beer?

**Additional datasets**

Our datasets contains of two datasets from two big beer review websites RateBeer and BeerAdvocate. Therefore our datasets contains reviews from users and rates beers with a text reviews. However, there is no data on consumption of beers. This information is very important, as the increase number of reviews may be caused by the increase of production of the beers and therefore, no concrete conclusion could be made. After searching through internet, we found that Alcohol and Tobacco Tax and Trade Bureau of the United States department of treasury publishes data regarding production and sales of beers in the united states from 2012 to 2023. The data that they publish is on PDF or Excel files and they could be quarterly at the level of states or monthly at the national level. We use this data to implement the robustness check on our analysis at least for the data in the United States. On additional_data directory, the excel files are available. 

**Method**

The first step is to understand the data sets that we have and what each of them represents. What Information they have, generate statistics for the data in order to make a clear understanding regarding the data. 

**RQ 1,2,4:**

To address RQ1,2, we are going to investigate, number of ratings, ratings for each beer style temporally. As we have four different ratings for each beer and overall score, we can use these ratings as a metric for users to judge different beer styles. Linear regression is going to be used as the main tool for this objective. We are going to predict the average overall ratings of a beer style (DV) using _year_, _beer_ _style_,_ ratings of aroma_,_ ratings for appearance, ratings for palette, ratings for taste and geographical location_. We can use marginal means in order to investigate more in detail how does variations in our independent variables would react at their different values. For instance having an interaction with _year_ and other variables to investigate their influence on the overall outcome. In order to check the no multicollinearity of our regression we will use variance inflation factors to be sure that our independent variables are not correlated.

 

**RQ 3:**

We are going to implement almost the same analysis to investigate the time lag of introduction of one beer to the market and its popularity. We choose to use the first rating on the website as an indication of an entrance of beer to the market (this measure overestimates the release date of the beer). We introduce the lag time into the equation and check its association to the overall ratings. As there are newer beers introduced to the market with new initial ratings annually, it is important to see whether the overall demand in the market has increased or these new beers are a response to new beer tastes to the market. To analyze this we used the data on the beer production and sales from the US department of Treasury. We will check the hypothesis if the the sales and production of beers in the US has increased significantly from 2012 (availability of the data) to 2017 (upper bound of data on beer dataset).


### **Proposed timeline **

We set up six sprints, the first one matching the deadline for milestone 2 and the last one corresponding to the final submission.



* 01/12/23 : RQ1,2,4
* 08/12/23 : RQ3
* 15/12/22 : website draft
* 22/12/23 : finish data story, website and review

### 
**Organization within the team **

* Datastory: All
* Website UI: Ambroise
* Visualizations: All
* Methods: All
