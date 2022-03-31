---
date: 2021-05-29 08:57:07
layout: post
title: CS Projects
subtitle: Brief overview of my CS Projects. Can't say it was a smooth-sailing
  process, but completing them made me proud.
description: "Build a version control system that mimics Git. Implement the 2048 Game. Generate a 2D tile-based world...<br></br> Berkeley CS projects really give you something to talk about."
image: /assets/img/uploads/code.jpeg
optimized_image: /assets/img/uploads/code.jpeg
category: SWE
tags:
author: meinlee
paginate: false
---
Projects ranked from lowest to highest diffculty level.
<div id="toc_container">
<h2 class="toc_title">Table of Contents</h2>
<ul class="toc_list">
  <li><a href="#2048">2048</a></li>
  <li><a href="#Ants vs. SomeBees">Ants vs. SomeBees</a></li>
  <li><a href="#Scheme Interpreter">Scheme Interpreter</a></li>
  <li><a href="#Gitlet">Gitlet</a></li>
  <li><a href="#Tile-Based World Generator">Tile-Based World Generator</a></li>
  <li><a href="#References & Repositories">References & Repositories</a></li>
</ul>
</div>

Build a version control system that mimics Git. Implement the 2048 Game. Generate a 2D tile-based world... Berkeley CS projects really give you something to talk about. 

But not until they've made you lose sleep, stare at the screen for 8 hours straight (then burst into tears),  desperately beg TAs for guidance during Office Hours, lose hair, develop PTSD......

Despite all that, I've learned *so much* from my CS classes at Cal. It definitely pushed me to my limits. Before taking just two CS classes (61A&B), I considered myself a pretty bad programmer. Now, I am proud to say that I am a not-so-bad programmer.

# 2048

<b>Language: Java</b>

![2048 Game Demo](https://sp21.datastructur.es/materials/proj/proj0/img/example-2048.gif "2048 Game Demo")

This game is so addictive that test running it was dangerously distracting. GIF of my test run [here](https://media.giphy.com/media/tRnqwjV2qRtptJnqj6/giphy.gif).

The trickiest part was figuring out how to sum up the tile numbers systematically. Otherwise, I only needed to implement the 'swipe ups'. Swiping left, right and downwards holds the same logic as swiping up, but with different parameters passed into `setViewingPerspective(Side s)`. Neat! 

<h1 id="Ants vs. SomeBees"></h1>

# Ants vs. SomeBees

<b>Language: Python</b>

![Ants vs. SomeBees Banner](/assets/img/uploads/plants.png "Ants vs. SomeBees Banner")

Plants vs. Zombies? Never heard of that. I only know Ants vs. SomeBees. (Don't worry if you don't hear it. I was confused when I first heard it, too. Give it some time).

This is a [tower defense](https://secure.wikimedia.org/wikipedia/en/wiki/Tower_defense) game. As the ant queen, I populate my colony with the bravest ants I can muster. My ants must protect their queen from the evil bees that invade their territory. Irritate the bees enough by throwing leaves at them, and they will be vanquished. Fail to pester the airborne intruders adequately, and the colony will succumb to the bees' wrath. 

This project combines functional and object-oriented programming paradigms; involves understanding, extending, and testing a large program.

```python
class QueenAnt(ScubaThrower):  
    """The Queen of the colony. The game is over if a bee enters her place."""

    name = 'Queen'
    food_cost = 7
    queen_count = 0
    implemented = True  

    def __init__(self, armor=1):
        ScubaThrower.__init__(self, armor)
        self.queen_id = self.queen_count 
        QueenAnt.queen_count += 1
        
    def reduce_armor(self, amount):
            """Reduce armor by AMOUNT, and if the True QueenAnt has no armor
            remaining, signal the end of the game.
            """
            ScubaThrower.reduce_armor(self, amount)
            if self.queen_id == 0 and self.armor <= 0:
                bees_win()
```
<h1 id="Scheme Interpreter"></h1> 

# Scheme Interpreter

<b>Language: Python</b>

![Scheme interpreter](/assets/img/uploads/hi.png "Scheme interpreter")

This project involves writing an interpreter for the Scheme language. 

* **Read:** Parses user input (a string of Scheme code) into my interpreter's internal Python representation of Scheme expressions (the Pairs class).
* **Eval:** Evaluates Scheme expressions (represented in Python) according to various rules to obtain values. Mutually recursive functions parse Scheme tokens.
* **Print**: Prints the `__str__` representation of the obtained value.
* **Loop**: Reads and evaluates input until EOF or keyboard interrupt

![Scheme joke](/assets/img/uploads/scheme.png "Scheme joke")

<h1 id="Gitlet"></h1> 

# Gitlet

<b>Language: Java</b>

![Gitlet](/assets/img/uploads/gitlet.png "Gitlet")

The infamous Gitlet! Notoriously known as the toughest project in CS61B (Data Structures).

This project implements a simpler version of the popular version-control system, Git.
The main functionalities that Gitlet support are **Init, Add, Remove, Commit, Checkout, Log, Branch, Reset, Merge**

Below are the Data Structures and Algorithms that I used to implement Gitlet:

* **ArrayLists:** To link consecutive branches
* **Depth-first Search (DFS):** To traverse branches for checking out or merging purposes
* **HashMaps:** To store the unique SHA-1 id of each commit 
* **Files:** To store the files of each commit
* **Trees and Blobs:** To store files and file contents
* **Serialization:** Serialize file contents as to not lose the state of my program across multiple runs (Persistence)

<h1 id="Tile-Based World Generator"></h1> 

# **Tile-Based World Generator**

<b>Language: Java</b>

![](/assets/img/uploads/screenshot-2021-05-29-at-9.43.45-pm.png)

My partner and I designed and implemented a 2D tile-based world exploration engine. We built software that generates worlds based on the user's input `seed`. The user will then explore by walking around and interacting with objects in that world from an overhead perspective.

We also added creative mechanisms such as game menu, animations, respawning, a "game over" state, etc. 

Personally, the most challenging part of this project was not applying data structures or creating algorithms. Unlike other projects where I could code however and whenever I wanted, this project required great teamwork and communication skills among project partners. When faced with varying ideas and perspective inputs, it took a while to achieve cohesion, but the outcome was *so* worth it. Major shoutout to my project buddy <a href="https://www.linkedin.com/in/thanh--tran/">Thanh</a> -- we created our own world! :)

<h1 id="References & Repositories"></h1>

# References & Repositories

**2048** 

* [Project Spec](https://sp21.datastructur.es/materials/proj/proj0/proj0)
* [](https://sp21.datastructur.es/materials/proj/proj0/proj0)Repository

**Ants vs. Some Bees**

* [Project Spec](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/ants/)
* [](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/ants/)Repository
* [PopCap Games' Plants Vs. Zombies](https://www.ea.com/studios/popcap/plants-vs-zombies)

**Scheme Interpreter**

* [Project Spec](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/scheme/)
* [Repository](https://github.com/mein-lee/scheme_interpreter)

**Gitlet**

* [Project Spec](https://sp21.datastructur.es/materials/proj/proj2/proj2)
* Repository

**Tile Based World Generator**

* [Project Spec](https://sp21.datastructur.es/materials/proj/proj3/proj3#introduction)
* Repository
* [Youtube video walkthrough](https://www.youtube.com/watch?v=O4LYj1ILTfU)
