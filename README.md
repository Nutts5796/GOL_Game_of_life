This code is written using the lncurses library. 
The command in the terminal to compile the code is: 
    gcc -lncurses 
The command in the terminal to run the code is: 
    ./a.out < Space.txt

Conway’s Game of Life Implementation in C with ncurses

This repository contains an implementation of Conway’s Game of Life using the C programming language. The program utilizes the ncurses library to create a dynamic and interactive console-based visualization of cellular automata.

Features
    •    Dynamic Grid Size: Fixed grid of 25x80 cells.
    •    Interactive Speed Control: Adjust simulation speed using predefined keyboard shortcuts.
    •    Stability Check: Detects when the simulation reaches a static or repeating state.
    •    Dynamic Input Handling: Accepts an initial configuration of cells and handles user interaction seamlessly.
    •    Robust Simulation Logic: Implements the classic Game of Life rules:
    •    A live cell with 2 or 3 neighbors survives.
    •    A dead cell with exactly 3 neighbors becomes alive.
    •    All other cells die or remain dead.

How It Works
    1.    Matrix Initialization:
The program starts by reading the initial state of the grid from standard input.
    2.    Simulation Loop:
The main loop handles:
    •    User input for speed adjustment and termination.
    •    Updating the grid based on the rules of the Game of Life.
    •    Detecting static or empty states to end the simulation gracefully.
    3.    Cell Neighbor Calculation:
A specialized function calculates the number of neighbors for each cell, considering the grid as a toroidal surface (wrapping around edges).
    4.    Rendering:
Uses ncurses to render the grid, displaying live cells as 0 and dead cells as -.

Controls
    •    1: Slow speed
    •    2: Medium speed
    •    3: Fast speed
    •    q: Quit simulation

File Overview
    •    main Function: Orchestrates the simulation flow.
    •    Utility Functions:
    •    input_matrix: Reads the initial grid configuration.
    •    update_matrix: Updates the grid for the next generation and renders it.
    •    count_neighbors: Calculates the number of neighbors for a cell.
    •    decision: Applies the Game of Life rules.
    •    replace: Transfers the new state to the main grid.
    •    check: Verifies if the grid is static or repeating.
    •    change_speed: Handles user inputs for speed changes.
    •    count: Counts the number of live cells.
    
