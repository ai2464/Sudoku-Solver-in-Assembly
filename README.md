# Assembly Sudoku Solver

## Overview
This project is an Assembly language implementation of a Sudoku solver. It efficiently solves Sudoku puzzles using advanced algorithms, all implemented in Assembly for optimal performance.

## Features
- **Efficient Solving Algorithm:** Utilizes a custom algorithm to solve Sudoku puzzles of varying difficulties.
- **Assembly Optimization:** Hand-crafted Assembly code for the MIPS architecture, ensuring maximum performance.
- **Robust Error Handling:** Includes comprehensive checks to ensure puzzle validity and solvability.

## Getting Started

### Prerequisites
- MIPS Assembly Simulator (e.g., MARS or SPIM)
- Basic understanding of Assembly language

### Installation
1. Clone the repository or download the source code.
```
git clone https://github.com/ai2464/Sudoku-Solver-in-Assembly.git
```
2. Open the `.s` file in your MIPS Assembly Simulator.

### Usage
1. Load a Sudoku puzzle into the program.
2. Run the solver.
3. View the solution output.

## Input Format

To solve a Sudoku puzzle using this solver, the puzzle must be formatted according to the following guidelines:

1. **Puzzle Representation:**
   - Each row of the Sudoku puzzle should be represented as a string of characters.
   - Each character represents a cell in the Sudoku grid.
   - Use digits `1` through `9` for pre-filled cells.
   - Use a period `.` or `0` (based on your implementation preference) for empty cells.

2. **Example Format:**
   - A typical 9x9 Sudoku puzzle should be represented as 9 lines of 9 characters each.
   - Example:
     ```
     53..7....
     6..195...
     .98....6.
     8...6...3
     4..8.3..1
     7...2...6
     .6....28.
     ...419..5
     ....8..79
     ```

3. **Uploading the Puzzle:**
   - The puzzle should be loaded into the solver by modifying the `.data` section of the Assembly code.
   - Replace the existing puzzle strings with the new puzzle strings in the provided format.

4. **Data Section Modification:**
   - Navigate to the `.data` section of the Assembly code.
   - Locate the existing Sudoku puzzle strings.
   - Replace them with your puzzle, following the format mentioned above.

5. **Consistency:**
   - Ensure that each row string is exactly 9 characters long.
   - Confirm that the total number of rows is 9 to represent a standard Sudoku grid.

By adhering to this input format, the solver can correctly interpret and process the puzzle for solving.

## Code Structure and Authorship

The Assembly Sudoku Solver is composed of various functions, each serving a specific role in the process of solving a Sudoku puzzle. Below is an outline of the code structure along with authorship details:

### Written by Me
- `num_candidates`: Determines the number of viable candidates for a given cell.
- `rule_out_of_cell`: Eliminates a candidate from a cell's possibilities.
- `count_solved_cells`: Counts the number of solved cells in the puzzle.
- `solve_board`: Main function to solve the Sudoku puzzle.

## How It Works
The Sudoku solver operates in several key steps:
1. **Cell Analysis:** Identifies the number of viable candidates for each cell.
2. **Rule Application:** Applies Sudoku rules to eliminate candidates.
3. **Recursive Solving:** Employs a backtracking algorithm for cells with multiple candidates.
4. **Solution Output:** Displays the solved Sudoku puzzle.

## Contributing
Contributions to enhance the solver or optimize the code are welcome. Please follow these steps:
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License
Distributed under the MIT License. See `LICENSE` for more information.

