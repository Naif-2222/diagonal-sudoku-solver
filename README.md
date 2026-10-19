# diagonal-sudoku-solver
An AI rule based agent that solves Diagonal Sudoku puzzles using constraint propagation (Naked Twins) and Depth-First Search (DFS).

# Symbolic AI: Diagonal Sudoku Solver

A Classical AI agent designed to solve standard and diagonal Sudoku puzzles. 
Unlike probabilistic machine learning or neural networks, this project utilizes **Symbolic AI** techniques to frame the game as a formal Constraint Satisfaction Problem (CSP). 

By representing the board state logically, the agent deterministically solves complex, heavily constrained puzzles by alternating between rule-based constraint propagation and recursive search tree exploration.

## Classical AI Techniques Used

This agent solves puzzles by alternating between two core strategies:
# Diagonal Sudoku Solver

An artificial intelligence agent designed to solve standard and diagonal Sudoku puzzles. This project demonstrates the application of constraint satisfaction algorithms and search tree techniques to solve complex, heavily constrained state-space problems.

## Artificial Intelligence Techniques Used

This agent solves puzzles by alternating between two core AI strategies:

1. **Constraint Propagation:** The agent systematically applies logical rules to reduce the state space of the board. 
   * **Eliminate:** If a box has a single assigned value, that value is removed from the possibilities of all its peers.
   * **Only Choice:** If a unit (row, column, 3x3 square, or diagonal) has only one valid box for a specific digit, that digit is assigned to that box.
   * **Naked Twins:** If two boxes in the same unit have the exact same two possible digits, those two digits are eliminated from all other unassigned boxes in that unit.

2. **Depth-First Search (DFS):** When constraint propagation stalls and cannot deduce the next move, the agent uses DFS to explore the search tree. It selects the box with the fewest remaining possibilities, guesses a valid digit, and recursively attempts to solve the resulting board. If it hits a dead end, it backtracks.

## The Diagonal Constraint

In addition to the standard Sudoku rules (digits 1-9 in every row, column, and 3x3 block), this solver enforces a diagonal constraint. The two main diagonals of the board must also contain the digits 1-9 exactly once.

## Getting Started

### Prerequisites
* Python 3.x

### Running the Solver
To execute the solver and visualize the output in the terminal:
```bash
python solution.py
