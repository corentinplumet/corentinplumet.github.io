x---
layout: home
title: Covid-eo Games
subtitle: Analysis of the Covid-19 lockdown impact on the interest towards video games
---

Have you ever wondered if the COVID-19 had more impact on people than just the sudden urge for people to become expert in Zoom? Or did you spend most of your time training to become the last survivor on the Fortnite island? If the answer is yes, then this article is just for you because we are going to reveal the mysterious connection between the pandemic and the video games industry. Our mission: understanding the relationship between global lockdown experiences, variations in intensity, and the consequent shifts in attention towards video games. Our study aims not only to decrypt the impact of lockdown measures but also to discern whether the interest in distinct genres of games underwent different changes during this period.

This article contains many interactive visualizations. Don't forget to use them to be sure to understand all the important informations. Let's get started, it's about to get real (or at least virtually real)!

# Introduction

To introduce the subject properly, we first need to get an idea of what type of games there are and their distribution in the wikipedia database. By parsing down all the game pages from the Wikipedia database and categorizing them into several game genres, we can get an overview and get started with our data analysis!

<iframe
  src="/assets/img/game genre count.html"
  width = 900
  height = 550
  style="border:none;"
></iframe>

The most prevalent genre in the dataset is "Action”. This suggests that action games are highly popular and/or widely produced. The dataset encompasses diverse genres, including sports, role-playing games (RPG), adventure, science fiction, puzzle, strategy, simulation, and more. This diversity indicates a variety of gaming preferences and interests, which aligns with the current development of the worldwide game industry.

The following graph plots for each day the total views of pages related to the same main genre according to a specific language of research. From this graph we can already see trends on the Wikipedia traffic, depending on the periods, languages and themes. Do not hesitate to interact with this graph!

<div align="center">
<iframe
  src="/assets/img/pageviews.html"
  width = 800
  height = 650
  style="border:none;"
></iframe>
</div>

# Lockdown and overall video games interest: how strong is the relationship?

In this part, we are going to discuss the relation between the different types of lockdowns around the world, and their impact on people's interest for video games. 

To measure people's interest towards video games we will use the Wikipedia pageviews. Wikipedia being the largest and most popular encyclopedia in the world, the pageviews on the website are a good metric to know what people are searching for and thus, are interested in.

To categorize the lockdown of different country, we will use the reported mobility of Google from January 2020 until August 2020.  It's like the GPS for lockdown strictness – the biggest the decrease in mobility, the tighter the lockdown grip. 

Our study extends to countries where a singular language predominantly prevails. This way we will link accurately Wikipedia pages written in a specific language to a specific country. For example, using the views on pages in Swedish will give us a way more accurate estimation of people's interests in Sweden than if we were to do the same thing with English.

## Mobility pattern

The plot below presents the evolution of moblity between the 15th of February 2020 and the 25th of August 2020, taking as 0 the mobility on the first day of the interval. We have data for France, Denmark, Germany, Italy, the Netherlands, Norway, Serbia, Sweden, South Korea, Catalonia (Barcelona), Finland and Japan. The 2 red lines represent the dates were we can statistically consider a mobility drop and then a normality comeback. These dates are really close to the start and finish of the moblity restrictions (1 or 2 days delay). Also, a smoothened curve of each mobility signal can be displayed by clicking on the button at the bottom of the plot.  

<div align="center">
<iframe
  src="/assets/img/output.html"
  height = 825
  width = 800
  style="border:none;"
></iframe>
</div>

For most of the countries, the lockdown is a real anormaly in the mobility pattern. Mobility in France for example, decreases by around 70% after the beginning of the lockdown. However, for some countries like Japan the decrease is less noticeable. This disparity in moblity change motivates the clustering of countries. If we want to see if the lockdown had an impact on the attention towards video games, we can't consider all the countries as one group but we need to group them according to what we will call their "lockdown Intensity".

![Branching](/assets/img/countries_cluster.png)

There are 3 clear tendancies with very similar patterns. One group, had a very restrictive lockdown with a minimum mobility of around 75% of what it was before the lockdown. The second group, had a restrictive lockdown with a minimum mobility of around 45% of what it was before the lockdown. And the last group also experienced a lockdown, but it was an unrestrictive one, leading to a small decrease in total mobility. 

