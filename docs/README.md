**By: Sourabh Lal, Sonia Alouni, Charlotte Theisen**

# Introduction

Amazon.com has been making waves for the past decade or so, as they grow stronger and stronger. What once started as a small online bookstore, has now become not just America’s largest retailer; but a company bigger than most brick and mortar retailers in America put together.

![Amazon_growth](/ada2017/images/amazon_growth.PNG)


We are now right in the middle of America’s great retail period; the holiday season from Thanksgiving till Christmas!  Amazon has said the 2016 holidays were its best-ever shopping season. During the winter holiday season, not only did they sell 50% more items than the previous year, but they also doubled their total sales for 2016 [(Source)](http://fortune.com/2017/01/04/amazon-marketplace-sales/).

One of the consequences of this amazing growth has been an explosion of data. Every product sold on amazon has metadata than can be analyzed and insights can be gained. Furthermore, Amazon has excelled in collecting consumer reviews of products sold on their website and we have decided to delve into the data to see what trends and patterns we could find!

The data we examine in this project comes from the [McAuley Amazon Review Dataset](http://jmcauley.ucsd.edu/data/amazon/). This dataset contains reviews of products sold on Amazon spanning a time period from May 1996 to July 2014, as well metadata about each of these products. 

Naturally, many people, whether happy or disappointed, will want to share their opinion of their new product with the world. Even within the single product category Electronics, more than 1.5 million reviews have been written by the consumers. This is the category we will examine further here, but it should be noted that we have looked at other categories and observed similar trends and patterns.


# Amazin' growth
The amount of reviews written on Amazon is of course a different thing than the amount of sales. However, we did suspect that the growth of Amazon's sales must have an effect on the amount of reviews - if more products are sold, surely more products must be getting reviews. Therefore, we visualized the number of reviews per day over the entire time period available in the dataset along with a moving average. 

<iframe width="100%" height="400" src="/ada2017/images/1_number.html" frameborder="0"></iframe>

The number of reviews is a good indicator of how people’s use of Amazon reviews has evolved through the years. As suspected we do indeed see a very clear trend that seems to accelerate every year. In the first decade of Amazon's existence almost no reviews were written even though the option was there. The increase starts around 2005 and continues slowly until 2012. In 2013 there is a sudden increase in the amounts.

The increase in reviews could of course also be due to some internal changes in how the reviews are promoted or whether Amazon encourages people to write a review or not.  The general growth of online reviews as a discipline might also have made consumers more familiar with it and interested in writing their own review. A third explanation could be that Amazon have removed old data or some data is missing, however, we have no way to verify that this is the case.

To understand whether this is a global trend or perhaps one or more subcategories of Electronics that leads the the trend, we have looked at the amounts of reviews per subcategory. We notice that they all follow the same trend, although at different scales depending on the number of products they contain.

![Category breakdown number of reviews](/ada2017/images/Categories_number_reviews.png)


# Discovering seasons
We have already mentioned how the increase in sales during the christmas season of 2016 was quite tremendous and therefore an interesting question to ask is whether this also means an increase in reviews and whether this trend is a regular occurence?

To answer this question we look at the time series decomposition of the data.This decomposes the data into a trend component, a seasonal component and a residual. The latter is the variation in the number of reviews that cannot be modeled by the former two components.

![Seasonal Decomposition](/ada2017/images/3_seasonal_decomposition.png)

The decomposition is only done on the time period from 2007 to 2011, since the jump in the number of reviews after that is too large to be captured by the model and the years before that have to little data to yield interesting results. Looking at the seasonal component, we see a clear spike right around every new year fitting surprisingly well with the Christmas season. Even though 2012 and 2013 are not taken into account in this plot it should still be noted that we can observe the same phenomena for this year.

Below we can see how the monthly mean of the number of reviews varies. While 2013 and 2014 have a lot higher means than the other years, the trend does persist, and we can see clear spikes in January and December. While it isn’t to the extent that sales did, we conjecture that this could be attributed to the fact people can’t write reviews for gifts they gave or received.

<iframe width="100%" height="400" src="/ada2017/images/2_number.html" frameborder="0"></iframe>

We tried to investigate whether there is another form of seasonality left in the residual component, a weekly one for example. Do people write more reviews on the weekend perhaps? Starting from the hypothesis that there is a 7-day period in the series, we estimated weekly trends. 

![Weekly patterns](/ada2017/images/4_zoom_weekly_pattern.png)

Here it seems like the customers prefer to review their new products during the weekdays. Clearly less reviews are written on Saturday and Sunday, and Thursday seems to be the preferred day of the week for writing reviews.

# Have the reviewers become lazy?
An interesting pattern that we notice in the data is the evolution of the length of the reviews. 
It seems that the average daily length of the reviews tends to be longer during the years 2008-2012 compared to the years 2013-2014. Before 2008 there were so few reviews that the variance is huge and we cannot say a lot about that period.

<iframe width="100%" height="400" src="/ada2017/images/6_Length_reviews.html" frameborder="0"></iframe>

We observe a drastic drop in the length of reviews that occurs at the end of 2012. This is not as easy to explain. We tried to examine whether this could be due to some kind of restriction from Amazon, but that does not seem to be the case, as we still have the very long reviews in after 2012.

![box](/ada2017/images/box2.PNG)





### Plot 7:
![Sentiment Analysis](/ada2017/images/7_sentiment_scores.png)

### Plot 8:
<iframe width="100%" height="400" src="/ada2017/images/8_Overall_evolution.html" frameborder="0"></iframe>

### Plot 9:
![Categorical Sentiment Analysis](/ada2017/images/sentiment.PNG)

### Plot 10:
![Vairable Distribution](/ada2017/images/distribution_Variables.png)

### Plot 11:
![Categorical Distribution](/ada2017/images/distribution_across_categories.png)

### Plot 12:
![Overall Distribution](/ada2017/images/distribution_overall.png)










The amount of reviews written on Amazon is of course a different thing than the amount of sales, however, we did suspect that a the impressive trend in the growth of Amazons marketshare could naturally be expected to have a co 
The first step of our project was to visualize the number of reviews from 1996 to 2014. 
this is a good indicator on how people’s use of  amazon reviews has evolved through the years.

We group the reviews according to the category of the corresponding product and we notice that they all follow the same trend , although at different scales depending on the number of products they contain.

