---
date: 2021-05-30 23:19:29
layout: post
title: All about Classifications
subtitle: Classified movies, emails, and questions from a discussion forum
description: Classified movies, emails, and questions from a discussion forum
image: /assets/img/uploads/class.png
optimized_image: /assets/img/uploads/class.png
category: datascience
tags:
author: meinlee
paginate: false
---
<div id="toc_container">
<h2 class="toc_title">Table of Contents</h2>
<ul class="toc_list">
  <li><a href="#Spam vs. Ham: Email Classification">Spam vs. Ham: Email Classification</a></li>
  <li><a href="#Piazza (Discussion forum) questions">Piazza (Discussion forum) questions</a></li>
  <li><a href="#IMDB Movies">IMDB Movies</a></li>
</ul>
</div>


<h2 id="Spam vs. Ham: Email Classification">Spam vs. Ham: Email Classification</h2>

I classified over 1000 emails as "spam" or "ham" (not spam) using logistic regression and achieved a 92% testing accuracy. 

<b>Feature Engineering</b>
![Screen Shot 2022-05-04 at 10 10 09 PM](https://user-images.githubusercontent.com/73072620/166866512-4d48315e-5604-4102-b80b-0ef9919146ce.png)

Since this is a classification problem that requires a numeric input, I derived numeric features from the text data by using a pre-defined list of words as an indicator. For example, if the email contain words such as "now" or "call" (common words in a spam email), it will be classified as spam. 

<b>Evaluating Classifiers</b>

![Screen Shot 2022-05-04 at 10 08 46 PM](https://user-images.githubusercontent.com/73072620/166866430-af4c2154-a353-48c3-99a1-36ba3fe52398.png)

I looked into Precision, Recall, and ROC curves to evaluate my model. 

<b>Improving Accuracy</b>

![Screen Shot 2022-05-04 at 10 17 18 PM](https://user-images.githubusercontent.com/73072620/166866948-f3a37af5-81b5-46ee-9900-ddbe3d84c2eb.png)

In order find better features for my model, I used Regex to clear redundant words (HTML, links, stop words), categorized emails based on length of the email, caculated the percentage of capitalized characters and punctuations, and checked for the tone of the email through casual words like "oh", "ok", "yeah", etc. After adjusting the features and performing a 5-fold cross validation, my model's training accuracy improved from 88% to 92%.

<h2 id="Piazza (Discussion forum) questions">Piazza (Discussion forum) questions</h2>

![image](https://user-images.githubusercontent.com/73072620/166869512-4e712df2-1952-4d7f-8acd-dcedb301e133.png)

My team and I attended a 1-day Hackathon that was hosted by the UC Berkeley School of Information and sponsored by Atlassian. We identified professors' pain points in online learning and presented a coded POC consisting of machine learning predictions and a dashboard of a full-stack web app.

<b>Scraping, Cleaning, and Training Data</b>

We pulled 200+ questions from the Piazza discussion forum of a CS course. Then, we used a modified version of the Bloom and Garrison et al 2001 methods to label the data between 4 categories in order to create numeric features for logistic regression:

- Other/Logistics
- Recall/Remember
- Exploration/Analysis
- Create/Expand

Due to the small sample size, our model has high variance and may be prone to overfitting. We used cross-valifation techniques to retrain our model and achieve a training accuracy of 60% -- so at least it's better than a coin flip. 

<b>Results</b>

The challenge most professors face in a Zoom environment is not being able to read students' physical cues. With students' cameras turned off, how would professors know if a student is nodding in confidence or frowning in confusion during lectures? We leveraged the fact that most students turn to anonymous course discussion forums (Piazza) to ask questions or raise concerns. Our algorithm quantified student understanding using Bloom's Taxonomy (refer above) and informed professors of overall levels of understanding on course topics.

We impressed the judges with our creativity and technical skills -- earning ourselves a first runner-up position among 50+ teams. 

<h2 id="IMDB Movies">IMDB Movies</h2>

<a href="https://docs.google.com/forms/d/e/1FAIpQLSfh1Kx8ftMOR92ijcBb_-K2OAv2XAnQlWChwuBG2vTGkkBeuQ/viewform?usp=sf_link">Sign up for my mailing list for post updates!</a>