## The attention shift towards video games

Now that we have grouped the countries according to their lockdown intensity, we will get the measure of the attention shift towards video games.

During the lockdown, people were most of the time at home, and thus had more leisure time than usual, which translates into a higher traffic on the Wikipedia website overall. For this reason, we will not be using the absolute value of the pageviews, but rather the percentage of views on video games related pages amongst all the Wikipedia traffic.

To fulfill this purpose, we will be using the percentage of pageviews for video games, in proportion to the entire trafic on the Wikipedia website. The following figure shows the percentage of Wikipedia pageviews related to video games for the same countries we have in the mobility part.

![Branching](/assets/img/pageviews.png)

After the mobility drop, it appears that certain countries experienced a rise in attention towards video games. To have a better understanding of the meaning of these curves, we will group them following the "lockdown intensity" shown previously in the mobility context.

![Branching](/assets/img/pageviews_cluster.png)

## But is there a correlation...

In the previous part, we saw that there might be an increase in the proportion of views for video games related pages after the mobility drop. To get a representation of this shift in attention, we can plot the relative increase in proportion between the pre-lockdown and post-lockdown period.

<p align="center">
  <img src="/assets/img/medianpercentage.png" />
</p>

There is a clear tendancy of increase in attention towards video games during the lockdown period as all the countries, except for Finland, experienced an increase in percentage of pageviews related to video games on Wikipedia. And with this graph, it is clear that the intensity of lockdown had an impact on the attention shift towards video games. The countries with an unrestrictive lockdown (yellow: Sweden, Korea, Japan) experienced a small increase in attention compared to the 2 groups with a restrictive and very restrictive lockdown. It also looks like the red group (very restrictive lockdown) had a larger increase compared to the orange group (restrictive lockdown), but the difference is less significant than the one with the unrestrictive lockdown group.

<div align="center">
<iframe
  src="/assets/img/boxplot.html"
  width = 800
  height = 500
  style="border:none;"
></iframe>
</div>

The boxplot above gives us another distribution view of the attention shift. And with the confidence interval of 95% percent, we can confirm our previous analysis. The "restrictive" group's confidence intervals overlap with the 2 other, but the "very restrictive" group and "unrestrictive" group don't overlap. Also the overlap for the "restrictive" and "unrestrictive lockdown" are really small. We can note that the odd shape of the box (the confidence interval being larger than the 1st to 3rd quartile interval) is due to the small number of points in our samples.

But is this attention shift towards video games correlated to the mobility of people? To answer this question, we get a first glance by plotting the correlation coefficient between the mobility time series and the Wikipedia pageviews time series.

<p align="center">
  <img src="/assets/img/correlation_coeff_plot.png" />
</p>

According to this graph, the intensity of lockdown doesn't have an impact on the correlation value. Japan and Korea which belong to the unrestrictive group have a high negative correlation that is statistically significant, just like the countries that belong to the other groups.

What is interesting with this graph is that it reveals that the countries with a very low and not significant correlation are Norway, Sweden, Finland and Denmark, which all are Scandinavian countries. It means that even though these countries experienced an increase of the video games page views percentage during the lockdown period (Norway and Denmark especially because Sweden experienced a very low increase and Finland no increase at all), it's not related to the mobility decrease. For Denmark and Norway, the increase in views on Wikipedia pages related to video games during the lockdown is simply part of an overall increase, not necessarily linked to the drop in moblity. That's why we notice an increase of video games related pageviews during the lockdown but no correlation with the drop in mobility.

From all this analysis, 3 conclusions can be drawn: First, the amount of decrease in mobility and the intensity of the lockdown are factors that drive the attention shift towards video games: the less the people are moving, the more they spend time playing video games and doing research about it. The second statement is an extension of the first one, in the sense that the mobility decrease intensity doesn't impact its correlation with the attention shift. A mobility decrease, no matter its importance, will lead to a proportionnal increase in video games interest. The third statement is an exception for the Scandinavian countries. These countries may have experienced an increase in video games research proportionnally speaking, but it's not related to the mobility. 

However, we need to be aware of the limit of these conclusions. What we found is a correlation relation, not a causation one. It means that even if it looks like the drop in mobility may be the cause of the attention increase towards video games, maybe there is another factor linked to the pandemic that drives the increase in attention.

