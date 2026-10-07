Tic-Tac-Toe Search Agent: Minimax vs Alpha-Beta Pruning

Introduction

This project is a Tic-Tac-Toe search agent developed for SLE-3 of the course 02AML204 – Introduction to Artificial Intelligence.

The program compares two AI search algorithms:

- Minimax
- Minimax with Alpha-Beta Pruning

Both algorithms search possible moves and find the best result for player X when both players play perfectly.

Project Objective

The main objective of this project is to compare Minimax and Alpha-Beta Pruning based on:

- Running time
- Number of positions/nodes searched
- Search performance

The program uses three fixed test boards representing best, average and worst cases.

How the System Works

1. A Tic-Tac-Toe board is given as input.
2. The Minimax algorithm searches possible moves.
3. The Alpha-Beta algorithm searches the same board with pruning.
4. The number of visited positions is counted.
5. Both algorithms are executed multiple times.
6. Execution time is measured.
7. Results are saved in JSON files.

Main Components

1. Test Boards

Three fixed boards are used for testing:

- Best case
- Average case
- Worst case

2. Profiler / Runner

Runs both algorithms five times for each test board and measures execution time and node count.

3. Minimax Engine

Uses the normal Minimax algorithm.

- X is MAX
- O is MIN

4. Alpha-Beta Engine

Uses Minimax with Alpha-Beta pruning. It skips branches that cannot affect the final result.

5. Game Rules Module

Contains common game functions:

- "winner()"
- "get_moves()"

Both algorithms use the same game rules.

6. Results Output

The program displays the results and saves them in:

- "results.json"
- "profile.json"

Functions Used

winner(b)
get_moves(b)
minimax(b, player)
alphabeta(b, player, alpha, beta)
run_minimax(board)
run_alphabeta(board)

The program is written using functions only and does not use classes.

Design Decisions

Minimax and Alpha-Beta are implemented as separate search engines, but both use:

- The same game rules
- The same move order
- The same test boards

This makes the comparison fair.

The profiling code is kept separately in the Runner so that measurement does not change the algorithm.

The board is represented as a list of 9 cells, which keeps the implementation simple.

Technologies Used

- Python
- Minimax Algorithm
- Alpha-Beta Pruning
- "time"
- "cProfile"
- "pstats"
- "json"

AI Contribution

AI tool used:

Claude (Anthropic)

AI was used to help with the Minimax/Alpha-Beta code, profiling code, C4 architecture explanation, diagrams and report drafting.

The project structure, system choice, diagram checking and understanding of the implementation were done by me.

Conclusion

This project helped me understand how Minimax and Alpha-Beta Pruning work in a Tic-Tac-Toe game.

The main difference is that Alpha-Beta Pruning can skip unnecessary branches while producing the same final result as Minimax.

The C4 architecture also helped me understand the system from the overall level down to individual functions.
