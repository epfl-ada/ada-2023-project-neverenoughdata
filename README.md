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

**RQ 1**

To address RQ 1, we used clustring technique to evaluate two metric for different beer styles. 
Metric 1: Rating’s average

In this metric it is about grouping a set of beer together and take the mean of those beers. The changes of this metric []through time[] can be explained by two ways :

It shows that a group of beer is less/more appreciated through a certain period of time
It shows that the actual beers of this group get better through time Those 2 explanation can also be seen as one. For instance if blonde beer become has a better rating average in 2015 than 2003, does this mean that blond beer has a better taste in 2015 or does it mean that poeple like more the blond beers in 2015 than in 2003. This is effectively quite subjective, but it tells the same at the end.
Metric 2 : Number of rating

This one is the more interresting : it measure the number of rating for a certain group of beer. This metric express a sort of popularity.

**RQ 2:** 
n this research question we would like to answer, which aspect of the beer in the ratings (aroma, appearance, taste, pallate and overall rate) have the highest impact on the popularity of the beer. First lets visualize the ratings for each of these aspects during the time we have data, to see if the perception of reviewers towards different beer styles in each of these aspects is changed or not.

To answer this question we should define the popularity in this context. For the research question we define the popularity as follow.

Metric 3

Populairty = scaled number of reviews per beer style per year * average rating per beer style per year.

The reason to construct the populaity like this is the fact that, the number of reviews are not constant during different years therefore we need to devide the number of reviews for each beer style per year by total number of reviews in that year to find a relative attaction of certain beer style for writting the review. But having number of review is not only pillar to quality and acceptance of a beer, maybe we can have a bad beer with high number of reviews. Therefore, we multipy the relative number of comments to average rating for that year and beer style. This metric could represent the populaity of beer.

Now we have our dependant varibale, lets talk about the independant varibales. We are going to use aroma, appearance, taste, pallate and overall rate as our IVs. But before construcitng the regression we need to make sure our independant variables are indeed independant

**RQ 3:**
The third research question tries to assess the time it takes for a beer to get popular. This analysis holds on two date definitions : the date the beer is released ; and the date it becomes popular.
This analysis, to be relevant must only be ran on beers with a high number of ratings, so that the beer is really popular, we’ve chose 500.
The release date is defined as the earliest rating we have in our dataset, to avoid beers released before dates in our dataset, we neglect all beers appearing in ratings in the two first years of activity of the website (2000, 2001).
The “popularity reach date” is defined as the average between the time taken to reach 500 ratings and the time to reach the highest increase in number of ratings. This average smoothes the differences in popularity (500 ratings threshold) and trendyness.

**RQ 4:**

In this section we try to analyze how beer preferences change in different parts of the world. We analyze both popularity (taken as the number of ratings) as well as appreciation (taken as the mean rating). We focus on beer styles, the ones provided in the data frame, and not on specific beers.

**Data filtering:**

As the ratings are the main analysis for us, we are going to remove the beers with less than 10 ratings. This is a way to ensure that the ratings are from users and not some biased review from the producers of the beer (It is important to know that the threshold of 10 may be changed as the project continues). Regarding the ourliers we will remove any data in our feature which is more than Q3 + 1.5 * interquartile range. 



### Organization within the team 

* Datastory: All
* Website UI: Ambroise
* Visualizations: All
* RQ1: Ambroise
* RQ2: Amirsiavosh
* RQ3: Jules
* RQ4: Kuba
* Ethical Risk: Amir
