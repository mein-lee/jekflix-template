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

[This game](https://sp21.datastructur.es/materials/proj/proj0/proj0) is so addictive that test running it was dangerously distracting. At least I know it works! 

The trickiest part was figuring out how to sum up the tile numbers systematically. Otherwise, I only needed to implement the 'swipe ups'. Swiping left, right and downwards holds the same logic as swiping up, but with different parameters passed into `setViewingPerspective(Side s)`. Neat! 

GIF of my test run [here](https://media.giphy.com/media/tRnqwjV2qRtptJnqj6/giphy.gif)

# Scheme Interpreter

Language: Python

![Scheme interpreter](/assets/img/uploads/hi.png "Scheme interpreter")

[This project](https://inst.eecs.berkeley.edu/~cs61a/fa20/proj/scheme/) involves writing an interpreter for the Scheme language. 

* **Read:** Parses user input (a string of Scheme code) into my interpreter's internal Python representation of Scheme expressions (the Pairs class).
* **Eval:** Evaluates Scheme expressions (represented in Python) according to various rules to obtain values. Mutually recursive functions parse Scheme tokens.
* **Print**: Prints the `__str__` representation of the obtained value.
* **Loop**: Reads and evaluates input until EOF or keyboard interrupt

Github repository linked [here](https://github.com/mein-lee/scheme_interpreter)

![My CS Professor thought this was funny, so I figured I'll use it this time](/assets/img/uploads/scheme.png "From the timeless XKCD — https://xkcd.com/297/")



# Ants vs. SomeBees

Language: Python

![Acknowledgement: CS61A Staff](/assets/img/uploads/plants.png "Acknowledgement: CS61A Staff")

Plants vs. Zombies? Never heard of that. I only know Ants vs. SomeBees. (Don't worry if you don't hear it. I was confused when I first heard it, too. Give it some time).

This is a [tower defense](https://secure.wikimedia.org/wikipedia/en/wiki/Tower_defense) game. As the ant queen, I populate my colony with the bravest ants I can muster. My ants must protect their queen from the evil bees that invade their territory. Irritate the bees enough by throwing leaves at them, and they will be vanquished. Fail to pester the airborne intruders adequately, and the colony will succumb to the bees' wrath. 

Inspired by PopCap Games' [Plants Vs. Zombies](https://www.ea.com/studios/popcap/plants-vs-zombies).

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