### The catalonian exception

But what about Catalonia? This region chose to not follow the trend. We noticed a huge increase in attention towards video games after the lockdown with the previous plots, but we also saw a very strong positive correlation between the mobility and the interest in video games. Does that mean that the catalans are more interested in video games when they are free to move? Let's take a look:

![Branching](/assets/img/catalonia.png)

The mobility curve and the video games attention curve are closely following once the lockdown is effective. When the mobility dropped, the attention towards video games didn't change much, but after that, it followed the rise in mobility. That explains the strong positive correlation and the huge increase in attention between the lockdown.

# Now let's take a look at specific types of video games!

Now that we have seen the overall relationship between interest in video games and the mobility decrease, let's get specific and dive further in the video games part of the analysis. There are many types of video games and even though they are, as a group, correlated with the mobility not all of them might share the same link with it. By assigning each page to a video game genre, we can try to see what the trends are amongst all the different types of video games. The following part analyses French, Japanese, Italian and German growth in pageviews across gaming categories. These four languages, nearly unique to a single country, are becoming our focal point due to their distinct lockdown measures, geographic placement, and cultural differences, offering a rich ground for analysis.

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
 
The French government implemented a strict lockdown on March 17, 2020, initially planned for 15 days but extended to 55 days until May 11, 2020. As we saw before, the mobility disruption led to an increase in gaming popularity. During the lockdown, game pageviews surged, but post-intervention, they returned to pre-COVID levels. When considering game genre, we can see that during the lockdown, the video games about Action, Adult, Adventure, Horror, Puzzle, RPG, Sports and Strategy attracted the most people. We also note that Horror games actually remained more popular than pre-lockdown after the restrictions had been lifted, while other games went back to their normal popularity just like at pre-covid time. We will specifically look into games about Sports and Multiplayer/Online. After the normalcy comeback, the popularities of these two genres of games actually declined, which is reasonable since people tend to play sports offline and meet offline to hang out and have fun.

### Germany – Less Restrictive, Less Interest in Games

<div align="center">
<iframe
  src="/assets/img/germany.html"
  width = 550
  height = 850
  style="border:none;"
></iframe>
</div>

Compared to its bordering country France, Germany had less restrictions on the movements of people, leading to a smaller mobility decrease in Germany. This is a reason why people spent less time at home and play video games, and there is less increase in the pageviews of games in German-version Wikipedia. Overall, there is a minor increase of popularity in games, but it is obviously milder than that in France. Regarding different game genres, RPG, Stimulation, Sports and Strategy enjoy the biggest gain from the lockdown, but if you compare it to other same genres in France, it is definitely a smaller gain. Interestingly, the Miscellaneous games have the most gain during the lockdown time. And the Stimulation and Strategy games are also quite popular, while the Action games actually have no interest increase.

### Japan – We Play Games for Passion

<div align="center">
<iframe
  src="/assets/img/japan.html"
  width = 550
  height = 850
  style="border:none;"
></iframe>
</div>

Japan didn't suffer from first wave of the pandemic, leaving thus the mobility disruption at the minimum level. In this case, people enjoyed more freedom moving around and the mobility data seems much more normal compared to France and Germany. In this case, the popularity in games is not forcefully increased due to the intervention from the government. However, there are still some minor gains in the game of Multiplayer/Online, Puzzle, Sports and Strategy. The Anime-theme games, which are supposed to be popular in Japan, have surprisingly not had a large interest gain during the lockdown period. Also, the popularity seems to last longer than expected after the intervention is over. We believe the explanation to be the follwing: since the mobility did not change sharply, the popularity in the games can last longer since people are not "forced" to play games. Instead they appreciate the new free time without get a "video game overdose". Therefore, there is some evidence that the game industry in Japan actually benefits from covid in a longer time span.

## A deeper dive in the data...

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

To summarize, French and Italian gamers shared similar tastes during the pandemic, with the French leaning more towards action and adult games, while Italians showed less interest in adult games. Japanese gamers favored strategy and adult games and showed little enthusiasm for other genres. Germans appeared to prefer strategy and miscellaneous games, with a significant inclination towards the latter.

