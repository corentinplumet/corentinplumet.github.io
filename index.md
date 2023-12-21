---
layout: home
title: Covid-eo Games
subtitle: Analysis on the impact of the Covid-19 lockdown on the interest towards video games
---

Have you ever wondered if the COVID-19 had more impact on you than just the sudden urge to become an expert in Zoom? Or did you spend the most of your time training to become the last survivor on the fortnite Island? If the answer is yes this article is for you because we are going to reveal the mysterious connection between the pandemic and the the video games Industry. The mission is to understand the relationship between global lockdown experiences, varying in intensity, and the consequent shifts in attention towards video games. Our study aims not only to decrypt the impact of lockdown measures but also to discern whether distinct genres of games underwent differential changes during this period.

This article contains lots interactive visualizations. Don't forget to use them to be sure to understand all the important informations. Let's get started, it's about to get real (or at least virtually real)!

# Lockdown and overall video games interest: a relation ?

So let's start by discussing about the relation (or not) between the different type of lockdown around the world, and their possible impact on people's interest for video games. 

To measure people's interest towards video games we will use the Wikipedia pageviews. Indeed, Wikipedia being the largest and most popular encyclopedia in the world, the pageviews of the website are a good metric to know what people are searching for and thus, are interested in.

To categorize the lockdown of diiferent country, we will use the reported mobility of google from January 2020 until August 2020.  It's like the GPS for lockdown strictness – the bigger the dip in people moving around, the tighter the lockdown grip. 

Our study focus extends to countries where a singular language predominantly prevails. This way we can link accurately Wikipedia page written in a specific language to a specific country. For example, we can assume that only swedish people are using wikipedia pages written in swedish.

## Mobility pattern

The plot below presents the moblity evolution between the 2020-02-15 and the 2020-08-25, taking as 0 the mobility on the first day of the interval. We got data for France, Denmark, Germany, Italy, Netehrlands, Norway, Serbia, Sweden, South Korea, Catalonia (Barcelona), Finland and Japan. Also the 2 red lines represent the 2 dates were we can statistically consider a mobility drop and then a normality comeback.   

<div align="center">
<iframe
  src="/assets/img/output.html"
  height = 825
  width = 800
  style="border:none;"
></iframe>
</div>

For most of the countries, the lockdown is a real break in the mobility pattern. Mobility in france for example, decreases by around 70% after the beginning of the lockdown. However, for some countries like Japan the decrease is less noticeable. This disparity in moblity change motivates the clustering of countries. If we want to see if the lockdown had an impact on the attention towards videogames, we can't consider all the countries has one group but we need to group them according to their "lockdown Intensity".

![Branching](/assets/img/countries_cluster.png)

There are 3 clear tendancies with very similar pattern. One group, had a very restrictive lockdown with a minium mobility around 70%-80% of what it was before the lockdown. The second group, had a restrictive lockdown with a minium mobility around 45% of what it was before the lockdown. The last group also experienced a lockdown but it was an unrestrictive one, leading to a small decrease in total mobility. 

## Attention towards video games

Now that we have grouped the countries according to their lockdown intensity, we can get the measure of the attention shift towards video games.

During the lockdown, people were most od the time at home, and thus got more free time than usual, which translate into a higher traffic on the wikipedia website overall. Thus, we are not using the absolute value of the pageviews, but the percentage of views on video games related pages amongst all the wikipedia traffic.

The following figure shows therefore the percentage of wikipedia pageviews related to video games in the same countries we have in the mobility part.

![Branching](/assets/img/pageviews.png)

We can see that after the mobility drop, it seems that certain countries experienced a rise in the attention toward video games. To have a better understanding of these curves, we can group them following the clustering we did previously in the mobility context.

![Branching](/assets/img/pageviews_cluster.png)

## Correlation ?

We just saw in the previous part that there might be an increase in the proportion of views for video games related paages after the mobility drop. To get a representation of this increase, we can plot the relative proportion increase between the pre-lockdown and post-lockdown period.

![Branching](/assets/img/change_in_attention_plot.png)

We can see that there is clear tendancy of increase in attention toward video games during the lockdown period as all the countries, except for Finland, experienced an increase in percentage of pageviews related to video games amongst all the wikipedia pageviews. Also, with this graph it's clear that the intensity of lockdown had an impact on the attention shift towards videogames. Indeed, the countries with an unrestrive lockdown (yellow: Sweden, Korea, Japan) experienced a small increase in attention compared to the 2 groups with a restrictive and very restrictive lockdown. It also seems like the red group (very restrictive lockdown) had a larger increase compared to the orange group (restrictive lockdown), but the difference is less likely to be significant than with the unrestictrive lockdown.

