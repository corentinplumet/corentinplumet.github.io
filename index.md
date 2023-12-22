---
layout: home
title: Covid-eo Games
subtitle: Analysis of the Covid-19 lockdown impact on the interest towards video games
---

Have you ever wondered if the COVID-19 had more impact on you than just the sudden urge to become an expert in Zoom? Or did you spend the most of your time training to become the last survivor on the fortnite Island? If the answer is yes this article is for you because we are going to reveal the mysterious connection between the pandemic and the video games industry. The mission is to understand the relationship between global lockdown experiences, varying in intensity, and the consequent shifts in attention towards video games. Our study aims not only to decrypt the impact of lockdown measures but also to discern whether distinct genres of games underwent differential changes during this period.

This article contains many interactive visualizations. Don't forget to use them to be sure to understand all the important informations. Let's get started, it's about to get real (or at least virtually real)!

# Introduction

To introduce the subject well, we first need to get an idea of what type of games there are and their distribution in the wikipedia database. By parsing down all the game pages from the Wikipedia database and categorized them into several main game genres, we can get the overview we need.

<iframe
  src="/assets/img/game genre count.html"
  width = 900
  height = 550
  style="border:none;"
></iframe>

The most prevalent genre in the dataset is "Action”. This suggests that action games are highly popular or widely produced. The dataset encompasses a diverse range of genres, including sports, role-playing games (RPG), adventure, science fiction, puzzle, strategy, simulation, and more. This diversity indicates a variety of gaming preferences and interests, which aligns with the current development of the worldwide game industry.

Also, the following graph plots for each day the total views of pages related to the same main genre depending on the language. From this graph we can already see trends on the wikipedia traffic, depending on the periods, languages and themes. Do not hesitate to play a lot with this graph!

<div align="center">
<iframe
  src="/assets/img/pageviews.html"
  width = 800
  height = 650
  style="border:none;"
></iframe>
</div>

# Lockdown and overall video games interest: a relation ?

In this part, we are going to discuss the possinle relation between the different type of lockdown around the world, and their impact on people's interest for video games. 

To measure people's interest towards video games we will use the Wikipedia pageviews. Indeed, Wikipedia being the largest and most popular encyclopedia in the world, the pageviews of the website are a good metric to know what people are searching for and thus, are interested in.

To categorize the lockdown of different country, we will use the reported mobility of google from January 2020 until August 2020.  It's like the GPS for lockdown strictness – the bigger the dip in people moving around, the tighter the lockdown grip. 

Our study focus extends to countries where a singular language predominantly prevails. This way we can link accurately Wikipedia page written in a specific language to a specific country. For example, we can assume that only swedish people are using wikipedia pages written in swedish.

## Mobility pattern

The plot below presents the moblity evolution between the 2020-02-15 and the 2020-08-25, taking as 0 the mobility on the first day of the interval. We got data for France, Denmark, Germany, Italy, Netehrlands, Norway, Serbia, Sweden, South Korea, Catalonia (Barcelona), Finland and Japan. The 2 red lines represent the 2 dates were we can statistically consider a mobility drop and then a normality comeback. These dates are really close to the beginning and ending of moblity restrictions (1 or 2 days away). Also, a smoothed curve of each mobility signal can be displayed by clicking on the button at the bottom of the plot.  

<div align="center">
<iframe
  src="/assets/img/output.html"
  height = 825
  width = 800
  style="border:none;"
></iframe>
</div>

For most of the countries, the lockdown is a real break in the mobility pattern. Mobility in France for example, decreases by around 70% after the beginning of the lockdown. However, for some countries like Japan the decrease is less noticeable. This disparity in moblity change motivates the clustering of countries. If we want to see if the lockdown had an impact on the attention towards videogames, we can't consider all the countries has one group but we need to group them according to their "lockdown Intensity".

![Branching](/assets/img/countries_cluster.png)

There are 3 clear tendancies with very similar pattern. One group, had a very restrictive lockdown with a minium mobility around 75% of what it was before the lockdown. The second group, had a restrictive lockdown with a minium mobility around 45% of what it was before the lockdown. The last group also experienced a lockdown but it was an unrestrictive one, leading to a small decrease in total mobility. 

## Attention towards video games

Now that we have grouped the countries according to their lockdown intensity, we can get the measure of the attention shift towards video games.

