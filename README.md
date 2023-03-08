# HogGame

* This project is a modified version of UCB CS 61A - Hog project, available [here]

[here]: <https://inst.eecs.berkeley.edu//~cs61a/fa13/proj/hog/hog.html>

//TO DO
![](https://github.com/ZhihanTuo/HogGame/blob/995e383b5a88be5e0139a8b58d27b2e5522c3d14/images/Sample.gif?raw=true) 

### 1. Introduction
In Hog, two players alternate turns trying to reach 100 points first. On each turn, the current player chooses some number of dice to roll, up to 10. His/Her turn score is the sum of the dice outcomes, unless any of the dice come up a 1, in which case the score for his/her turn is only 1 point (the Pig out rule).

### 2. Special rules
To spice up the game, we will play with some special rules:

  - __Free bacon.__ If a player chooses to roll zero dice, he/she scores one more than the largest digit in her opponent's score.
    * _Example 1:_ if Player 1 has 42 points, Player 0 gains 1 + max(4, 2) = 5 points by rolling zero dice.
    * _Example 2:_ If Player 1 has 48 points, Player 0 gains 1 + max(4, 8) = 9 points.
    * _Example 3:_ If Player 1 has 7 points, Player 0 gains 1 + max(0, 7) = 8 points by rolling zero dice.


  - __Hog wild.__ If the sum of both players' total scores is a multiple of seven (e.g., 14, 21, 35), then the current player rolls four-sided dice instead of the usual six-sided dice.


  - __Swine Swap.__ If at the end of a turn one of the player's total score is exactly double the other's, then the players swap total scores. 
    * _Example 1:_ Player 0 has 20 points and Player 1 has 5; it is Player 1's turn. She scores 5 more, bringing her total to 10. The players swap scores: Player 0 now has 10 points and Player 1 has 20. It is now Player 0's turn.
    * _Example 2:_ Player 0 has 90 points and Player 1 has 50; it is Player 0's turn. She scores 10 more, bringing her total to 100. The players swap scores, and Player 1 wins the game 100 to 50.

### 3. Files

Files in the project:

* `hog.py`: Implementation of Hog
* `dice.py`: Functions for rolling dice
* `hog_gui.py`: The graphical user interface for Hog
* `ucb.py`: Utility functions for CS 61A
* `hog_grader.py`: Tests to check the correctness of your implementation.
* `autograder.py`: Utility functions for grading.
* `images`: A directory of images used by hog_gui.py

### 4. Running (GUI) - Tkinter required

To play against Bot, run:
```sh
$ python3 hog_gui.py -f
```
To play as both players, run:
```sh
$ python3 hog_gui.py
```
To see experiment result of strategy, run:
```sh
$ python3 hog.py -r
```