To analyse the reasons behind these preferences, we considered societal openness to sexual content by referencing Pornhub viewership rankings. Given the similar population sizes of France, Germany, and Italy, and Japan's slightly higher population, these rankings provide insight into national attitudes towards sex-related topics. France's higher ranking compared to Italy and Germany aligns with the interest in adult games during the pandemic. Interestingly, despite Germany's larger population, it has lower Pornhub traffic than Italy, further correlating with our gaming data.

<p align="center">
  <img src="/assets/img/Ph50.png" />
</p>

For action and strategy games, differing trends suggest a link with national personality tendencies. For instance, the MBTI personality index suggests that the French, being more extraverted and observant, may prefer action-oriented games that engage their senses over strategic thinking.

Miscellaneous games defy easy categorisation by personality or preference but seem to offer an accessible option during lockdowns, especially for those without a strong pre-existing preference for other genres.

![Branching](/assets/img/personalities.png)

But wait. Don't you think that we missed something? Since the beginning of the article we are talking about different languages without mentioning the most used and known worldwide. I'm of course speaking about English. It's true that we didn't include the english language yet, but it's because this language is not representative of a country as many people speak it around the globe. Thus, is it representative of worldwide tendencies? Let's answer that question!

# To what extent can English Wikipedia pages serve as a reliable estimate of the average video game popularity?

In this section we look at the possibility of english wikipedia pages being able to represent the global average and trend of video games. This is likely as video games are often released in english and do not always have other languages. Furthermore a lot of countries speak english on top of their native languages since english is the most common language worldwide. Studies show that 1.45 billion people speak english, and this encompasses more the higher classes. Therefore the people more likely to have access to video games often speak english, again explaining why english wikipedia pages could serve as a reliable estimate of the average video game popularity.

## Data Exploration / Processing

In order to find out if English Wikipedia pages can serve as a reliable estimate of the average video game popularity, we used the interventions and global mobility datasets in order to find enough relevant information. Later on we used an API to search for more specific games. As we can see wikipedia is accessed a lot, with a little increase during the COVID-19 lockdown period:

<p align="center">
  <img src="/assets/img/Total_views.jpg" />
</p>

We analysed the differences between pre-lockdown, lockdown, and normalcy of all the data. We looked at the different mobilities, page views, more specifically, page views in comparison to total page views. To find the relevant pages in the interventions dataset, we had to extract culture -> media -> video games, and then look at the percent usage of wikipedia that was associated with video games. We will see below the relationship between the English Wikipedia pages and the rest.

At first thought, given the amount of people that speak English, as well as most video games originally being created in english would lead us all to believe that the English pages would follow a similar trend to the average wikipedia pages, right? Keep on reading to find out!

## Analysis

Take a look at the graph below, unsurprisingly, the lockdown in Great Britain is not representative of the average mobility. This is to be expected as the lockdowns were decided by every country individually and had nothing to do with their spoken language.

<div align="center">
<iframe
  src="/assets/img/average_mobility.html"
  width = 950
  height = 625
  style="border:none;"
></iframe>
</div>

At first glance, the english wikipedia pages do not seem to be a reliable estimate of the average video game popularity of all countries as it has very often the highest or lowest value. However when we scale down the english page views (two and a half times) we end up with the orange curve which is extremely similar to the average. This shows that english wikipedia pages (when toned down) are quite reliable when trying to estimate the global average.

But why are the English Wikipedia pages so much more volatile than the average page views?

Especially during the COVID-19 lockdown, English spiked a lot more than other countries. English is by far the most used language in the video game world for anything competitive. All the professional games are cast in English, so all the viewers and players of high level video games are forced to use English. Furthermore the lockdown allowed everyone that is higher level and passionate about video games to have a lot more time to dedicate to it than previously. Furthermore someone less passionate would most likely not put as much time into video games and would be more likely to spend less of their time online.

Before the COVID-19 lockdown, players often played the same games as they didn't have as much time to put into learning new ones. Since higher levels of video games are english speaking, they don't really need to look up their games on wikipedia as they already know it well enough. However during the lockdown, many new games rose to popularity (Among Us, Fall Guys), and these games pushed people to look them up and learn the new games, therefore the spike in english wikipedia pages during the lockdown. On top of that the people that play more often enjoy playing with add-ons to the games, which are almost always solely in English. However the higher level players tend to always return to their game of choice after the hype of the new games die down.