During the lockdown, people were most of the time at home, and thus had more free time than usual, which translates into a higher traffic on the wikipedia website overall. Thus, we are not using the absolute value of the pageviews, but the percentage of views on video games related pages amongst all the wikipedia traffic.

The following figure shows therefore the percentage of wikipedia pageviews related to video games for the same countries we have in the mobility part.

![Branching](/assets/img/pageviews.png)

We can see that after the mobility drop, it seems that certain countries experienced a rise in the attention towards video games. To have a better understanding of these curves, we can group them following the clustering we did previously in the mobility context.

![Branching](/assets/img/pageviews_cluster.png)

## Correlation ?

We just saw in the previous part that there might be an increase in the proportion of views for video games related pages after the mobility drop. To get a representation of this increase, we can plot the relative proportion increase between the pre-lockdown and post-lockdown period.

![Branching](/assets/img/medianpercentage.png)

We can see that there is a clear tendancy of increase in attention towards video games during the lockdown period as all the countries, except for Finland, experienced an increase in percentage of pageviews related to video games amongst all the wikipedia pageviews. Also, with this graph it's clear that the intensity of lockdown had an impact on the attention shift towards videogames. Indeed, the countries with an unrestrictive lockdown (yellow: Sweden, Korea, Japan) experienced a small increase in attention compared to the 2 groups with a restrictive and very restrictive lockdown. It also seems like the red group (very restrictive lockdown) had a larger increase compared to the orange group (restrictive lockdown), but the difference is less likely to be significant than with the unrestrictive lockdown.

<div align="center">
<iframe
  src="/assets/img/boxplot.html"
  width = 800
  height = 500
  style="border:none;"
></iframe>
</div>

The boxplot above gives us another distribution view of the attention shift. Thanks to the confidence interval of 95% percent, we can confirm our previous analysis. Indeed, we see that the "restrictive" group confidence intervals overlap with the 2 other, but the "very restrictive" group and "unrestrictive" group don't overllap. Also the overlap for the "restrictive" and "unrestrictive lockdown" are really small. We can note that the odd shape of the box (the confidence interval being larger than the 1st to 3rd quartile interval) is due to the small number of point in our samples.

But is really this attention shift towards video games correlated to the mobility of people? To answer this question, we can plot the correlation coefficient between the mobility time series and the wikipedia pageviews time series. We get this plot:

![Branching](/assets/img/correlation_coeff_plot.png)

According to this graph, the intensity of lockdown doesn't have an impact on the correlation value. Indeed, Japan and Korea which belong to the unrestrictive group have a high negative correlation that is statistically significant like the countries that belongs to the other groups.

What is interesting with this graph is that we can note that the countries with a very low and not significant correlation are Norway, Sweden, Finland and Denmark, which all are Scandinavian countries. It means that even though these countries experienced an increase of the video games page views percentage during the lockdown period (Norway and Denmark especially because Sweden experienced a very low increase and Finland no increase at all) it's not related to the mobility decrease. For Denmark and Norway, the increase in views on wikipedia pages related to video games during the lockdown is simply part of an overall increase, not necessarily linked to the drop in moblity. That's why we notice an increase of videogames related pageviews during the lockdown but no correlation with the drop in mobility.

Therefore, overall, 3 conclusions can be drawn from this analysis. First, the mobility decrease amount and the intensity of lockdown are indeed a factor that drives the attention shift towards video games: the less the people are moving, the more they spend time playing video games and doing research about it. The second statement is an extension of the first one, in the sense that the mobility decrease intensity doesn't impact its correlation with the attention shift. A mobility decrease, no matter its importance, will lead to a proportionnal increase in video games interest. The third statement is an exception for the Scandinavian countries. These countries may have experienced an increase in videogames research proportionnally speaking, but it's not related to the mobility. 

However, we need to be aware of the limit of these conclusions. What we found is a correlation relation, not causation one. It means that even if it seems like the drop in mobility may be the cause of the attention increase towards video games, maybe an other factor linked to the covid-19 that drives the increase in attention.

### The catalonian exception

But what about catalonia? We get very strange data for this region. We saw that there is a huge increase in the attention towards video games after the lockdown with the "change in proportion" plot. But also we saw a very strong positive correlation between the mobility and the video games interest. Does it mean that the catalans are more interested in video games when they are free to move? Let's take a look:

![Branching](/assets/img/catalonia.png)

