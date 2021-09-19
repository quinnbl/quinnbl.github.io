---
layout: project
type: project
image: images/huligutta.jpg
title: Strategy Inference
permalink: projects/Strategy_Inference
# All dates must be YYYY-MM-DD format!
labels:
  - Python
  - numpy
  - pygame
  - tkinter
  - tensorflow
summary: A project I am a part of which aims to create a machine learning model to strategize in a virtual board game.
---

  I am a designer/developer in the Strategy Inference Vertically Integrated Project (VIP) working under Dr. Narayana Santhanam.

## Gameplay

  The game we are working with is called Huligutta, or Goats and Tigers, a game which involves two players playing asymmetrically. That is, they each have different pieces and different goals. One side controls three tigers, whose goal is to eat five goats. The tigers can eat goats by jumping over them, much like in checkers. The other side controls up to 15 goats, who start out off the board. The player takes 15 turns placing the goats, then moves the goats around after all have been placed. The goal for the goats is to block in all the tigers so they have no moves.

## My roles

  In this project my main goal is to create a machine learning model which will determine a strategy for the computer controlled side of our game. Some additional goals are making the game run smoother, as well as making the interface look more professional and reducing the number of bugs in the system. I am currently in the process of developing an algorithm which will determine a value based on any current state of the board, which works by adding positive value when there is a beneficial situation for the goats and adding negative value when there is a beneficial situation for the tigers. This will be used to determine a next move based on how it will affect the value of the board state, and will be pitted against other algorithms designed by two other teams in our project. 
