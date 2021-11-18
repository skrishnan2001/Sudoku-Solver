# Sudoku-Solver
An Android application built using Java that can solve a given valid Sudoku board

## Know the sudoku grid
Every sudoku puzzle involves a 9×9 grid of squares subdivided into 3×3 boxes. In total there are 81 squares on a sudoku grid and when the puzzle is completed each square will contain exactly one number.

## Rules of the Sudoku puzzle
Sudoku is a puzzle based on a small number of very simple rules:

- Every square has to contain a single number
- Only the numbers from 1 to 9 can be used
- Each 3×3 box can only contain each number from 1 to 9 once
- Each vertical column can only contain each number from 1 to 9 once
- Each horizontal row can only contain each number from 1 to 9 once

Once the puzzle is solved, this means that every row, column, and 3×3 box will contain every number from 1 to 9 exactly once. 

In other words, no number can be repeated in any 3×3 box, row, or column. 

## Find squares that can only be one number
When you start a new sudoku puzzle, some squares will already be filled with numbers. 

Based on how difficult the puzzle is, these numbers will ‘lock in’ specific numbers to specific squares. That is, squares where only one number can go without breaking any rules. 
As you start filling in squares that can only be one number, you’ll be adding more numbers to the grid which start to help ‘lock in’ additional numbers to additional squares.


Unless you’re completing an easy sudoku grid designed for beginners, you’ll soon run out of possible numbers you can ‘lock in’ for certain. When you get to this stage, it’s time to start pencilling in possible candidates for various cells. 

This is where you use small ‘pencil marks’ to list all the possible numbers a cell could contain based on the information you currently have. 

Instead of focusing on adding all the possible numbers to every empty cell, it’s easier and quicker to focus on certain cells and numbers at a time. 

## Sudoku Solver application
Harder sudokus may however require additional techniques to solve them. But for computers, this problem is quite an easy task. This application uses the concept of backtracking to 'lock in' the 
correct numbers in the appropriate grid.

### Algorithm
Like all other Backtracking problems, Sudoku can be solved by one by one assigning numbers to empty cells. Before assigning a number, check whether it is safe to assign. Check that the same number is not present in the current row, current column and current 3X3 subgrid. After checking for safety, assign the number, and recursively check whether this assignment leads to a solution or not. If the assignment doesn’t lead to a solution, then try the next number for the current empty cell. And if none of the number (1 to 9) leads to a solution, return false and print no solution exists.
