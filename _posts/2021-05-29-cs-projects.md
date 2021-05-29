---
date: 2021-05-29 08:57:07
layout: post
title: CS Projects
subtitle: Brief overview of my CS Projects. Can't say it was a smooth-sailing
  process, but completing them sure made me proud.
description: "Brief Overview of my CS Projects "
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559820489/js-code_n83m7a.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559820489/js-code_n83m7a.jpg
category: projects
tags:
  - CS
  - projects
  - berkeley
  - cal
  - software
  - computer
  - undergraduate
author: meinlee
paginate: false
---
Build a version control system that mimics Git. Implement the 2048 Game. Generate a 2D tile-based world... Berkeley CS projects really give you something to talk about. 

But not until they've made you lose sleep, stare at the screen for 8 hours straight (then burst into tears),  desperately beg TAs for guidance during Office Hours, scream at your project partner, develop PTSD......

Despite all that, I've learned *so much* from my CS classes at Cal. It definitely pushed me to my limits. Before taking just two classes (61A&B), I considered myself a pretty bad programmer. Now, I am proud to say that I am a not-so-bad programmer.

# 2048

Language: Java

![2048 Game Demo](https://sp21.datastructur.es/materials/proj/proj0/img/example-2048.gif "2048 Game Demo")

This game is so addictive that test running it was dangerously distracting. At least I know it works! 

The trickiest part was figuring out how to sum up the tile numbers systematically. Otherwise, we only needed to implement the 'swipe ups'. Swiping left, right and downwards holds the same logic as swiping up, but with different parameters passed into `setViewingPerspective(Side s)`. Neat! 

[Click Here for Project Spec](https://sp21.datastructur.es/materials/proj/proj0/proj0)

[Click Here for Gif of My Test Run](https://media.giphy.com/media/tRnqwjV2qRtptJnqj6/giphy.gif)

# Scheme Interpreter

Language: Python

![Scheme interpreter](/assets/img/uploads/hi.png "Scheme interpreter")

This project involves writing an interpreter for the Scheme language. 

* **Read:** Parses user input (a string of Scheme code) into our interpreter's internal Python representation of Scheme expressions (the Pairs class).
* **Eval:** Evaluates Scheme expressions (represented in Python) according to various rules to obtain values. Mutually recursive functions parse Scheme tokens.
* **Print**: This step prints the `__str__` representation of the obtained value.
* **Loop**: Read and evaluate input until an end of file or keyboard interrupt

  ![My CS Professor thought this was a good joke](/assets/img/uploads/scheme.png "From the timeless XKCD — https://xkcd.com/297/")