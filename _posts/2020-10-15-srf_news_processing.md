---
layout: post
title: News Headlines during Corona Pandemic. Crawling and Processing of Swiss Media Headlines 2019-2020 
cover-img: /assets/img/srf_head.jpg
tags: [data, news, corona, pandemic, swiss]
---

While having no clue about a global pandemic about to start just 6 months later I started to build a web crawler on srf.ch news headlines. Initially I was curious about the topics srf.ch is about to post every day, so I decided to save the headlines and see what I can process and visualize after a year. Then covid-19 came and dominated news rapidly, what we will see in the final plots of this blog post.

Title Image by: <span>Photo by <a href="https://unsplash.com/@raphaelphotoch?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Raphael Schaller</a> on <a href="https://unsplash.com/s/photos/words?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

## The Crawler

The crawler project is build on very basic R scripts and executed once a day by windows task manager. The tokenization, text processing and visualization are based on pandas, nltk and matplotlib.
First I want to share the inital crawler and how to get information from html pages on the web, in this case srf.ch. Schweizer Radio und Fernsehen SRF (English: Swiss Radio and Television) is a Swiss broadcasting company. The new business unit of SRG SSR, became the largest electronic media house of German-speaking Switzerland. About 2,150 employees work for SRF in the four main studios in Basel, Bern and Zürich. Thanks to fees, SRF works independently of economic or political interest groups. Journalistic quality has top priority. SRF cultivates diversity in its programming, which, wherever possible, takes a Swiss perspective. Fees enable a program for the entire society. This includes programs for the vast majority, but also offers for smaller groups. At SRF, children find their favorite formats as well as a mobile, web-savvy audience; the needs of older people are taken into account as well as the special needs of people with sensory disabilities. In this way, SRF serves the cohesion of society and mutual understanding.


```R
library(rvest)
library(xml2)
library(curl)
library(plyr)
library(readxl)
library(ggplot2)
library(lubridate)
library(stringr)
library(DataCombine)

url <- "https://www.srf.ch"
html <- paste(readLines(url), collapse="\n")
matched <- str_match_all(html, " href=\"(.*?)\"")                #hyperlinks
date    <- str_match_all(html, " data-date-published=\"(.*?)\"") #dates
links <- matched[[1]][, 2]

links_frame <- as.data.frame(links) %>% mutate(links=as.character(links)) %>% mutate(date=Sys.Date())

links_news     <- grepl.sub(data = links_frame, pattern = "/news/", Var = "links")
```

<span>Photo by <a href="https://unsplash.com/@martinsanchez?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Martin Sanchez</a> on <a href="https://unsplash.com/s/photos/news-corona?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span> ![covid](/assets/img/srf.jpg)

## The Processing

```python
import pandas as pd
import sys
import nltk
import texthero as hero
from nltk.corpus import stopwords
import matplotlib.pyplot as plt

# Read the data in
df_covid_stats = pd.read_csv('srf_data_all.csv')
df=df_covid_stats[['links','date']].copy()

# tokenize data
df['links']=df['links'].str.replace('-', ' ', regex=True)
df['tokenized_sents'] = df.apply(lambda row: nltk.word_tokenize(row['links'], language='german'), axis=1)

# explode tokens
df_deep=df.explode('tokenized_sents')

# remove stop words and other trash
df_deep['tokenized_sents'] = hero.remove_stopwords(df_deep['tokenized_sents'])
stop = stopwords.words('german')
df_deep['tokenized_sents']= df_deep['tokenized_sents'].apply(lambda x: ' '.join([word for word in x.split() if word not in (stop)]))

searchfor = ['https',':']
df_deep=df_deep[~df_deep.tokenized_sents.str.contains('|'.join(searchfor), regex= True, na=False)]

# final data prep
df_deep = pd.merge(df_deep, df, left_index=True, right_index=True)
df_deep=df_deep[['tokenized_sents_x','date_x']]

# corona data
searchfor = ['corona', 'virus', 'sars','covid','pandemie']
df_corona=df_deep[df_deep.tokenized_sents_x.str.contains('|'.join(searchfor), regex= True, na=False)]
df_corona['count']=1
df_corona=df_corona[['count','date_x']].copy()
df_corona=df_corona.groupby(['date_x']).sum()
df_corona['news']='corona'
df_corona.rename(columns={'count':'corona'}, inplace=True)

```

## The Visualization

```Python
plt.figure()
plt.ylim(0, 100)

ax=df_tot.plot()
ax.xaxis.set_major_locator(plt.MaxNLocator(10))

# Add labels to the plot
style_election = dict(size=7, color='orange')
style_corona = dict(size=7, color='blue')

ax.text('2020-01-01', 35, "first corona", **style_corona)
ax.text('2020-01-01', 33, "deaths china", **style_corona)

ax.text('2019-10-24', 60, "Swiss federal", **style_election)
ax.text('2019-10-24', 58, "election", **style_election)



ax.legend(loc='upper center', bbox_to_anchor=(0.5, 1.2),
          ncol=3, fancybox=True, shadow=False)

ax
```

![plot](/assets/img/srf_news.jpg)
