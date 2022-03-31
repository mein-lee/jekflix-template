---
date: 2021-05-30 11:06:42
layout: post
title: Internship at Amazon Web Services 
subtitle: Overview of my 3-Month remote internship with AWS
description: Overview of my 3-Month remote internship with AWS
image: /assets/img/uploads/aws.jpeg
optimized_image: /assets/img/uploads/aws.jpeg
category: internships
tags:
author: meinlee
paginate: false
---

<div id="toc_container">
<h2 class="toc_title">Highlighted Projects</h2>
<ul class="toc_list">
   <li><a href="#Reinforcement Learning for Autonomous Vehicle Simulation">Reinforcement Learning for Autonomous Vehicle Simulation</a></li>
  <li><a href="#NLP Automation">NLP Automation</a></li>
  <li><a href="#Cloud Practioner Certification">Gitlet</a></li>
  <li><a href="#Recommendation Engine Research">Scheme Interpreter</a></li>
</ul>
</div>

<h1 id="Reinforcement Learning for Autonomous Vehicle Simulation">Reinforcement Learning for Autonomous Vehicle Simulation</h1>

![Racing League](/assets/img/uploads/giphy_car.gif "Racing League")

That's my (simulated) car! See how smoothly it manuevers each turn? I coded that!!! :)

AWS DeepRacer is a way of using Reinforcement Learning, an advanced machine learning technique, to train models. I coded a reward function, fed it to a model, and trained it for 10+ hours to recorgize turning angles, avoid going off-track, find the apex of a turn, and optimize speed. I learned to read patterns from each training iteration and made changes to my model that will help my autonomous vehicle manuever more smoothly. 

Then, I participated in the intern league, where Amazon interns from all over the world submit their trained autonomous vehicles to compete in three simulated races. My simulated vehicle and I proudly represented team Malaysia as we ranked top 10 in the final round. 

<h1 id="NLP Automation">NLP Automation</h1>

![AWS Automation](/assets/img/uploads/automation.png "AWS Automation")


AWS Asia worked on many high-valued projects (+$100K) but there are no compilation of reports and no knowledge bank that provides advice for future project managers. 

I came up with the idea to build an automation with AWS resources to read and parse the texts, then generate a data report that is interpretable and insightful. In order to do so, I taught myself cloud computing knowledge from scratch. I read through every necessary documentation to understand the code, consulted and shadowed my mentors who have experience building automations, and I was not afraid to ask questions or advice whenever I was stuck. 

The diagram above is the end to end flow of my automation which kickstarts by uploading a CSV file to an S3 Bucket. A Lambda function is triggered at each step to activate AWS resources. For example, Amazon Comprehend to extracts keywords, AWS Glue to store keywords in a database, Amazon Athena to query the database, and Amazon Quicksight to generate data visualizations. 

When the automation was complete, I took a few more days to ask for feedback, make final tweaks to improve usability, and made sure the final product is a clear and useful asset to the company. 

The end product for my automation only requires one button click, automatically categorizes projects, cuts down analysis time from weeks to within 20 minutes, and provides project managers with a quick overview of lessons learnt and advice from previous projects.

I am incredibly grateful for my mentors, manager, fellow interns, and the sea of documentations that helped me achieve this. 

<h1 id="Cloud Practioner Certification">Cloud Practioner Certification</h1>

![CCP](/assets/img/uploads/cert.png "CCP")

I read AWS Whitepapers and worked through practice exams on TutorialsDojo to study for the certification. I also made sure to familiarize myself with AWS resources by having hands-on experience with the tools, simultaneously learning how to build my NLP automation. 

As an AWS employee, I was very fortunate to have the certification costs reimbursed, but that did not take away my anxiety for the test. After over a month of preparation, I finally took the test... and I aced it (thankfully!). The hands-on experience was an overkill since theoretical knowledge is sufficient for the Cloud Practitioner Certification, but it did not hurt to have more experience!

Despite taking a longer time than intended to earn the certification (Some interns took the certification within their first two weeks!), I am proud of myself for overcoming the intimidation of learning a new technology. 

<h1 id="Recommendation Engine Research">Recommendation Engine Research</h1>

This was a research project for an AI/ML Consultant at AWS. I linked my research in another blogpost -- check it out here!

<h1 id="That's all!">That's all!</h1>

Overall, I learned so much cloud computing knowledge from my internship, and met many amazing people. The Leadership Principles that I have learned through the Amazonian experience have guided me to this day and will continue to benefit me in the future. (LPs are must-knows not just in Amazon interviews, but throughout your internship and career!)

As the first intern cohort of AWS Malaysia, I am proud to have set the bar for future interns. My only feedback is that it could have been a more structured program. For example, a planned out 3-month project for the interns with set guidelines and expectations. Regardless, the support and mentorship that I have received was phenomenal! Everyone works hard to be the best leaders in their role, but also geniunely wants to see each other succeed. 

That is all! If you would like to learn more about what I worked on during my internship, or would like to talk about anything else, please reach out to me!

[Sign up for my mailing list](https://meinlee.netlify.app/contact/) to stay updated.

