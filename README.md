# Report

**Title: Evolution of beer preferences**

**Data Stroy** 
The link to data story is accessible via: [Data story](https://ambor1011.github.io/NeverEnoughData/)

**Abstract**

Beer is one of the most used alcoholic beverages in the world. It’s consumption has exceeded more than 185 million kiloliters in recent years. As a beverage that hundred of millions of people drink, its taste and style have experienced considerable evolution. As with any business understanding consumer preferences of beer styles is crucial for producers, distributors, and enthusiasts alike. This report digs into a comprehensive beer dataset, aiming to show the history of beer preferences over time. We are going to investigate what variables are contributing to beer preferences and how they evolve through time.

Our dataset comprises a collection of beer ratings and their associated beers and users, providing a good overview through which we can observe the preferences of beer enthusiasts. We are particularly interested in exploring how the popularity of specific beer styles has shifted over different temporal intervals.

**Research Questions?**

RQ1: How do beer preferences evolve? How do different beer styles become more popular by time? Do they experience a decay in their popularity as time goes on?

RQ2: Which aspects of beers are associated with the popularity of beer the most? Does the importance of these aspects change over time?

RQ3: What is the estimated lag time between introducing a new beer and the gain of popularity on average?

RQ4: Is there any difference geographically between the trends of beer?


**Method**

The first step is to understand the data sets that we have and what each of them represents. What Information they have, generates statistics for the data in order to make a clear understanding regarding the data. 

**RQ 1,2,4:**

To address RQ1,2, we are going to investigate a number of ratings, and ratings for each beer style temporally. As we have four different ratings for each beer and an overall score, we can use these ratings as a metric for users to judge different beer styles. Linear regression is going to be used as the main tool for this objective. We are going to predict the average overall ratings of a beer style (DV) using _year_, _beer_ _style_,_ ratings of aroma_,_ ratings for appearance, ratings for the palette, ratings for taste, and geographical location_. We can use marginal means in order to investigate more in detail how variations in our independent variables would react at their different values. For instance, having an interaction with _year_ and other variables to investigate their influence on the overall outcome. In order to check the no multicollinearity of our regression, we will use variance inflation factors to be sure that our independent variables are not correlated.

We intend to do the analysis on both datasets, and it is interesting to see if the conclusion of both data sets for the similar beer styles is the same or not. As it is concluded in the literature, these data sets are suffering from the herding effect (https://arxiv.org/abs/1802.06578); therefore, it is interesting to check whether the two data sets will end up with the same results or not.

 

**RQ 3:**

We are going to implement almost the same analysis to investigate the time lag of introduction of one beer to the market and its popularity. We choose to use the first rating on the website as an indication of an entrance of beer to the market (this measure overestimates the release date of the beer). We introduce the lag time into the equation and check its association to the overall ratings. As there are newer beers introduced to the market with new initial ratings annually, it is important to see whether the overall demand in the market has increased or these new beers are a response to new beer tastes to the market. To analyze this we used the data on the beer production and sales from the US department of Treasury. We will check the hypothesis if the the sales and production of beers in the US has increased significantly from 2012 (availability of the data) to 2017 (upper bound of data on beer dataset).

**Data filtering:**

As the ratings are the main analysis for us, we are going to remove the beers with less than 10 ratings. This is a way to ensure that the ratings are from users and not some biased review from the producers of the beer (It is important to know that the threshold of 10 may be changed as the project continues). Regarding the ourliers we will remove any data in our feature which is more than Q3 + 1.5 * interquartile range. 

### Proposed timeline 

We set up six sprints, the first one matching the deadline for milestone 2 and the last one corresponding to the final submission.



* 01/12/23 : RQ1,2,4
* 08/12/23 : RQ3
* 15/12/22 : website draft
* 22/12/23 : finish data story, website and review

### Organization within the team 

* Datastory: All
* Website UI: Ambroise
* Visualizations: All
* Methods: All
