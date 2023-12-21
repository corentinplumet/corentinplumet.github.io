---
layout: default
---

# Lockdown and overall video games interest: a relation ?

In this part, we are going to discuss about the relation (or not) between the different type of lockdown around the world, and their possible impact on people's interest for video games.

To measure people's interest towards video games we will use the Wikipedia pageviews. Indeed, Wikipedia being the largest and most popular encyclopedia in the world, the pageviews of the website are a good metric to know what people are searching for and thus, are interested in.

To categorize the lockdown of diiferent country, we will use the reported mobility of google from January 2020 until August 2020. We state that the highest the decrease in mobility, the more strict the lockdown is. 

The countries with which we chose to do the analysis speak a language that is mainly speaken only in this country. This way we can link accurately Wikipedia page written in a specific language to a specific country. For example, we can assume that only swedish people are using wikipedia pages written in swedish.

## Mobility pattern

The plot below present the moblity evolution between the 2020-02-15 and the 2020-08-25, taking as 0 the mobility on the first day of the interval. We got data for France, Denmark, Germany, Italy, Netehrlands, Norway, Serbia, Sweden, South Korea, Catalonia (Barcelona), Finland and Japan. Also the 2 red lines represent the 2 dates were we can statistically consider a mobility drop and then a normality comeback.   

<iframe
  src="output.html"
  height="750"
  width="700"
  style="border:none;"
></iframe>

For most of the countries, the lockdown is really a break in the mobility pattern. Mobility in france for example, decreases by around 70% after the beginning of the lockdown. However, for some countries like Japan the decrease is less likely noticeable. This disparity in moblity change motivate the clustering of countries. If we want to see if the lockdown had an impact on the attention towards videogames, we can't consider all the countries has one group but we need to group them according to their "lockdown Intensity".

![Branching](countries_cluster.png)

There are 3 clear tendancies with very similar pattern. One group, had a very restrictive lockdown with a minium mobility around 70%-80% of what it was before the lockdown. The second group, had a restrictive lockdown with a minium mobility around 45% of what it was before the lockdown. The last group also experienced a lockdown but it was an unrestrictive one, leading to a small decrease in total mobility. 

## Attention towards video games

Now that we have grouped the countries according to their lockdown intensity, we can get the measure of the attention shift towards video games.

During the lockdown, people were most od the time at home, and thus got more free time than usual, which translate into a higher traffic on the wikipedia website overall. Thus, we are not using the absolute value of the pageviews, but the percentage of views on video games related pages amongst all the wikipedia traffic.

The following figure shows therefore the percentage of wikipedia pageviews related to video games in the same countries we have in the mobility part.

![Branching](pageviews.png)

We can see that after the mobility drop, it seems that certain countries experienced a rise in the attention toward video games. To have a better understanding of these curves, we can group them following the clustering we did previously in the mobility context.

![Branching](pageviews_cluster.png)

## Correlation ?

We just saw in the previous part that there might be an increase in the proportion of views for video games related paages after the mobility drop. To get a representation of this increase, we can plot the relative proportion increase between the pre-lockdown and post-lockdown period.

![Branching](change_in_attention_plot.png)

We can see that there is clear tendancy of increase in attention toward video games during the lockdown period as all the countries, except for Finland, experienced an increase in percentage of pageviews related to video games amongst all the wikipedia pageviews. Also, with this graph it's clear that the intensity of lockdown had an impact on the attention shift towards videogames. Indeed, the countries with an unrestrive lockdown (yellow: Sweden, Korea, Japan) experienced a small increase in attention compared to the 2 groups with a restrictive and very restrictive lockdown. It also seems like the red group (very restrictive lockdown) had a larger increase compared to the orange group (restrictive lockdown), but the difference is less likely to be significant than with the unrestictrive lockdown.

But is really this attention shift towards video games correlated to the mobility of people inside this country ? To answer this question, we can plot the correlation coefficient between the mobility time series and the wikipedia pegeviews time series. We get this plot:

![Branching](correlation_coeff_plot.png)

According to this graph, the intensity of lockdown doesn't have an impact on the correlation value. Indeed, Japn and Korea that belongs to the group of unrestrictive lockdown have a high negative correlation that is statistically significant, as the the countries that belongs to the other groups.

What is interesting with this graph is that we can note that the countries with a very low and not significant correlation are the Norway, Sweden, Finland and Denmark, which are all the Scandinavian countries. It means that even though these countries experienced an increase of the video games page views percentage during the lockdown period (Norway and Denmark especially because Sweden experienced a very low increase and Finaland no increase at all) it's not related to the mobility decrease. For Denmark and Norway, the increase in views on wikipedia pages related to video games during the lockdown is simply part of an overall increase, not necessarily linked to the drop in moblity. That's why we notice an increase of videogames related pageviews during the lockdown but no correlation with the drop in mobility.

# Conclusion

Therefore, overall, 3 conclusions can be drawn from this analysis. First, the mobility decrease amount, and so the intensity of lockdown is indeed a factor that drives the attention shift towards videogames: the less the people are moving, the more they spend time playing videogames and doing research about it. The second statement is an extension of the first one in the sense that the mobility decrease intensity doesn't impact its correlation with the attention shift. A mobility decrease, no metter its importance, will lead to a proportionnal increase in video games interest. The third statement is an exception for the Scandinavian countries. These countries may have experienced an increase in videogames research proportionnally speaking, but it's not related to the mobility. 

However, we need to be aware of the limit of these conclusions. What we found is a correlation relation, not causation one. It means that even if it seems like the drop in mobility may be the cause of the attention increase towards video games, maybe an other factor linked to the covid-19 that drives the increase in attention.