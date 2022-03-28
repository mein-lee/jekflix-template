---
date: 2021-05-30 11:06:42
layout: post
title: Internship at Amazon Web Services 
subtitle: Overview of my 3-Month remote internship with AWS
description: Overview of my 3-Month remote internship with AWS
image: <img src="/assets/img/uploads/aws.jpeg" 
     width="1200" 
     height="600" />
optimized_image: <img src="/assets/img/uploads/aws.jpeg" 
     width="1200" 
     height="600" />
category: internships
tags:
  - Amazon
  - AWS
  - internship
author: meinlee
paginate: false
---

> ##### Failure is a feeling long before it becomes an actual result. It's vulnerability that breeds with self-doubt and then is escalated, often deliberately, by fear.
> ###### Michelle Obama

<div id="toc_container">
<h2 class="toc_title">Highlighted Projects</h2>
<ul class="toc_list">
   <li><a href="#Reinforcement Learning for Autonomous Vehicle Simulation">Reinforcement Learning for Autonomous Vehicle Simulation</a></li>
  <li><a href="#NLP Automation">NLP Automation</a></li>
  <li><a href="#Cloud Practioner Certification">Gitlet</a></li>
  <li><a href="#Recommendation Engine Research">Scheme Interpreter</a></li>
</ul>
</div>

Fear. That's what I felt before, during, and I am still undergoing my internship. I will update this post when I complete it in August. 

# Reinforcement Learning for Autonomous Vehicle Simulation

![Racing League](/assets/img/uploads/giphy_car.gif "Racing League")

That's my (simulated) car! See how smoothly it manuevers each turn? I coded that!!! :)

AWS DeepRacer is a way of using Reinforcement Learning, an advanced machine learning technique, to train models. I coded a reward function, fed it to a model, and trained it for 10+ hours to recorgize turning angles, avoid going off-track, find the apex of a turn, and optimize speed. I learned to read patterns from each training iteration and made changes to my model that will help my autonomous vehicle manuever more smoothly. 

Then, I participated in the intern league, where Amazon interns from all over the world submit their trained autonomous vehicles to compete in three simulated races. My simulated vehicle and I proudly represented team Malaysia as we ranked top 10 in the final round. 

# NLP Automation

![AWS Automation](/assets/img/uploads/automation.png "AWS Automation")


AWS Asia worked on many high-valued projects (+$100K) but there are no compilation of reports and no knowledge bank that provides advice for future project managers. 

I came up with the idea to build an automation with AWS resources to read and parse the texts, then generate a data report that is interpretable and insightful. In order to do so, I taught myself cloud computing knowledge from scratch. I read through every necessary documentation to understand the code, consulted and shadowed my mentors who have experience building automations, and I was not afraid to ask questions or advice whenever I was stuck. 

The diagram above is the end to end flow of my automation which kickstarts by uploading a CSV file to an S3 Bucket. A Lambda function is triggered at each step to activate AWS resources. For example, Amazon Comprehend to extracts keywords, AWS Glue to store keywords in a database, Amazon Athena to query the database, and Amazon Quicksight to generate data visualizations. 

When the automation was complete, I took a few more days to ask for feedback, make final tweaks to improve usability, and made sure the final product is a clear and useful asset to the company. 

The end product for my automation only requires one button click, automatically categorizes projects, cuts down analysis time from weeks to within 20 minutes, and provides project managers with a quick overview of lessons learnt and advice from previous projects.

I am incredibly grateful for my mentors, manager, fellow interns, and the sea of documentations that helped me achieve this. 

# Cloud Practioner Certification

# Recommendation Engine Research


Please [sign up for my mailing list](https://meinlee.netlify.app/contact/) to stay updated.

Stay tuned!