We can see a strange effect. The mobility curve and the video games attention curve are closely following once the lockdown is effective. when the mobility dropped, the video games attention didn't change much but after that, it followed the evolution (rise) in mobility. That explains the strong positive correlation and the huge increase in attention between the lockdown.

# What about specific types of video games ? 

Now that we have seen what is the overall relationship between videogames interest and the mobility decrease, let's get specific and dive further in the video games part of the analysis. There are many type of video games and even though they are, as a group, correlated with the mobility not all of them might share the same link with it. By assigning each page to a video game genre, we can try to see what are the trends amongst all the types. The following part analyse French, Japanese, Italian and German growth in pageviews across gaming categories. These four nations are becoming our focal point due to their distinct lockdown measures, geographic placement, and cultural differences, offering a rich ground for analysis.

## Overview

###	France – Popularity Boosts Strong in Games

<div align="center">
<iframe
  src="/assets/img/france.html"
  width = 550
  height = 850
  style="border:none;"
></iframe>
</div>
 
The French government implemented a strict lockdown on March 17, 2020, initially planned for 15 days but extended to 55 days until May 11, 2020. As we saw before, the mobility disruption led to increased gaming popularity. During the lockdown, game pageviews surged, but post-intervention, they returned to pre-COVID levels. When considering game genre, we can see that during the lockdown, the video games about Action, Adult, Adventure, Horror, Puzzle, RPG, Sports and Strategy have attracted the most increase. We also note that Horror games actually remain more popular than pre-lockdown time after the intervention has been lifted, while other games are back to normal popularity just like the pre-covid time. We can specifically look into games about Sports and Multiplayer/Online. After the normalcy comeback, the popularities of these two genres of games actually declined, which is reasonable since people tends to play sports offline and meet offline to hang out and have fun.

### Germany – Less Restrictive, Less Interest in Games

<div align="center">
<iframe
  src="/assets/img/germany.html"
  width = 550
  height = 850
  style="border:none;"
></iframe>
</div>

Compared to its bordering country France, Germany has less restriction on the free move of the people, leading to less mobility decrease in Germany. Thus people actually spend less time at home and play games, and there is less increase in the pageviews of games in German-version Wikipedia. Overall, there is minor increased popularity in games, but it is obviously milder than that in France. Regarding to different game genres, RPG, Stimulation, Sports and Strategy enjoy the most gain from the lockdown, but if you compared it to other same genres in France, it is definitely a smaller gain. Interestingly, the Miscellaneous games have the most gain during the lockdown time. And the Stimulation and Strategy games are also quite popular, while the Action games actually have no interest increase.

### Japan – We Play Games for Passion

<div align="center">
<iframe
  src="/assets/img/japan.html"
  width = 550
  height = 850
  style="border:none;"
></iframe>
</div>

Japan didn't suffer from first wave of the pandemic, leaving thus the mobility disruption at the minimum level. In this case, people enjoyed more freedom moving around and the mobility data seems much more normal compared to France and Germany. In this case, the popularity in games is not forcefully increased due to the intervention from the government. However, there are still some minor gains in the game of Multiplayer/Online, Puzzle, Sports and Strategy. The Anime-theme games, which are supposed to be popular in Japan, have surprisingly not attained enough interest gain during the lockdown period. Also the popularity seems to last longer than expected after the intervention is over. We believe the explanation to be the follwing: since the mobility did not changed sharply, the popularity in the games can last longer since people are not "forced" to play games. Instead they appreciate the new free time without get a "video game overdose". Therefore, there is some evidence that the game industry in Japan actually benefits from covid in a longer time span.

## Le's dig deeper

Our previous findings reveal that while overall interest in gaming surged in many countries, the pattern wasn't uniform across all genres or regions. Some genres saw a spike in certain countries, whereas others experienced a decline within the same borders. This suggests that gaming preferences might vary from country to country, influenced by numerous factors.

Now, our study will be particularly focused on four genres: Action, Adult, Strategy, and Miscellaneous. These were selected based on their high view counts, which likely meant more robust data. Interestingly, these genres exhibited diverse trends in different nations.