![Branching](/assets/img/Among_Us.jpg)

Among Us is a great example to showcase this. It's not an accident that there is only information about the English wikipedia searches for Among Us mid-2020. The vast majority of games are created in English only and they are then only translated into other languages when, but more importantly if they become more popular. Among Us was released mid 2018, however it gained a bit of popularity when the lockdown happened as a lot of people were home with time to play, often wanting to play fun games together, which Among Us clearly is. However even with this increase with wikipedia searches being in the hundreds didn't warrant for the game to be translated into any other languages, and therefore the lack of wikipedia pages for the game in any other language before it blew up.

This really is a great example of how the game has to gain in popularity in english before being translated, as we can see when the game really blew up mid September 2020 reaching hundreds of thousands of wikipedia searches, all the other languages began to exist and rise in popularity too. However this game, even though it was the perfect game for the COVID-19 lockdown in order to both have fun keep contact with friends, it only gained in popularity thanks to youtubers and twitch streamers playing it, making their viewers want to play the game too. Again we can see how the english pages reached higher than other languages, however the searches came down a lot faster too, but by looking at the english pages before the other pages even existed, we could easily predict what would happen with the other wikipedia pages.

<div align="center">
<iframe
  src="/assets/img/percent_pageviews.html"
  width = 850
  height = 675
  style="border:none;"
></iframe>
</div>

Obviously the COVID-19 lockdown increased the page views related to video games, but we can also see below that video games increased more relatively to other pages during the COVID-19 lockdown. This is important because all page views increased as we could see above when we showed the total amount of wikipedia searches. Unfortunately we cannot see the longer lasting effect that COVID-19 had on the page-views a few years after the lockdown due to the lack of data with this dataset.

Furthermore, when we compare the trends individually, we can still match the english to be the average, no matter how restrictive the lockdown was. However it matches the semi_restrictive lockdowns the best. Look at the graph below and toggle between the different restrictivenesses or look at all of them at once and see for yourself that english matches the average trends quite well when toned down.

<div align="center">
<iframe
  src="/assets/img/normalized_percent.html"
  width = 850
  height = 700
  style="border:none;"
></iframe>
</div>

We could also look at the fact that England had a semi-restrictive lockdown and therefore represents the average of those countries the best, but that isn't the main point we are interested in as we want to see if the english pages are a good representation of the worldwide average in order to be able to predict the worldwide trend of games.

<div align="center">
<iframe
  src="/assets/img/mobility.html"
  width = 850
  height = 450
  style="border:none;"
></iframe>
</div>

In summary, we found that by toning down the English Wikipedia pages, making it less volatile, we can accurately predict the worldwide average Wikipedia pages. Furthermore by looking more closely at specific games, we can see how English is often the first to follow a trend and therefore ride the "hype" longer, but crash more afterwards, explaining why it is often more volatile. English is also very commonly first to follow the "hype" of a new game as newer games are nearly exclusively made in english, and the other languages are added later on if the game takes off.

# Video games? Not the only type of games to entertain!

We've crunched the numbers and found fascinating things. There's a significant shift in people's interest in games during these lockdown periods. But is it only about video games? To be completely exhaustive we also need to study the old school version of video games. We're talking about board games, these classic, timeless entertainers.

In the following section we will discuss the shift in attention towards board games and see if they follow the same trends as the video games.

## Chess Games: A Trend or an Anomaly?

First up, chess games. You can almost see the spike in interest during the lockdowns on our charts. Weekends are particularly interesting because they often align with peaks in online searches. Let's take a look at the change in pageviews of chess.

![Branching](/assets/img/JUSTE_CHESS.png)

But here's the problem: chess might not be our best indicator for this study. Why? Its popularity exploded in recent years, skewing our data (thanks mostly to Magnus Carlsen and Gotham Chess).

<p align="center">
  <img src="/assets/img/chesscom.png" />
</p>

This is why in the next analysis, we're shifting our focus to more traditional board games, ones that have stood the test of time.

## Board Games: A Window into People's Lives

