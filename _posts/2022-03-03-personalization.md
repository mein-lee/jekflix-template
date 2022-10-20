---
date: 2022-08-01 12:00:00
layout: post
title: This is your sign to personalize your products or services using ML 
subtitle: I personalized discounts for 1 Million retail customers during my summer internship 
description: I personalized discounts for 1 Million retail customers during my summer internship 
image: /assets/img/uploads/personalize.jpeg
optimized_image: /assets/img/uploads/personalize.jpeg
category: datascience
tags:
author: meinlee
paginate: false
---

<div id="toc_container">
<h2 class="toc_title">Table of Contents</h2>
<ul class="toc_list">
  <li><a href="#Acknowledgements">Acknowledgements</a></li>
   <li><a href="#Project Inspiration and Research">Project Inspiration and Research</a></li>
   <li><a href="#Working in Cross-Functional Teams">Working in Cross-Functional Teams</a></li>
   <li><a href="#Data Cleaning & Data Engineering">Data Cleaning & Data Engineering</a></li>
  <li><a href="#Building the Model">Building the Model</a></li>
  <li><a href="#A/B Testing">A/B Testing</a></li>
  <li><a href="#Implementation and Presentation">Implementation and Presentation</a></li>
  <li><a href="#Closing Thoughts">Closing Thoughts</a></li>
</ul>
</div>

<h2 id="Acknowledgements">Acknowledgements</h2>

This past summer, I had the pleasure of working as an Analytics intern at a large retail company and meeting over 20 interns from different departments. I did not know this going into the internship, but I've gained mentorship, industry experiences, and friendships that I will never forget. I'd like to preface this post by thanking everyone I've met over the short 3 months of Summer '22, and for giving me one of the best summer experiences yet.

In this post, I will share the end-to-end process of my internship project: generating personalized discounts, overcoming obstacles, and learning valuable lessons.

<h2 id="Project Inspiration">Project Inspiration and Research</h2>

![Personalization](/assets/img/uploads/personalization.jpg "Personalization")

Giving the right discount to the right people is known to make customers spend more with a store. 
As companies shift to the ability to promote discounts and promotions through digital marketing such as app notifications and email subscriptions, there is a need to identify the optimum amount for each customer -- a personalized discount that will incentivize them to spend more than usual. 

In fact, 78% of customers expect personalization, and 71% of customers are more likely to repurchase from companies that personalize experiences for their customers. 

Many companies have successfully implemented personalization strategies in their phone apps -- HelloFresh, Starbucks, Target, Puma, etc. The benefits of personalization can be summarized into four areas, represented by the blue arrows: 

![Benefits](/assets/img/uploads/benefits.png "Benefits")

This is the reason why Puma, for example, created email optimization marketing campaigns and ultimately achieved 5x Email-Attributed Revenue in 6 Months. 
 
<h2 id="Working in Cross-Functional Teams">Working in Cross-Functional Teams </h2>

Working in cross-functional teams is a highly transferable skill because it demands communication, collaboration, and sometimes even negotiation with people from different professional backgrounds. 

Generating personalization discounts is great, but useless if I can’t test it on real customers. This requires the marketing team’s help to push out discount notifications to email subscribers and app users, so I created a detailed project proposal to convince them that the time and energy that they will invest in my project is worth it. The proposal also includes a strict timeline, proposed results, and how my project will benefit their existing marketing strategies. 

After many rounds of research and discussion, I finally got the green light to start building the model!

In classes, the start of the project is <i>import pandas as pd</i>. In the industry, the start of a project involves crucial soft skills such as communication and collaboration.

<h2 id="Data Cleaning & Data Engineering">Data Cleaning & Data Engineering</h2>

The features below are among the 100+ features that were queried and built using SQL for the 1 Million customers that I plan to test on. Some features are basic demographic data that are readily available (e.g. age and education level), and some require more engineering such as the time elapsed between their first and second interaction with a discount. 

![Data Inputs](/assets/img/uploads/data_inputs.jpg "Data Inputs")

Although it may be tiring to stare at SQL queries all day – I got my very first pair of blue light glasses cus’ my eyes started hunting – having hands-on experience with SQL tricks like views, pivots, window functions, and subqueries is pretty cool.

Then comes the important (yes, very important, as repeated over and over again by university professors and tech bloggers) part – data cleaning and preprocessing. I encoded and normalized many features to get them into a clean format. Some of the work with cleaning were simultaneously performed when I built the features on SQL Server, and I also narrowed it down to 1 (out of 70) Million <i>active</i> customers only, meaning that at least I didn’t have to worry about sparse data.

However, I had to deal with skewed data which was resolved through resampling.

<h2 id="Building the Model">Building the Model</h2>

There are two stages in this phase:
1) Assigning discounts to each customer based on their transactional history
2) Predicting engagement with the assigned discount and making necessary changes 

First, the goal is to predict which discount among No Discount (0%), 20%, and 25% should be assigned to each customer, and these amounts were chosen because it was the most commonly engaged discount, hence more transactional data to work with. 

In order to determine the best assignment for each customer, I calculated the Conditional Average Treatment Effect (CATE) between No Discount (0%), 20%, and 25%. The effect is represented by the sales generated, and the assignment is generated based on the rules of the table below.

![CATE Table](/assets/img/uploads/CATE_table.jpg "CATE Table")

Now that each person is assigned a discount, I wanted to predict how likely would they actually use the discount.

In hindsight, perhaps 100+ features is an overkill. After applying the RFECV (Recursive Feature Elimination, Cross-Validated) sklearn package and Principal Component Analysis to the features, only 10% of them were chosen for optimal model performance. I guess that made sense since many transactional data were calculated from each other and probably correlate with each other. 

Between Random Forest and Logistic Regression, Random Forest reported a better precision, recall, and F1 score on the testing set. 

![Discount Predictions](/assets/img/uploads/discount_pred.jpg "Discount Predictions")

<h2 id="A/B Testing">A/B Testing</h2>

Theoretically, the steps for A/B testing are
1) Determine evaluation metric
2) Determine significance level and sample size
3) Decide the timeframe 
4) Coordinate implementation with Engineering & Marketing 
5) Randomly assign into control and treatment 
6) Check assumptions
7) Measure and analyze results 

### In Progress! Updating Soon! Interested in this post? 
<a href="https://docs.google.com/forms/d/e/1FAIpQLSfh1Kx8ftMOR92ijcBb_-K2OAv2XAnQlWChwuBG2vTGkkBeuQ/viewform?usp=sf_link">Sign up for my mailing list for updates!</a>

<div id="toc_container">
<h2 class="toc_title">Table of Contents</h2>
<ul class="toc_list">
  <li><a href="#Acknowledgements">Back to Top</a></li>
  <li><a href="#Acknowledgements">Acknowledgements</a></li>
   <li><a href="#Project Inspiration and Research">Project Inspiration and Research</a></li>
   <li><a href="#Working in Cross-Functional Teams">Working in Cross-Functional Teams</a></li>
   <li><a href="#Data Cleaning & Data Engineering">Data Cleaning & Data Engineering</a></li>
  <li><a href="#Building the Model">Building the Model</a></li>
  <li><a href="#A/B Testing">A/B Testing</a></li>
  <li><a href="#Implementation and Presentation">Implementation and Presentation</a></li>
  <li><a href="#Closing Thoughts">Closing Thoughts</a></li>
</ul>
</div>
.
.
.
.
.
.
.
.
.


