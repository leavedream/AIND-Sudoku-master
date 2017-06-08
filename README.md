# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: First I find out all naked twins pairs. A pair of naked twins should follow below rules:
    (1) They belong to same unit.
    (2) They have same value
    (3) The length of the value is 2
   So I iterate through the unit list, and in each unit if there exists naked twins pair, for any other boxes in the same unit I remove the values that appear are the same as the values of the twins boxes.
   Then this naked_twins() function is invoked in the reduce_puzzle() function, similar to eliminate() function and only_choice() function.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: I created a variable called diag_units, similar to column_units and row_units, to store the two diagonal units, then add the diag_units to the unit list. So any constraint that applies to the column_units, row_units and squar_units will apply to diag_units automatically.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.