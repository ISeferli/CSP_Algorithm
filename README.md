# CSP_Algorithm-COM311
------------------------
Assignment
Course: COM 311 - Artificial Intelligence

Seferli Iliodora 2017030094
------------------------

------------------------
I. Java Classes         
------------------------
Algorithm.java		 Code implementing Backtracking algorithm for CSP use
Main.java		 Main program
Node.java		 Node that keeps each letter of the words given and its value

------------------------
II. Requirements
------------------------
Any Java IDE

------------------------
III. Execution
------------------------
Running the main program will give the result of the cryptarithmetic problem that it has acquired as an input. Specifically, the program will require from the user as an input the
words given from the riddle, its result and in which arithmetic system it has been computed.

------------------------
IV. Design
------------------------
Backtracking algorithm is implemented in the Algorithm class, which contains three useful functions that where inspired by https://www.tutorialspoint.com/Solving-Cryptarithmetic-Puzzles.
Function **assignWords(String first, String second, String res)**: 
The execution of the algorithm starts with this function. With the three words of the riddle as an input, I take each individual character of the words and put them in a HashMap named **usedLetter**, which has as a key the character given and as a value how many times it has appeared. Then the HashMap is used to fill a list of Nodes, so that the backtracking algorithm can assign later the cryptarithmitic number that each character was assigned to have the specific result. If the total number of characters is bigger than the given arithmetic base, the algorithm won't be able to find a solution as there won't be enough numbers to assign to the characters. In the end, the function calls the backtracking algorithm and starts the search of the solution.

Function **backtracking(int visitedChar, Node[] list, int n, String first, String second, String res)**:
