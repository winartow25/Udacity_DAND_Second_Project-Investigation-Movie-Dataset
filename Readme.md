
# Project: Investigate a Dataset - TMDb Movie Dataset

This data set contains information about 10,000 movies collected from The Movie Database (TMDb), including user ratings and revenue.

What can we say about the success of a movie before it is released? Are there certain companies (Pixar?) that have found a consistent formula? Given that major films costing over $100 million to produce can still flop, this question is more important than ever to the industry. Film aficionados might have different interests. Can we predict which films will be highly rated, whether or not they are a commercial success?

This project will investigate the dataset to gain some insights and recommendation

<a id='intro'></a>
## Introduction
#### Questions that can be addressed using this dataset:

Q1: How is the popularity of movies over the years?

Q2: What are recommendation movie's properties to achieve commercial success?
- Investigation on which genre that has become the most commercial successful movie
- Investigation on which cast that has become the most commercial successful movie
- Investigation on which production company that has become the most commercial successful movie
- Investigation on which director that has become the most commercial successful movie
- Investigation on what budget level is required to become the most commercial successful movie

Q3: What are Top 15 favourite movies over the years?

Q4: Which Genres is the most popular among the generations?

<a id='wrangling'></a>
## Data Wrangling

Based on the Data Wrangling, there are several steps that need to be done in Data Cleaning Step:

1. Drop the unnecessary columns which are not related with question, such as: imdb_id, budget, revenue, homepage, tagline, overview, keywords

2. Drop the missing value 

3. Drop the duplicate value

4. Replace zero value with NaN value

### <a id='conclusions'></a>
## Conclusions

#### Q1: How is the popularity of movies over the years?
In this research question, I am investigating the popularity of movies from 1960’s until 2000’s by averaging the popularity score in each year. Based on the chart, it shows a positive trend which popularity of movies is increasing along the years. An interesting finding in this research question is there is a spike of increment on 2010 onwards. I believe this is due to the growth of internet that has been drastically increase after 2000. As generally known, several streaming platforms entered the industry after 2000’s such as Netflix, Amazon Prime Video, Youtube, Hulu, and others. Those platforms lead viewers have high accessibility to watch the movie. This finding indicates that film industry is growing exponentially along with the growth of internet in nowadays.

#### Q2: Findings Analysis - What are recommendation movie's properties to achieve commercial success?
In this research question, the scope of investigation is narrowed down only for commercial success movie. Since as we know, there are numbers of failed movie even though it was produced with high budget and with famous casts and director. Therefore, the intention to conduct this investigation is to be able provide a recommendation what kind of movie’s properties that the industry need to consider before they produce a movie in order to be a commercial success. 

In this project, revenue and budget with adjusment value were used. Considering the inflation rate is critically important since we are investigating profit from the data in 1960's untill 2000's.
Determination of commercial success is based on the profit by subtracting revenue with budget. Then I classify the profit into 4 subcategories, such as low (0-25%), medium (25-50%), moderately high (50 – 75%) and high (>75%).  This research question is only focused on high profit movies (75th Percentile). By using query, we can have the desired dataframe. Based on the new dataframe, the investigation can be done for each movie’s properties such production company, cast, genre, director, and budget level. Since the unique value in production movie, cast, director, and genres are repetitive in each row, we need to gather the value based on the number of appearances in the whole dataset. By only selecting top 5 value of each movie properties, the recommendation can be used to produce a commercial success movie in the future. 

Those recommended movie's properties are:

**1.Recommended Production Movie:**
- Warner Bros
- Universal Pictures
- Paramount Pictures
- Twentieth Century Fox Film Corp
- Walt Disney Pictures

**2.Recommended Cast:**
- Tom Cruise 
- Tom Hanks
- Brad Pitt
- Adam Sandler
- Sylvester Stallone

**3.Recommended Genre:**
- Action
- Comedy
- Drama
- Adventure 
- Thriller

**4.Recommended Director:**
- Steve Spielberg
- Robert Zemeckis
- Clint Eastwood
- Ron Howard
- Michael Bay

**5.Recommended Movie budget:**
- To have a commercial successfull movie, to production movie is suggested to have a high budget with an average of $ 111,864,878



#### Q3: Findings Analysis - What are Top 15 favourite movies over the years?

In this research question, we are interested to investigate the most favorite movies based on the viewer’s vote. Since the number of vote for each movie is not equivalent, we can’t take the vote average to determine the favorite movie. Based on the IMDb, the right method to calculate favorite movie is by using weighted rating (Bayesian Method). Based on this weighted average, the top 15 favorite movies can be investigated.

#### Q4: Findings Analysis - Which Genres is the most popular among the generations?
This research question aims to support a recommendation of recommended genre in the second research question. Since the recommended genre based on high profit movies was done based on the whole generation, this research question is testing the consistency of those 5 recommended genres through generation by generation. According the given data, there are 4 generation been set. The finding shows that **action, drama, comedy, adventure, and thriller** are the most frequent genres that appear as the most commercial success throughout the generations.

### Limitation
1.Revenue and Budget Data Quality
- Since there are numerous zero data, we can’t remove it by considering the quality of dataset. This recommendation is not quite precise since almost 50% of the value is filled by Nan value, thus it tends to create a bias.

2.Keywords
- This project is not using keywords data as a research instrument due to limitation of researcher’s knowledge. Further research will be recommended to use keywords data as resourceful instrument to create a prediction for machine learning. 

3.Recommendation Time Frame
- The accuracy of the recommendation based on the several movie's properties such as cast and director could be affected by age factor



```python

```
