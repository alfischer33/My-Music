# My Music
An analysis run on my iTunes/Apple Music library to discover which artists I quantitatively enjoy the most
 

## Jupyter Notebook
In my jupyter notebook analysis using Python, I began with data taken directly from my itunes library, that included the following categories:
![df](mymusic_df.png)

After that, I created a function to aggregate stats by artist using a pivot table. I extracted a variety of measurements from the initial 
DataFrame, created mechanisms by which I could filter out songs by when they were added to my library or when the last time I'd listened to 
them was, and then created a variety of features that I thought would be useful in quantifying which artists were really capturing my attention
and affection. 

To give a details about a few of the things I did here: 

The plays per week gave me issue when being used as a metric for how frequently I listened to an artist's songs, because the songs most recently 
added had much higher values, with the small number of weeks in the denominator far outweighing the smaller number of plays in the numerator, 
since I listen to songs I've just added more frequently than old ones. This was making this statistic severely unbalanced towards artists with recently 
added songs, so I transformed the data to a more level distribution by adding 40 "empty" weeks to the calculation, then multiplying by a ratio of (6/5),
which brought songs added 200 weeks ago (a somewhat central point in my library) to the same value they had before the transformation, while decreasing
the value of songs added after that, and increasing the value of songs added before that.



## Tableau
Here is a dashboard I made in Tableau from my music data, giving the options to filter by songs last played within a certain time frame,
date the songs were added to my library, the number of stars I'd given the songs, whether or not they'd been "loved", and by genre.

![My Music Tableau](TableauMyMusicDashboard.png)
