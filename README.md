# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: After identifying the Naked Twins in the corresponding unit, Constraint Propagation is applied such that all the other boxes in the unit (other than the Twins) cannot have the possible values of the Twins.

In other words, all the other boxes in the corresponding unit of the Twins are constrained such that the set of their possible values cannot contain the possible values of the twins.

The constraint is valid because if 2 boxes within the same unit have the same possible values of length 2 eg: 4 or 5. Then only the following combinations are valid. First twin : 4 Second Twin : 5 or vice versa. If any other box within the same unit takes on value 4 or 5, then there would no longer be any valid solution because at least one of the twin would not have any solution.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The constraint that no boxes in the diagonal can contain the same digits is applied to solve this problem.

In order to introduce this constraint, 2 new units consisting of the 2 diagonals in the sudoku board were introduced. These units were taken into account when performing the Only Choice algorithm.

Constraint propagation is effectively used here to reduce the set of possible solutions by setting a constraint on the diagonals.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `test_solution.py` - Do not modify this. You can test your solution by running `python -m unittest`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login) for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

