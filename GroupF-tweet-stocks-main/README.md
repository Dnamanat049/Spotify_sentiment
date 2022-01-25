#Feel(ings) of the Beat

Project Outline

Group Members:
Mohsin Ali Butt
Project Manager & Director of Research

Tianna Couch
Facilitator & Reporter

Deen Amanat
Task Manager & Director of Computation


Question: Over the past 60 years, how has the ratio of happy:sad songs trended in the billboard hot 100? 

Purpose: We believe that people’s choice of music is based on how they are feeling at the time. We want to develop a model that is able to classify songs that people are listening to into the two categories: 1) “Happy” and 2) Sad. We then apply that model on the Top Billboard Songs from different time periods to see how the type of music is varying over time. For example, what is the type of music people were listening to in 2020-2021 and how does that compare to previous years?

The challenge is to measure happiness or the sadness of a song. To build our model, we use the following Variables:

1) Song Title — our ID Variable
2) Sentiment Score —  This will be calculated through a Sentimental Analysis run on the song data gathered through a Spotify API. The idea is to classify the songs into “Happy” or “Sad” based on the sentiment of the words in the lyrics of the song.  
3) BPM — beats per minute. Higher BPM makes it likely that its a happy song. 
4) Chords — Research has shown that regardless of musical training, culture or subject age, major chords are evaluated as “bright and happy”, and minor chords as “dark and sad”.

Model Building Framework:

Get 100 Top Happy Songs + 100 Top Sad Songs from Popular Spotify Playlists
Build Random Forest Model to Classify Sad or Happy using the variables described above.
Label Top Hot 100 Billboard songs as Happy or Sad
Plot # of happy songs by year (data viz.)

To account for variation in the definition of happy and songs, we will create 3 models:

1) A random forest model with all variables given above. 
2) One model would be isolating just the sentimental score. 
3) One model would be excluding the sentimental score to account for the fact that songs can also be classified into “happy” or “sad” based on the beat rather than the lyrical content. 
