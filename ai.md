---
title: Artificial Intelligence
---
<nav>
  <a href="/">About</a>
  <a href="/ai" class="active">Artificial Intelligence</a>
  <a href="/software">Software Development</a>
  <a href="/network">Networking and Architecture</a>
  <a href="/mobile">Mobile Programming</a>
  <a href="/other">Logical and Functional Programming</a>
</nav>

<style>
nav {
  display: flex;
  gap: 20px;
  margin-bottom: 40px;
}
nav a {
  color: #00ffff;
  text-decoration: none;
  font-weight: bold;
  padding: 6px 12px;
  border: 1px solid #00ffff;
  border-radius: 4px;
  transition: background 0.2s, color 0.2s;
  font-size: 13px;

}
nav a:hover {
  background: #00ffff;
  color: #000;
}
nav a.active {
  background: #00ff00;
  color: #000;
  border-color: #00ff00;
}
</style>

# Artificial Intelligence

## Prison Dodgeball! Ballistic Trajectory Prediction and Finite State Machines

This project involves two parts. The first involves implrmenting the ballistic trajectory prediction for projectiles as well as shot selection logic (deciding when to throw dodgeballs). For implementation, I use Millington's static target method with iterative refinement.
The second part involves using Finite State Machines to have AIs that can defeat the other AIs in a game of prison ball. Naturally, it uses the algorithms from part 1. The results are shown below. The numbers on the sides are the current number of games won.
<video controls="controls" src="vids/gameai.mov" style="width: -webkit-fill-available">
    Your browser does not support the HTML5 Video element.
</video>

**Race Track: Fuzzy Logic**
Using the FuzzyLogic library by t0chas, I created a fuzzy logic control for my vehicle to drive along the road and not fall off. It does its best not to lose any speed. Results can be seen below.
<video controls="controls" src="vids/gameai7.mov" style="width: -webkit-fill-available">
    Your browser does not support the HTML5 Video element.
</video>

## Procedural Content Generation With Perlin Noice

Using Perlin Noice generation with a hierarchical set of generation rules, I made a complex heightmap terrain.

My pcg terrain consists of three biomes. I named them mountains, foresty plains, and wavy river. Each of these terrains use the trapezoid function to transition
from one to the other. The mountain has a mountain base(name) which is responsible for making the mountain base, along with detail(name) , which is used to create details, 
just like in the demo video. The foresty plain is similar in that it uses a plain base, and then adds details using the plain detail(name) . Trees were also
added by zeroing out of the parrent and using a customized mapping curve with perlin noise. In the wavy river biome, we can see that the waves are quite big. I have 
a child called river level (name)  to control the level of the river, as well once again a child called river detail to alter the waves of the river.
![](images/pcgforestyplain.PNG)
![](images/pcgoverview.PNG)
![](images/pcgwavyriver.PNG)

## Hidden Markov Models! Sign Language


This project involves using the coordinates of the hand and thumbs to analyze sign language. After building an HMM, I built a Viterbi Trellis and return the sequence of states along with the confidence probability based on the evidence input. As of right now, the project involves deciphering only the following three words.

Alligator, Nuts, and Sleep


<img width="230" height="150" src="images/alligator-singlesign-00000015.gif"> <img width="230" height="150" src="images/nuts-singlesign-00000016.gif"> <img width="230" height="150" src="images/sleep-singlesign-00000001.gif">


Below is some example test runs:

<img width="500" height="330" src="images/hmm.png">


## Machine Learning for Trading

This project involes using machine learning techiques to help trade stocks The entire paper on the project can be found here.

As a brief overview, one of the techniques used was random forests and it was able to beat out our manual technique by quite a bit. The manual technique is a using basic logic of Bollinger Bands and SMA (and other financial techniques) to act upon the stocks. A snippet of the results can be seen below.

<img width="500" height="330" src="images/ml4.png">


## Q Learning Robot

This projects involves implementing Q-Learning and Dyna-Q algorithms in a game setting to practice reinforcement learning. The game world is a simple field with each field containing one of the following.
0: blank space. 
1: an obstacle. 
2: the starting location for the robot. 
3: the goal location. 
5: quicksand. 
The rules for the rewards are as follows.
-1: if the robot moves to an empty or blank space, or attempts to move into a wall 
-100: if the robot moves to a quicksand space 
1: if the robot moves to the goal space 

After impleneting the Q-Learning algorithm, Dyna-Q was also implemented so that our AI agent could "hallucinate" extra experiences. Below is a sample run of a difficult course where we can see the dyna score helped improve the non-dyna score quite a bit.

<img width="500" height="330" src="images/qlearning.png">

## Colorization!

This project involves practicing computer vision along with supervised and unsupervised colors without any ML frameworks. The Agent takes in an image, greyscales it, and then divides it into two portions. It then uses the left half as training data in order to recolor the right half of the image. Here the Basic image uses K-means clustering as a way to simplify the process to recolor the image. The Improved Agent, is a mini neural network that uses gradient descent as its main means of minimizing the loss function.

Below is the original image, followed by the results of the of the basic and improved agents respectively.


    
![](images/tmp2.jpeg)


![](images/basic.png)


![](images/improve.png)





## Search and Destroy!

This project involves an agent searching for a target through flat areas, hills, forests, and caves. Each terrain introduces a different difficulty in terms of actually being able to find the target as the target is good at hiding! The objective is for the agent to find the target in as few searches as possible as well as minimize the distance travelled. The project was made in pygames and was done to help supplement understanding of modeling knowledge and beliefs and practice the use of bayesian theory.

![](images/sedes.PNG)

Below is a more detailed report on the project.
[Search and Destroy Report](reports/searchdestroy.pdf)



## MineSweeper!

In this project, I first created a game of Minesweeper in pygames. The game assets are thanks to GooseNinja from itch.io. I then made four different agents to play the game. The Basic Agent just plays with basic logic in a single case. The Improved Agent plays the game as a constraint satisfaction problem and projects it's own possible solutions. The Global Improved Agent gets additional information of the total number of cells in its knowledge base, and the second improved Agent takes a simulated annealing approach to cells it deems risky in its projected solutions.
<p align="center">
<video controls="controls" src="vids/mimp.mp4" style="width: -webkit-fill-available">
    Your browser does not support the HTML5 Video element
</video>
</p>
Below is a more detailed report on the project.
[MineSweeper Report](reports/minesweep.pdf)



## The Maze is On Fire!

In this project, I worked with a partner and created an AI that attempts to reach the goal in a maze. The maze is a square and the AI will be unable to travel through walls or ”occupied cells”. In addition, the maze may be set on fire. In this case, the fire will spread with each move of the AI.This project is done in Python and Pygames is used for the GUI. Numpy and matplotlib were used for the graphs in the report. In the report below. Below are some sample images. In the first is an Agent performing DFS search in a 200x200 maze without any fire in it's way. The latter recomputes the shortest path using the A* algorithm, while exercising "caution" to account for future states.

<p align="center">
  <img src="images/200.PNG">
</p>
<p align="center">
  <img src="images/strat3.PNG">
</p>



Below is a more detailed report on the project.
[FireMaze Report](reports/fmazereport.pdf)
