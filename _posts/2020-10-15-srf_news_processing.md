
While having no clue about a global pandemic about to start just 6 months later I started to build a web crawler on srf.ch news headlines. Initially I was curious about the topics srf.ch is about to post every day, so I decided to save the headlines and see what I can process and visualize after a year. Then covid-19 came and dominated news rapidly, what we will see in the final plots of this blog post.

The Crawler

The crawler project is build on very basic R scripts and executed once a day by windows task manager. The tokenization, text processing and visualization are based on pandas, nltk and matplotlib.
First I want to share the inital crawler and how to get information from html pages on the web, in this case srf.ch. Schweizer Radio und Fernsehen SRF (English: Swiss Radio and Television) is a Swiss broadcasting company. The new business unit of SRG SSR, became the largest electronic media house of German-speaking Switzerland. About 2,150 employees work for SRF in the four main studios in Basel, Bern and Zürich. Thanks to fees, SRF works independently of economic or political interest groups. Journalistic quality has top priority. SRF cultivates diversity in its programming, which, wherever possible, takes a Swiss perspective. Fees enable a program for the entire society. This includes programs for the vast majority, but also offers for smaller groups. At SRF, children find their favorite formats as well as a mobile, web-savvy audience; the needs of older people are taken into account as well as the special needs of people with sensory disabilities. In this way, SRF serves the cohesion of society and mutual understanding.

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

The Processing


The Visualization
