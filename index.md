---
layout: home 
title: AStar Algorithm C++ Project
---

Welcome to my AStar Algorithm C++ Project , where l use the algorithm to find the cheapest way to reach the path. This project demonstrates how the algorithm calculates the the different paths and chooses the one that best fits. This project idea demonstrates the implementation and testing of the A* pathfinding algorithm in a 5x5 grid using modern C++ in Visual Studio.


<img src="AStar images/Screenshot 2026-03-11 111715.png">
In my programmmer.h, I defined the main structure of the project the Programmer class. I chose to seperate the class declarations into the header file to follow the project guidelines as it is object oriented. My header file declares the data types I am using in my project, such as the grid  and coordinates and as well as the functions that will help me execute the A* algorithm. this separations between the declarations and implementation makes the code easier to maintain and understand. The difficulty I had with this header file was deciciding which functions should remain private. I needed to ensure that onlt the neccessary functions were exposed to other parts of the program while keeping my helper functions enclosed within the class.


<img src="AStar images/programmer-cpp.png">
In this file I use the functions that I made in my header file, I implemented the A* pathfinding algorithm, which searches for the shortest path between the two points on the 5x5 grid while avoiding the obstacles that I put in the grid. I chose to use the vector library to store the grid and the path data because they provide safer and more flexiible memory management. I also implemented a node structure to represent each position in the grid along with its associated cost values used by the A* algorithm. I chose to use nodes and costs from the research and videos I watched about the A* algorithm as the vidoes and websites all seemed to have the same idea in their algorithms. A challenging part of this for me was after it reaches its goal that it correctly tracked and rebuilt the path from the start point to the goal.