Looking at the initial naive analysis, we noted that strategy games were uniformly popular across all three countries, with Japan showing the highest uptick. Action games presented a mixed picture: France saw considerable growth, Japan a modest rise, and Germany a slight drop. Adult games followed a similar pattern to action games, but with less variation between countries. Japan, in particular, showed a significant interest in adult games, which was not mirrored in action games. Miscellaneous games stood out, showing substantial increases in pageviews across almost all countries, with Germany showing a notable rise, which was not observed in the other genres.

<div align="center">
<iframe
  src="/assets/img/navie.html"
  width = 1000
  height = 900
  style="border:none;"
></iframe>
</div>

### Causal impact analysis

To refine our understanding, we applied a Google causal impact analysis and adjusted pageviews by the total Wikipedia views in respective languages. This adjustment revealed significant shifts, indicating that overall Wikipedia traffic was a factor to be considered.

For strategy games, the post-adjustment analysis indicated a clear preference in Japan and Germany during the pandemic. In contrast, the impact on action games was much more pronounced in France and Italy, with the effects in Japan and Germany not being statistically significant. French players showed a marked preference for adult games, whereas German players seemed to have little interest in this genre. Miscellaneous games, on the other hand, showed a compelling trend: Japan had a minimal relative impact, while Germany demonstrated a strong affinity for this category.

<div align="center">
<iframe
  src="/assets/img/casual.html"
  width = 800
  height = 550
  style="border:none;"
></iframe>
</div>

Summarizing, French and Italian gamers shared similar tastes during the pandemic, with the French leaning towards action and adult games, while Italians showed less interest in adult games. Japanese gamers favored strategy and adult games and showed little enthusiasm for other genres. Germans appeared to prefer strategy and miscellaneous games, with a significant inclination towards the latter.

To probe the reasons behind these preferences, we considered societal openness to sexual content by referencing Pornhub viewership rankings. Given the similar population sizes of France, Germany, and Italy, and Japan's slightly higher population, these rankings provide insight into national attitudes towards sex-related topics. France's higher ranking compared to Italy and Germany aligns with the interest in adult games during the pandemic. Interestingly, despite Germany's larger population, it has lower Pornhub traffic than Italy, further correlating with our gaming data.

<div align="center">
![Branching](/assets/img/Ph50.png)
</div>

For action and strategy games, differing trends suggest a link with national personality tendencies. For instance, the MBTI personality index suggests that the French, being more Extraverted and Observant, may prefer action-oriented games that engage their senses over strategic thinking.

Miscellaneous games defy easy categorization by personality or preference but seem to offer an accessible option during lockdowns, especially for those without a strong pre-existing preference for other genres.

![Branching](/assets/img/personalities.png)

# To what extent can English Wikipedia pages serve as a reliable estimate of the average video game popularity?

In this section we look at the possibility of english wikipedia pages being able to represent the global average and trend of video games. This is likely as video games are often released in english and do not always have other languages. Furthermore a lot of countries speak english on top of their native languages since english is the most common language worldwide. Studies show that 1.45 billion people speak english, and this encompasses more the higher classes. Therefore the people more likely to have access to video games often speak english, again explaining why english wikipedia pages could serve as a reliable estimate of the average video game popularity.

## Data Exploration / Processing

In order to find out if English Wikipedia pages can serve as a reliable estimate of the average video game popularity, we used the interventions and global mobility datasets in order to find enough relevant information. Later on we used an API to search for more specific games. As we can see wikipedia is accessed a lot, with a little increase during the COVID-19 lockdown period:

<div align="center">
  ![Branching](/assets/img/Total_views.png)
</div>

We analyzed the differences between pre-lockdown, lockdown, and normalcy of all the data. We looked at the different mobilities, page views, more specifically, page views in comparison to total page views. To find the relevant pages in the interventions dataset, we had to extract culture -> media -> video games, and then look at the percent usage of wikipedia that was associated with video games. We will see below the relationship between the Enlgish Wikipedia pages and the rest.

At first thought, given the amount of people that speak enligsh, as well as most video games originally being created in english would lead us all to believe that the English pages would follow a similar trend to the average wikipedia pages, right? Keep on reading to find out!

### Analysis

Take a look at the graph below, unsurprisingly, the lockdown in Great Britain is not representative of the average mobility. This is to be expected as the lockdowns were decided by every country individually and had nothing to do with their spoken language.

<div align="center">
<iframe
  src="/assets/img/average_mobility.html"
  width = 800
  height = 550
  style="border:none;"
></iframe>
</div>

At first glance, the english wikipedia pages do not seem to be a reliable estimate of the average video game popularity of all countries as it has very often the highest or lowest value. However when we scale down the english page views (two and a half times) we end up with the orange curve which is extremely similar to the average. This shows that english wikipedia pages (when toned down) are quite reliable when trying to estimate the global average.

But why are the English Wikipedia pages so much more volatile than the average page views?

Especially during the COVID-19 lockdown, English spiked a lot more than other countries. English is by far the most used language in the video game world for anything competitive. All the professional games are cast in English, so all the viewers and players of high level video games are forced to use English. Furthermore the lockdown allowed everyone that is higher level and passionate about video games to have a lot more time to dedicate to it than previously. Furthermore someone less passionate would most likely not put as much time into video games and would be more likely to spend less of their time online.

Before the COVID-19 lockdown, players often played the same games as they didn't have as much time to put into learning new ones. Since higher levels of video games are english speaking, they don't really need to look up their games on wikipedia as they already know it well enough. However during the lockdown, many new games rose to popularity (Among Us, Fall Guys), and these games pushed people to look them up and learn the new games, therefore the spike in english wikipedia pages during the lockdown. On top of that the people that play more often enjoy playing with add-ons to the games, which are almost always solely in English. However the higher level players tend to always return to their game of choice after the hype of the new games die down.

<div align="center">
  ![Branching](/assets/img/Among_Us.png)
<div>

Among Us is a great example to showcase this. It's not an accident that there is only information about the engish wikipedia searches for Among Us mid-2020. The vast majority of games are created in Enlgish only and they are then only translated into other languages when, but more importantly if they become more popular. Among Us was released mid 2018, however it gained a bit of popularity when the lockdown happened as a lot of people were home with time to play, often wanting to play fun games together, which Among Us clearly is. However even with this increase with wikipedia searches being in the hundreds didn't warrant for the game to be translated into any other languages, and therefore the lack of wikipedia pages for the game in any other language before it blew up.

This really is a great example of how the game has to gain in popularity in english before being translated, as we can see when the game really blew up mid september 2020 reaching hunderds of thousands of wikipedia searches, all the other languages began to exist and rise in popularity too. However this game, even though it was the perfect game for the COVID-19 lockdown in order to both have fun keep contact with friends, it only gained in popularity thanks to youtubers and twitch streamers playing it, making their viewers want to play the game too. Again we can see how the english pages reached higher than other languages, however the searches came down a lot faster too, but by looking at the english pages before the other pages even existed, we could easily predict what would happen with the other wikipedia pages.

<div align="center">
<iframe
  src="/assets/img/percent_pageviews.html"
  width = 800
  height = 550
  style="border:none;"
></iframe>
</div>

Obviously the COVID-19 lockdown increased the page views related to video games, but we can also see below that video games increased more relatively to other pages during the COVID-19 lockdown. This is important because all page views increased as we could see above when we showed the total amount of wikipedia searches. Unfortunately we cannot see the longer lasting effect that COVID-19 had on the pageviews a few years after the lockdown due to the lack of data with this dataset.

Furthermore, when we compare the trends individually, we can still match the english to be the average, no matter how restrictive the lockdown was. However it matches the semi_restrictive lockdowns the best. Look at the graph below and toggle between the different restrictivenesses or look at all of them at once and see for yourself that english matches the average trends quite well when toned down.

<div align="center">
<iframe
  src="/assets/img/normalized_percent.html"
  width = 800
  height = 550
  style="border:none;"
></iframe>
</div>

We could also look at the fact that england had a semi-restrictive lockdown and therefore represents the average of those countries the best, but that isn't the main point we are interested in as we want to see if the english pages are a good representation of the worldwide average in order to be able to predict the worldwide trend of games.

<div align="center">
<iframe
  src="/assets/img/mobility.html"
  width = 800
  height = 550
  style="border:none;"
></iframe>
</div>

## Conclusion

In conclusion, we found that by toning down the English Wikipedia pages, making it less volatile, we can accurately predict the worldwide average Wikipedia pages. Furthermore by looking more closely at specific games, we can see how English is often the first to follow a trend and therefore ride the "hype" longer, but crash more afterwards, explaining why it is often more volatile. English is also very commonly first to follow the "hype" of a new game as newer games are nearly exclusively made in english, and the other languages are added later on if the game takes off.
