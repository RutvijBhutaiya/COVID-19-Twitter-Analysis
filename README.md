# COVID-19: Twitter-Analysis
#### Twitter study, includes the Tweets between the day first COVID-19 case detected from Whuan on 31st Dec 2019, till 15th March 2020. We did twitter mining based on this dates for the study. 



<p align="center"><img width=86% src=https://user-images.githubusercontent.com/44467789/76741958-64ac7300-6796-11ea-8e6b-db2c0859357b.png> 
  
                                                    Source: PNGKey




<br>

## Table of Content

- [Objective](#objective)
- [Approach](#approach)
- [Study Dataset Creation](#study-dataset-creation)
- [Tweet Analysis](#tweet-analysis)
- 


<br>

## Objective

Objective of this study is to do analysis on official twitter account from top countries health department and WHO twitter account on COVID-19 breakout since 31st Dec 2019 in Wuhan, China. We analysized which countries health departments are most active in this war against pandemic. 

<br>

## Approach
- Set Twitter API
- Use personal API and codes for tweet mining.
- Identify the countries official Health Department accunts on twitter
- Collect Tweets from 01/01/2020 to 15/03/2020
- Analysis on ReTweets and Active official accounts
- Analysis of frequently of words in tweets
- Combine data results and conclusion. 

<br>

## Study Dataset Creation

For the data, we turned to twitter API. Here, we targeted the important health department in countries and their official Twitter account. Twitter official accounts,

-  World Health Organization: @WHO
-  India: Ministry of Health: @MoHFW_INDIA
-  The USA: TheU.S. Department of Health and Human Services: @HHSGov
-  UK: Department ofHealth and Social Care: @DHSCgovuk
-  Australia:Australian Government Department of Health: @healthgovau


For the analysis, we collected the tweets from the respectedoffice health accounts from 31st Dec 2019 till 15th March2020. 

```

## @WHO

tweetWHO1 = searchTwitter('from:@WHO', 2000, lang = 'en', since = '2020-01-01', until = '2020-03-15')

tweetWHO1 = do.call('rbind', lapply(tweetWHO1, as.data.frame))

View(tweetWHO1)
```

F0r Study purpose we focused only on ReTweets, however,

```
> head(tweetWHO1)
                                                                                                                                                                text
1                       During times of stress and crisis, it is common for children to seek more attachment and be more demanding on paren… https://t.co/ttY5e8BS8L
2                       We thank our 6 million followers for their trust and support to provide the world with accurate health information.… https://t.co/DGuhFme9Rq
3                     RT @Refugees: "What are we doing to help refugees avoid the #coronavirus?"\n“Will people fleeing war still be able to cross borders?” \n“Coul…
4                       RT @DrTedros: You do a heroic job. We know that this crisis is putting a huge burden on you and your families. We know you are stretched to…
5                       RT @DrTedros: I want to send a personal and sincere thank you to every health worker around the world – especially nurses and midwives, who…
6 RT @DrTedros: Appreciated the chance to talk with @MattHancock today about #COVID19 in the <U+0001F1EC><U+0001F1E7>. @WHO is committed to working with the govern…
  favorited favoriteCount replyToSN             created truncated
1     FALSE          1414       WHO 2020-03-14 23:26:27      TRUE
2     FALSE          4675      <NA> 2020-03-14 23:12:56      TRUE
3     FALSE             0      <NA> 2020-03-14 23:10:57     FALSE
4     FALSE             0      <NA> 2020-03-14 23:10:33     FALSE
5     FALSE             0      <NA> 2020-03-14 23:10:30     FALSE
6     FALSE             0      <NA> 2020-03-14 23:10:12     FALSE
           replyToSID                  id replyToUID
1 1238962852024717318 1238969771808432129   14499829
2                <NA> 1238966369477169153       <NA>
3                <NA> 1238965873932722176       <NA>
4                <NA> 1238965769611984897       <NA>
5                <NA> 1238965760455835658       <NA>
6                <NA> 1238965683158990848       <NA>
                                                                        statusSource
1 <a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a>
2            <a href="https://mobile.twitter.com" rel="nofollow">Twitter Web App</a>
3 <a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a>
4 <a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a>
5 <a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a>
6 <a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a>
  screenName retweetCount isRetweet retweeted longitude latitude
1        WHO          831     FALSE     FALSE        NA       NA
2        WHO          960     FALSE     FALSE        NA       NA
3        WHO         1027      TRUE     FALSE        NA       NA
4        WHO          445      TRUE     FALSE        NA       NA
5        WHO          822      TRUE     FALSE        NA       NA
6        WHO          132      TRUE     FALSE        NA       NA
```

Similarly, we did for all the official twitter heal account from India, the US, UK and Australia. 

<br>

## Tweet Analysis



Note: GitUploaded data and Study us diffrent. 
