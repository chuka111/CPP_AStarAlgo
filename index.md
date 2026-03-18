---
layout: home 
title: AStar Algorithm C++ Project
---

## **Introduction**
Welcome to my AStar Algorithm C++ Project , where l use the algorithm to find the cheapest way to reach the path. This project demonstrates how the algorithm calculates the the different paths and chooses the one that best fits. This project idea demonstrates the implementation and testing of the A* pathfinding algorithm in a 5x5 grid using modern C++ in Visual Studio.

### **Project Set-Up**
For the A* pathfinding algorithm, it is an object oriented style project with 5 files: tesprogrammer.h, testprogrammer.cpp, programmer.h, programmer.cpp, main.cpp

### **Programmer.h**
<img src="AStar images/Screenshot 2026-03-11 111715.png">

In my programmmer.h, I defined the main structure of the project the Programmer class. I chose to seperate the class declarations into the header file to follow the project guidelines as it is object oriented. My header file declares the data types I am using in my project, such as the grid  and coordinates and as well as the functions that will help me execute the A* algorithm. this separations between the declarations and implementation makes the code easier to maintain and understand. The difficulty I had with this header file was deciciding which functions should remain private. I needed to ensure that onlt the neccessary functions were exposed to other parts of the program while keeping my helper functions enclosed within the class.

### **Programmer.cpp**
<img src="AStar images/programmer-cpp.png">

In this file I use the functions that I made in my header file, I implemented the A* pathfinding algorithm, which searches for the shortest path between the two points on the 5x5 grid while avoiding the obstacles that I put in the grid. I also used namespaces to organise the code and to avoid potential naming conflicts. I used an anonymous namespace to define the internal structures  like Node that gets used by the A* algorithm. By me placing these in the anonymous namespace, I ensured that they are only accessible within my programmer.cpp and cannot be used anywhere else in the project. This improves encapsulation and prevents unintended interactions between different parts of the codeI chose to use the vector library to store the grid and the path data because they provide safer and more flexiible memory management. I also implemented a node structure to represent each position in the grid along with its associated cost values used by the A* algorithm. I chose to use nodes and costs from the research and videos I watched about the A* algorithm as the vidoes and websites all seemed to have the same idea in their algorithms. A challenging part of this for me was after it reaches its goal that it correctly tracked and rebuilt the path from the start point to the goal. I overcame it by storing the parent of each node whenever a shorter path was discovered and then reconstructing the path by iterating backwards through these stored parent nodes until the starting position was reached.  

### **Testprogrammer.h**
<img src="AStar images/test.h.png">

Along with the guideline for this A* project we had to make test files, so I implemnted a header file that calls my test CPP file to run all the tests. Testing is an important part of this projet as it helps us to verify that all aspects of the algorithm works correctly under different conditions. The main issue for me with this was figuring out what parts of the code needs to be tested to ensure that the algorithm behaved correctly when being run. To solve this I used AI to help me to figure it out. The prompt I asked was "What unit tests should I create for a C++ program that implements the A* pathfindingon a 5x5 grid. The program uses a class based structure and vectors to store the grid. The test should check basic functionality and important cases such as when a path exists, when the start and goal are the same and when the start or goal is blocked and when no path is possible."

### **Testprogrammer.cpp**
<img src="AStar images/test.cpp.png">

My testprogrammer.cpp file contains the implementation of the unit tests declared in the header file. In this file, I created several tests to verify that the A* pathfinding algorithm functions correctly under different conditions. These tests check scenarios such as when a path exists between two points, when the start and goal positions are the same, when the start or goal position is blocked, and when no valid path can be found due to obstacles. At the end of the file I have a function called runAllTests that stores all the test functions I made and its called at the very start of my main.cpp file. All these test functions are grouped together in a namespace. this helps me to clearly separate testing logic from the main implementation and improves the overall structure of the project. 
The grid is created in both testprogrammer.cpp and main.cpp, but for different purposes. For testprogrammer.cpp I created the grid structures, but they are used for testing rather than demonstration. I implemented a helper function to generate an empty 5x5 grid, which was then modified to simulate different screnarios such as blocked paths or unreachable goals. This approach allowed to test the algorithm under multiple conditions and ensures its correctness. Doing this method allowed me to isolate testing from main.cpp improving the overall reliabilty of the project.
To help me identify appropriate test cases, I used AI assistance to suggest common scenarios that should be tested in a pathfinding algorithm. This helped ensure that the tests covered both normal operation and potential edge cases. I then implemented these suggested tests in C++ to validate that the algorithm behaved as expected. One challenge during this process was designing tests that were meaningful but still simple enough to clearly verify the behaviour of the algorithm. By focusing on a small set of key scenarios, I was able to create tests that effectively confirmed the correctness of the implementation.

### **Main.cpp**
<img src="AStar images/main.png">

In my main file it brings all the components of the prooject together. This file starts off by running all the tests from my testprogrammer.cpp file to verify that the algorithm is functioning correctly before it starts demonstrating the A* pathfinding algorithm on the same 5x5 grid. 
I defined another 5x5 grid in this file to demonstrate the behaviour of the A* pathfinding algorithm. This grid contains a combination of free cells and obstacles, allowing the program to calculate and display a valid path from the start position to the goal. The purpose of defining the grid in this file is to provide a clear and practical example of how the algorithm works, making it easier to visualise the final output.
I chose this structure so that it validates it first before anything else, then demonstrates the algorithm in action. This for me was the least complex and straightforward for me as most of the challenging work was done in the programmer.cpp and testprogrammer.cpp. I just had to make sure that everything linked up correctly and that the output displayed everything cleary for us to understand.


## **Future Improvements**
One potential improvement to this project that I would make would be to allow the grid size to be dynamic rather than fixed at 5x5 since the grid is hardcoded which limits the flexibility of the algorithm. I would also allow the user to be able to make their own grids on the UI so that they can pick where they want the obstacles on the grid rather than hardcoding the obstacles in.
Another improvement that I make would be extending the algorithm to support diagonal movement. Currently the algorithm only is limited to four directions: up,down, left right. Allowing diagonal movement would make the pathfinding more realistic and efficient in certain scenarios.


## **References**
[1]"A* Search Algorithm," GeeksforGeeks. [Online]. Available: https://www.geeksforgeeks.org/dsa/a-search-algorithm/. 
