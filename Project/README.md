# Title
Amazin’ Amazon Trends

# Data Story: 
https://sourabhlal.github.io/ada2017/

# Abstract
The goal of our project is to study the Amazon products categories and analyze them through the reviews left by the consumers. This analysis will be conducted in three parts : 

* First, we will study the reviews (their frequency and their content ) and the product metadata and extract the relevant variables to describe each product category and to assess their popularity with the customers.

* Secondly, we will study the influence of cyclical events ( holidays, seasons …) on buying habits. We could visualize our results on  a yearly calendar showing the peak periods for each category.

* Finally, we will investigate the influence of important events (financial crisis, natural disasters…) on the evolution of each category through the years, the lifespan of their products and their popularity. At the end of our analysis, we should be able to visualize our results on an interactive timeline.

# Research questions
* How have large events in society affected both the amount of reviews written or the sentiment of the reviews?

* How are the amount of reviews related to sales and revenues of Amazon?

* Can we detect temporal buying trends: e.g. do people buy more things around christmas, and does the type of thing they buy change?

* Can we predict the time of the year based on what people are reviewing?
	
* Does the time of the year affect how customers are reviewing, e.g. the rating and the sentiment?

* Is it possible to detect certain patterns of reviews based on the time of the day?

# Dataset

The primary dataset that we would like to use is the [Amazon Review Dataset](http://jmcauley.ucsd.edu/data/amazon/). This dataset contains reviews of products sold on Amazon spanning a time period from May 1996 to July 2014. Additionally, the dataset also contains metadata about each product, and an extension to the database has visuals (images of the products).

### Dataset Size

There are multiple configurations of the dataset that will be useful for our project, and each one has a different size depending on what we want to use if for:

* Raw review data:
  * 20GB
  * 142.8 million review
  * All the data

* Cleaned review data: 
  * 18GB
  * 83.68 million reviews.
  * Removed duplicate reviews
  * Two versions: sorted by user, and sorted by product

* 5-core data:
  * 9.9GB
  * 41.13 million reviews
  * Only contains reviews for products with 5 or more reviews, or by reviewers with 5 or more reviews.

For each of the above types of datasets, there is a breakdown available by category of varying size. There are other variations of the dataset too, but they will not be of use for our project.

### Dataset Structure/Format

* Review Dataset
  * Reviewer ID
  * Product ID
  * Reviewer Name
  * Helpfulness Rating of review
  * Text in review
  * Rating given
  * Summary/Title of review
  * Review time
  * Review date
* Product Metadata Dataset
  * Product ID
  * Product title
  * Price of product
  * Image of product
  * List of products also viewed
  * List of products also bought
  * List of products bought together
  * List of products bought after viewing
  * List of categories the product belongs to
  * Sales rank of product within each category
* Visual features dataset (binary)
  * productID followed by visual data	

We would like to process this dataset by arranging reviews temporally, and breakdown the data based on year/month/day and other similar temporal features.

We would like to enrich this dataset by looking at external events, for which we will consider using either the Wikidata or UCDP database. However this is something we will decide on later.


# A list of internal milestones up until project milestone 2
![Gantt Chart](https://github.com/sourabhlal/ada2017/blob/master/Project/Images/Gantt.JPG "Gantt Chart")

To illustrate the entire project plan we have made a Gantt diagram showing the headlines of all tasks that needs to be completed and at what time we expect to be working on them. All big milestones are marked with a red line. For now we will focus on the time until the next Milestone 2 and therefore this time period and the tasks related has been highlighted.

As we see on the diagram the main task (including internal milestones) until then are:

**Data Collection:** We need to fully understand the dataset and have access to it so that all members are able to work efficiently with it. Preferably this will be done around mid November.

**Descriptive Analysis:** Here we will look at the attributes of the dataset and compute statistics for the whole dataset and aggregated by categories. This has to be completed by 28th of November.

**Deeper analysis:** This part will begin mid November with deciding more precisely which methods will be used and by the end of November this task should have been somewhat explored.

**Jupyter Notebook:** The Jupyter Notebook will be created soon and finished code will be added to it after experimenting elsewhere. The code for the data collection and descriptive statistics should be added along with descriptions before end of November.

# Questions for TAs
* How specific does our story have to be (only one category or full dataset)
* Is it necessary to enrich our dataset with other data, or can we work with just the current dataset? For example, when tackling one-off events, we can add them up from another dataset, or add key events that we know about (e.g. hurricane katrina, 9/11, etc)

# Distribution of the tasks : 
Most of the tasks were carried out in parallel by the three of us and the results were discussed together.Other then that we did the following :

- **Sonia Alouini** : Data preprocessing + Timelines analysis  + Correlation plots
- **Charlotte Theisen**: Data preprocessing + MetaData processing + Website creation
- **Sourabh Lal**: Data Exploration + Sentiment Analysis (IBM and Vader) and Visualizations + Website creation 

**Presentation** : Sourabh Lal