But is really this attention shift towards video games correlated to the mobility of people inside this country ? To answer this question, we can plot the correlation coefficient between the mobility time series and the wikipedia pegeviews time series. We get this plot:

![Branching](/assets/img/correlation_coeff_plot.png)

According to this graph, the intensity of lockdown doesn't have an impact on the correlation value. Indeed, Japn and Korea that belongs to the group of unrestrictive lockdown have a high negative correlation that is statistically significant, as the the countries that belongs to the other groups.

What is interesting with this graph is that we can note that the countries with a very low and not significant correlation are the Norway, Sweden, Finland and Denmark, which are all the Scandinavian countries. It means that even though these countries experienced an increase of the video games page views percentage during the lockdown period (Norway and Denmark especially because Sweden experienced a very low increase and Finaland no increase at all) it's not related to the mobility decrease. For Denmark and Norway, the increase in views on wikipedia pages related to video games during the lockdown is simply part of an overall increase, not necessarily linked to the drop in moblity. That's why we notice an increase of videogames related pageviews during the lockdown but no correlation with the drop in mobility.

Therefore, overall, 3 conclusions can be drawn from this analysis. First, the mobility decrease amount, and so the intensity of lockdown is indeed a factor that drives the attention shift towards videogames: the less the people are moving, the more they spend time playing videogames and doing research about it. The second statement is an extension of the first one in the sense that the mobility decrease intensity doesn't impact its correlation with the attention shift. A mobility decrease, no metter its importance, will lead to a proportionnal increase in video games interest. The third statement is an exception for the Scandinavian countries. These countries may have experienced an increase in videogames research proportionnally speaking, but it's not related to the mobility. 

However, we need to be aware of the limit of these conclusions. What we found is a correlation relation, not causation one. It means that even if it seems like the drop in mobility may be the cause of the attention increase towards video games, maybe an other factor linked to the covid-19 that drives the increase in attention.

# What about specific types of video games ? 

Now that we have seen what is the overall relationship between videogames interest and the mobility decrease, let's get specific and go deeper into the video games part of the analysis. There are lots of type of video games and even though they are, as a group, correlated with the mobility not all of them might share the same link with it. By assigning each page to a video game genre, we can try to see what are the trends amongst all the types. The analysis is performed on one country of each lockdown intensity to capture the lockdown effect in the analysis.

###	France – Popularity Boosts Strong in Games

![Branching](/assets/img/france_type.png)
 
The French government implemented a strict lockdown on March 17, 2020, initially planned for 15 days but extended to 55 days until May 11, 2020. As we saw before, the mobility disruption led to increased gaming popularity. During the lockdown, game pageviews surged, but post-intervention, they returned to pre-COVID levels. When considering game genre, we can see that during the lockdown, the vidoe games about Action, Adult, Adventure, Horror, Puzzle, RPG, Sports and Strategy have attracted the most increase. We also note that the Horror games actually remain more popular than pre-lockdown time after the intervention has been lifted, while other games are back to normal popularity just like the pre-covid time. We can specifically look into games about Sports and Multiplayer/Online, after the society is back to normal, the popularities of these two genres of games actually decline, which is reasonable since people tends to play sports offline and meet offline to hang out and have fun.

### Germany – Less Restrictive, Less Interest in Games

Compared to its bordering country France, Germany has less restriction on the free move of the people, while more emphasis on the social distance and mask mandate, giving people more chances to go out. The difference between the French and German government has resulted to different mobility disruption, leading to less mobility decrease in Germany. Thus people actually spend less time at home and play games, and there is less increase in the pageviews of games in German-version Wikipedia.

![Branching](/assets/img/germany_type.png)

Compared to its bordering country France, Germany has less restriction on the free move of the people, leading to less mobility decrease in Germany. Thus people actually spend less time at home and play games, and there is less increase in the pageviews of games in German-version Wikipedia. Overall, there is minor increased popularity in games, but it is obviously milder than that in France. Regarding to different game genres, RPG, Stimulation, Sports and Strategy enjoy the most gain from the lockdown, but if you compared it to other same genres in France, it is definitely a smaller gain.

### Japan – We Play Games for Passion

![Branching](/assets/img/japan_type.png)

Japan didn't suffer from first wave of the pandemic, leaving thus the mobility disruption at the minimum level. In this case, people enjoy more freedom moving around and the mobility data seems much more normal compared to France and Germany. In this case, the popularity in games is not forcefully increased due to the intervention from the government. However, there are still some minor gains in the game of Multiplayer/Online, Puzzle, Sports and Strategy. And the popularity seems to last longer than expected after the intervention is over. We believe there is an explanation that since the mobility is not changed sharply, the popularity in the games can last longer since people are not "forced" to play games, instead they are actually like video games. Therefore, there is some evidence that the game industry in Japan actually benefits from covid in a longer time span.
