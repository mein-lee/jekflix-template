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
  - software
author: meinlee
paginate: false
---
Build a version control system that mimics Git. Implement the 2048 Game. Generate a 2D tile-based world... Berkeley CS projects really give you something to talk about. 

But not until they've made you lose sleep, stare at the screen for 8 hours straight (then burst into tears),  desperately beg TAs for guidance during Office Hours, scream at your project partner, develop PTSD......

Despite all that, I've learned *so much* from my CS classes at Cal. It definitely pushed me to my limits. Before taking just two classes (61A&B), I considered myself a pretty bad programmer. Now, I am proud to say that I am a not-so-bad programmer.

Projects ranked from lowest to highest diffculty level. References & Github repositories linked at the very bottom.

# 2048

Language: Java

![2048 Game Demo](https://sp21.datastructur.es/materials/proj/proj0/img/example-2048.gif "2048 Game Demo")

This game is so addictive that test running it was dangerously distracting. GIF of my test run [here](https://media.giphy.com/media/tRnqwjV2qRtptJnqj6/giphy.gif).

The trickiest part was figuring out how to sum up the tile numbers systematically. Otherwise, I only needed to implement the 'swipe ups'. Swiping left, right and downwards holds the same logic as swiping up, but with different parameters passed into `setViewingPerspective(Side s)`. Neat! 

# Ants vs. SomeBees

Language: Python

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

# Scheme Interpreter

Language: Python

![Scheme interpreter](/assets/img/uploads/hi.png "Scheme interpreter")

This project involves writing an interpreter for the Scheme language. 

* **Read:** Parses user input (a string of Scheme code) into my interpreter's internal Python representation of Scheme expressions (the Pairs class).
* **Eval:** Evaluates Scheme expressions (represented in Python) according to various rules to obtain values. Mutually recursive functions parse Scheme tokens.
* **Print**: Prints the `__str__` representation of the obtained value.
* **Loop**: Reads and evaluates input until EOF or keyboard interrupt

![Scheme joke](/assets/img/uploads/scheme.png "Scheme joke")

# Gitlet

Language: Java

Infamous. Notoriously tough. Unspeakable. Scandalous. Gitlet. 

# **Tile-Based World Generator**

Language: Java

![](/assets/img/uploads/screenshot-2021-05-29-at-9.43.45-pm.png)

Designed and implemented a 2D tile-based world exploration engine. My partner and I built software that generates worlds based on the user's input `seed`. The user will then explore by walking around and interacting with objects in that world from an overhead perspective.

We also added creative mechanisms like lore, game menu, animations, respawning, a "game over" state, etc. 

To me, the most challenging part of this project was not applying data structures or creating algorithms. Unlike other projects where I could code however and whenever I wanted, this project required great teamwork and communication skills among project partners. When faced with varying ideas and perspective inputs, it took a while to achieve cohesion, but the outcome was *so* worth it. Major shoutout to my project buddy Thanh -- we created our own world! 

This project definitely piqued my interest in software engineering. 

# References & Repositories

**2048** 

* [Project Spec](https://sp21.datastructur.es/materials/proj/proj0/proj0)
* [](https://sp21.datastructur.es/materials/proj/proj0/proj0)Repository

**Ants vs. Some Bees**

* [Project Spec](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/ants/)
* [](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/ants/)Repository
* PopCap Games' [Plants Vs. Zombies](https://www.ea.com/studios/popcap/plants-vs-zombies)

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