---
date: 2020-10-29 08:57:37
layout: post
title: "Data Science & Analytics Projects"
subtitle: Brief overview of my Data Science & Analytics Projects.
description: How I told stories with numbers
image: /assets/img/uploads/data.png
optimized_image: /assets/img/uploads/data.png
category: datascience
tags:
author:
paginate: false
---

<div id="toc_container">
<h2 class="toc_title">Table of Contents</h2>
<ul class="toc_list">
  <li><a href="#Analyzing Conference Disparity in the NBA">Analyzing Conference Disparity in the NBA</a></li>
  <li><a href="#More Coming!">More Coming!</a></li>
</ul>
</div>

<h2 id="Analyzing Conference Disparity in the NBA">Analyzing Conference Disparity in the NBA</h2>
This project is conducted in R using data from the 2005-06 season to 2020-21. I analyzed wins, losses, points scored, and other game stats to determine if there is a significant conference disparity in the NBA.

<h4>Datasets</h4> 
'combined_standings.csv' contains team by season information (one row for each team in each season going back to '05-'06) with variables for wins, losses, win percentage, points scored and allowed per game, and a playoff indicator. 


'combined_team_vs_team_records.csv' has rows for each team in each season with columns representing matchup records against every team in the NBA in that season. For example, the 2016-17 Golden State Warriors won all four regular season matchups against the Los Angeles Clippers. Therefore the 'LAC' column of the 2016 Warriors row contains the value '4-0'.

<h4>What is the regular season win percentage of Western Conference teams against the East in the 16 year window?</h4>
```{r}
library(tidyverse)
standings <- read_csv("combined_standings.csv")
team_v_team <- read_csv("combined_team_vs_team_records.csv")

# Combine tables so we can have all of our information available in one spot. We join on team and season.
df = left_join(standings, team_v_team, by=c('bb_ref_team_name' = 'bb_ref_team_name', 'season'='season'))

# Filtering out Eastern conference rows.
WestData = df %>% filter(conference=='West')

# We get get the West team names from the 'WestData' table. Then remove columns where we have West vs. West matchups to isolate West vs. East.
westTeams = unique(WestData$team_short)
westVeast = WestData[,!(names(WestData) %in% westTeams)]

# We can clean this up by isolating to a matrix solely of west vs east and correct NA's to 0-0 
westVeast = westVeast[12:26]
westVeast[is.na(westVeast)] = '0-0'

# We're dealing with stubborn characters as our objects. For each value, we take the first and third index (corresponding to wins & losses respectively). We convert to an integer and sum across the row to get a West teams total Wins & Losses against the Eastern Conference in a given year.
wins=c()
losses=c()
for (i in c(1:240)){
  wins[i] = sum(as.numeric(substring(westVeast[i,],1,1)))
  losses[i] = sum(as.numeric(substring(westVeast[i,1:15],3,3)))
}

# Get the total wins and losses and find the win percentage.
westVeastWinPct = sum(wins)/sum(wins+losses)
round(westVeastWinPct,3)*100
```

#### From 2005-06 to 2020-21, Western Conference teams won 55.7% of regular season matchups against Eastern Conference opponents.

Let's get a sense of the consistency of the inequality. 


We can shove the wins and losses vectors into the West table.

WestData$wins = wins
WestData$losses = losses
We group by season and get the total wins and losses for the West against the East. If the west outperforms the East, we set 'westbetter' to 1.

yearByyear = WestData %>%
  group_by(season) %>%
  summarise(WestvEastwins = sum(wins), 
            WestvEastlosses = sum(losses)) %>%
  mutate(westbetter = ifelse(WestvEastwins > WestvEastlosses, 1, 0))
Then we can sum 'westbetter' to find the number out of the past 16 seasons.

sum(yearByyear$westbetter)

Western Conference teams have won more regular season games than the East in 15 out of the last 16 seasons.