As we take a look at some classic board games, a pattern emerges for weekends, as they present an increase in Wikipedia visits. But there's more to be studied: during lockdowns, these games saw a noticeable increase in interest on Wikipedia's website. It's as if they became a go-to source of entertainment during those challenging times.

### Uncovering Board Game Trends: An Analytical Adventure

Next, we're embarking on a journey to analyze 20 beloved board games. Our mission? To study the patterns surrounding these games. How often do people look them up on Wikipedia? Take a look at the change in Risk's change in page views. Get ready for some eye-opening insights!

![Branching](/assets/img/VOILA_STP.png)

This investigation offers a captivating look into how the interest for board games has changed during these unprecedented times. In the next section of the study, we will embark on an exploration of 20 popular board games. Our objective? To decode the patterns of interest surrounding them. By tracking the total number of views these board games received on Wikipedia, we aim to uncover intriguing insights! 

![Branching](/assets/img/testbd.png)

This plot reveals a remarkable story, particularly evident during the COVID-19 era: the increasing popularity of board games. During these times, board games captured the public's attention, along with the general interest in Wikipedia's diverse topics. 

There is a peak that emerges in the end of 2021. This spike stands signals a period of heightened fascination. Maybe people were eager to spend time with their families playing their favourites board games? What extraordinary events unfolded during this year-end? As we get closer to resolving this mystery, we find ourselves on the edge of uncovering something fascinating.

## Predictive Modeling: Peering into the Future of Board Games

Now we're things are going to get even more interesting as we're going to use a user-friendly neural network model to predict the future popularity of board games. We will be using the 20 days surrounding to predict the pageviews for boardgames.We'll be comparing 'normal' times with the pandemic period to see if board games truly became the stars of family entertainment.

But why stop there? We're on a mission to uncover something special. We'll train our model using data up until 2020, giving it a sense of what "normal" days look like for board game interest. Then, the real magic begins. We'll put this trained model to the test after the begining the COVID-19 pandemic, a time when people turned to board games for family fun.
The question is whether board games experienced a surge in interest, not just because of Wikipedia's overall popularity, but because families across the globe rediscovered the joy of board game nights.

![Branching](/assets/img/actual_vs_predicted.png)

The Story Told by Graphs: Board Games in the Limelight

Our graphs sing a fascinating tune, showing how board games danced along with global Wikipedia trends. The lockdown period, however, reveals something extraordinary. Board games experienced an increase in interest, their popularity climbing higher than expected. As we approached the 2021 year-end festivities, this trend became even more pronounced. It's a heartwarming sign of families coming together, embracing the joy of board games, spending quality time together after some tough times.

# Conclusion

In conclusion, our study presents an insight of the impact of the COVID-19 pandemic and associated lockdown measures on the people's interest towards video games. This interest was measured using Wikipedia pageviews, revealing a correlation between lockdown intensity and the rise in video game attention. Countries with more restrictive lockdowns were more inclined to have a significant increase in video game pageviews, indicating that reducing the mobility is leading people play video games, as they gain a lot of free time. However, this correlation is not always true and varies among countries. Sometimes the increase is not directly linked to mobility changes, as seen in Scandinavian countries.

We also found that the type of video games that gained popularity varied by country. Cultural differences and lockdown intensity are the main influence that drives that popularity. For example, France experienced a rise in action and adult games, while Germany showed a preference for strategy and miscellaneous games. Japan, with its minimal mobility disruption, had a more prolonged interest in certain game genres. It suggests a less reactive but more sustained engagement with video games, as the player were less constrained to play video games.

The analysis extended to board games, reveals a similar trend of increased interest during lockdowns. The study showed that during times of restricted movement, people turned to both video games and board games for entertainment, highlighting the role of games as a significant source of leisure and social interaction during challenging times.

We could decrypt in this study the relation between english pageviews and global worldwide trend. We saw that we can accurately predict the worldwide average Wikipedia pages, even if the english page views is often more volatile than the other language.

In summary, the pandemic's impact on gaming interests was multifaceted, influenced by lockdown severity, cultural preferences, and the availability of leisure time. This shift in entertainment choices reflects a broader trend of adapting to new lifestyles and finding alternative means of engagement and social interaction during periods of isolation.
