*What’s the Vibe?*

The purpose of our project was to create a model that could analyze whether a song should be classified as “happy” or “sad”, and then use that model to analyze how the general sentiment of popular music in the United States has trended over the past 20 years. With depressions, pandemics, record economic expansions and tremendous social change, the United States has experienced some of the most unique events in its economic and social history over the past 20 years. Throughout this period, we want to investigate whether songs have become happier, sadder, or trended up and down along with the events playing out on the national stage. 

In order to do so, we began by collecting a dataset of happy and a dataset of sad songs across different genres in order to train our random forest classification model. We created these datasets by pulling user-created playlists from the Spotify API that contained either happy or sad songs. It is important to note that these songs were not objectively “happy” or “sad”, but instead reflected Spotify users’ preferences for what they found to be “happy” or “sad”. In choosing to select songs in this format and by aggregating 28 playlists together for a total of ~2,000 songs, we were able to create a dataset that reflected a more general definition of a “sad” song that reflected our biases as little as possible. In addition, diversity of genre was important in order to create a model that was robust to changes in the popularity of genres over different time periods. For example, hip hop music is the dominant genre nowadays, but in the early 2000s the charts were dominated by pop punk songs. From our dataset, we selected four features on which to train the model: tempo, valence, danceability, and mode (key). Training the random forest classification model off these songs, we achieved a test accuracy rate of 75%. 
After building the random forest model, we wanted to use it to analyze how sentiment of popular songs has trended over the past 20 years. We used the billboard hot 100 charts of each year since 2000 as a proxy for popular songs in that year. We compiled that data by pulling billboard hot 100 playlists of each year from Spotify and fed them into the model. A graphical depiction of our results can be seen in sentiment.png. 

As you can see, there is a clear trend of songs getting sadder over the past 20 years. This might be related to the rising depression rates that we have witnessed over the same time period as social media has become more prevalent. Interestingly, we see the strongest rebound in sentiment during the recovery from the great recession. This might reflect the general positive notion at the time after coming from such a difficult period of economic hardship. 
This study could have been significantly improved had we had access to lyrics data in order to run a sentiment analysis of our training dataset that would factor into our model. However, we discovered that there were copyright issues with scraping lyrics and thus decided to abandon the idea on an ethical basis. In addition, the study could be further improved by creating more classification groups besides happy and sad; after all, it is obvious that not all songs fit neatly into one category or the other! 

An ethical dilemma that we confronted while conducting these analyses builds off of the latter suggestion for improvement in that art is not meant to be classified into boxes and neatly labelled, which is inherently what a machine learning algorithm does. There is so much nuance, passion, and energy that is lost when we assign a label of merely “happy” or “sad” to a song. While this analysis is certainly fun, it is by no means a definitive summary of all the diverse feelings and emotions that listeners experienced when hearing these songs at the peak of their popularity. 

Citations:
Charlie Thompson, Daniel Antal, Josiah Parry, Donal Phipps and Tom Wolff (2021). spotifyr: R Wrapper for the ‘Spotify’ Web API. R package 
version 2.2.3. https://CRAN.R-project.org/package=spotifyr

“Decade in Review: 2010s Was the Decade of the Bull.” https://money.usnews.com/investing/stock-market-news/articles/2019-11-29/decade-in-review-2010s-was-the-decade-of-the-bull 

Garrett Grolemund, Hadley Wickham (2011). Dates and Times Made Easy with lubridate. Journal of Statistical Software, 40(3), 1-25. URL 
https://www.jstatsoft.org/v40/i03/ 

Hidaka, Brandon H. “Depression as a Disease of Modernity: Explanations for Increasing Prevalence.” Journal of Affective Disorders, vol. 140, no. 3, 2012, pp. 205–214., https://doi.org/10.1016/j.jad.2011.12.036. 

Kuhn et al., (2020). Tidymodels: a collection of packages for modeling and machine learning using tidyverse principles. 
https://www.tidymodels.org 

Paul, Crystal (2019). “A Look Back at 10 of the Biggest Social Movements of the 2010s, and How They Shaped Seattle.” The Seattle Times, The Seattle Times Company, https://www.seattletimes.com/life/a-look-back-at-10-of-the-biggest-social-movements-of-the-2010s-and-how-they-shaped-seattle/ 

Rich, Robert. “The Great Recession.” Federal Reserve History, https://www.federalreservehistory.org/essays/great-recession-of-200709 

Taylor, Derrick Bryson (2020). “A Timeline of the Coronavirus Pandemic.” The New York Times, The New York Times, 
https://www.nytimes.com/article/coronavirus-timeline.html

Wickham et al., (2019). Welcome to the tidyverse. Journal of Open Source Software, 4(43), 1686, https://doi.org/10.21105/joss.01686 Yihui Xie (2021). knitr: A General-Purpose Package for Dynamic Report Generation in R. R package version 1.33. 
