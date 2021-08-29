---
layout: project
type: project
image: images/hexsudoku_preview.png
title: Hexadecimal Sudoku Solver
permalink: projects/hexasudoku
# All dates must be YYYY-MM-DD format!
date: 2020-10-29
labels:
  - Java
  - Recursion
  - Backtracking
summary: I created a Hexadecimal Sudoku Solver for my ICS211 class using recursion method.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/hexsudoku_preview.png">
</div>


In my ICS211 course, I was tasked to implement a recursive method to find a solution to 16x16 Hexadecimal Sudoku. Professor Moore provided a format of the Sudoku code and our classmate have to implement the code. This particular assignment setted up by Sudoku is a 16x16 grid of integers with values of 0 to F. The valid answer for the Sudoku problem was each row, each column, and each 4x4 grid must have only one of 0 to F values without any duplicates. The recursive method to find the valid solution of the sudoku was the following:

  1. If all cells are filld, see if this Sudoku is valid. If it is valid, we have found a solution. If not, this Sudoku is not a solution. [Base case 1].
  2. If at least one cell is not filled, see what values are legal for this cell.

The algorithm of this assignment was an example of backtracking. From a starting point, it tries to search a vaild value and it retun to starting point if they cannot find an valid value. This algorithm keep tries to find a different option until all values have been tried.


Here is one example of my implentmention for the project, which to check Sudoku is solved or not:
```js
  public static boolean solveSudoku(int[][] sudoku) {

    // check sudoku is solved, if it is not solved then loop
    if (checkSudoku(sudoku, false)) {
      // loop through the sudoku row and column
      for (int row = 0; row < sudoku.length; row++) {
        for (int column = 0; column < sudoku.length; column++) {
          // if sudoku has a empty space then return fillCell method
          if (sudoku[row][column] == -1) {
            return fillCell(sudoku, row, column);
          }
        }
      }
    }
    return checkSudoku(sudoku, false);
  }
```

View the source code(https://github.com/cathy-kim95/Hexadeciaml-Sudoku).



