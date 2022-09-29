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
   <li><a href="#ETL and Data Migration to AWS">ETL and Data Migration to AWS</a></li>
  <li><a href="#Cloud Practioner Certification">Cloud Practioner Certification</a></li>
  <li><a href="#Recommendation Engine Research">Recommendation Engine Research</a></li>
</ul>
</div>

<h2 id="Reinforcement Learning for Autonomous Vehicle Simulation">Reinforcement Learning for Autonomous Vehicle Simulation</h2>

![Racing League](/assets/img/uploads/giphy_car.gif "Racing League")

AWS DeepRacer is a way of using Reinforcement Learning, an advanced machine learning technique, to train models. 

I participated in the AWS DeepRacer Intern League, where Amazon interns from all over the world train a reinforcement learning model to deploy onto an autonomous vehicle in a simulated racing environment. A big part of an RL model is the reward function which rewards the vehicle with points if it performs a correct action, such as not going off-track, or accelerating at the right time. Similarly, the vehicle is heavily rewarded for completing the track and penalized for actions such as going off track.

My strategy for the competition is to constantly examine the training metrics of rewards and track completion, then systematically tweak my reward function and fine-tune the hyperparameters. After over 10 hours of coding the reward function and iteratively training and tweaking parameters, I entered my model into the league and won top 10 based on the duration of three track completions. I was also very proud to represent team Malaysia and even more grateful for the opportunity to get my hands dirty with Reinforcement Learning.

<h2 id="NLP Automation">NLP Automation</h2>

![AWS Automation](/assets/img/uploads/automation.png "AWS Automation")

AWS Asia worked on many high-valued projects (+$100K) but there are no compilation of reports and no knowledge bank that provides advice for future project managers. 

I came up with the idea to build an automation with AWS resources to read and parse the texts, then generate a data report that is interpretable and insightful. In order to do so, I taught myself cloud computing knowledge from scratch. I read through every necessary documentation to understand the code, consulted and shadowed my mentors who have experience building automations, and I was not afraid to ask questions or advice whenever I was stuck. 

The diagram above is the end to end flow of my automation which kickstarts by uploading a CSV file to an S3 Bucket. A Lambda function is triggered at each step to activate AWS resources. For example, Amazon Comprehend to extracts keywords, AWS Glue to store keywords in a database, Amazon Athena to query the database, and Amazon Quicksight to generate data visualizations. 

When the automation was complete, I took a few more days to ask for feedback, make final tweaks to improve usability, and made sure the final product is a clear and useful asset to the company. 

The end product for my automation only requires one button click, automatically categorizes projects, cuts down analysis time from weeks to within 20 minutes, and provides project managers with a quick overview of lessons learnt and advice from previous projects.

I am incredibly grateful for my mentors, manager, fellow interns, and the sea of documentations that helped me achieve this. 

<h2 id="ETL and Data Migration to AWS">ETL and Data Migration to AWS</h2>

<a herf="https://aws.amazon.com/blogs/big-data/migrate-terabytes-of-data-quickly-from-google-cloud-to-amazon-s3-with-aws-glue-connector-for-google-bigquery/">Migrate terabytes of data quickly from Google Cloud to Amazon S3 with AWS Glue Connector for Google BigQuery</a>
For this project, my team followed this documentation closely.

Along with a team of solution architects and AI/ML enginners, I worked on a project to migrate terabytes of data from Google Cloud to Amazon S3 for a major telecommunication company.

Our team was tasked with building and automating an ETL process using AWS resources, using <a href="https://aws.amazon.com/glue/">AWS Glue</a> as the main component to migrate data into Amazon’s storage (<a href="https://aws.amazon.com/s3/">S3</a>). My role was to write and validate JSON scripts that will create ETL jobs on AWS Glue. After the scripts were developed, we sent them to our client to streamline current and future data migration processes. In other words, all the client would have to do is upload the JSON file onto <a href="https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html">AWS CloudFormation</a>. 

My role was essential in the data migration process because the JSON scripts contain essential and detailed information on how the cloud resources were going to be set up. (Many security settings and configurations tailored towards the client's needs). These resources were connected by <a href="https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html">AWS Lambda functions</a>, not just for data migration, but also to pipeline data as inputs into machine learning models.

Once again, I am incredibly grateful for everyone who have supported my internship journey. I started my intership with no cloud experience, but participated in two cloud automations --  thanks to the amazing and inspiring people that I have had the priveledge to meet.

<h2 id="Cloud Practioner Certification">Cloud Practioner Certification</h2>

![CCP](/assets/img/uploads/cert.png "CCP")

I read AWS Whitepapers and worked through practice exams on TutorialsDojo to study for the certification. I also made sure to familiarize myself with AWS resources by having hands-on experience with the tools, simultaneously learning how to build my NLP automation. 

As an AWS employee, I was very fortunate to have the certification costs reimbursed, but that did not take away my anxiety for the test. After over a month of preparation, I finally took the test... and I aced it (thankfully!). The hands-on experience was an overkill since theoretical knowledge is sufficient for the Cloud Practitioner Certification, but it did not hurt to have more experience!

Despite taking a longer time than intended to earn the certification (Some interns took the certification within their first two weeks!), I am proud of myself for overcoming the intimidation of learning a new technology. 

<h2 id="Recommendation Engine Research">Recommendation Engine Research</h2>

This was a research project for an AI/ML Consultant at AWS. I linked my research in another blogpost -- check it out here!

<h2 id="That's all!">Finishing Thoughts</h2>

Overall, I learned so much cloud computing knowledge from my internship, and met many amazing people. The Leadership Principles that I have learned through the Amazonian experience have guided me to this day and will continue to benefit me in the future. (LPs are must-knows not just in Amazon interviews, but throughout your internship and career!)

As the first intern cohort of AWS Malaysia, I am proud to have set the bar for future interns. My only feedback is that it could have been a more structured program. For example, a planned out 3-month project for the interns with predefined guidelines and expectations. Regardless, the support and mentorship that I have received was phenomenal! Everyone works hard to be the best leaders in their role, but also geniunely wants to see each other succeed. 

That is all! If you would like to learn more about what I worked on during my internship, or would like to talk about anything else, please reach out to me!

[Sign up for my mailing list](https://meinlee.netlify.app/contact/) to stay updated.

