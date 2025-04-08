# TicTacToeBig
Ultimate Tic-Tac-Toe Game - AI Player
This repository contains an implementation of an AI player for the Ultimate Tic-Tac-Toe game, using the Minimax algorithm with Alpha-Beta pruning.


Overview
Ultimate Tic-Tac-Toe is played on a 3×3 grid of 3×3 Tic-Tac-Toe boards. The goal is to win three small boards in a row. The twist is that the position of your previous move determines which board your opponent must play in next.

The AI uses:


Minimax algorithm with Alpha-Beta pruning
Iterative deepening with time limits
Heuristic board evaluation
Getting Started
Prerequisites
Java JDK 8 or higher
A game server that follows the protocol implemented in this client
Running the Application
Compile the Java files:


javac src/*.java
Run the client:


java -cp src Client [IP_ADDRESS] [PORT]
Connection Options
When you run the application, you have two options to connect:


Localhost (127.0.0.1)
Custom IP address and port
If you run the client without arguments, you'll be prompted to choose one of these options. Alternatively, you can provide the IP address and port as command-line arguments.


How It Works
The client connects to a game server that manages the game state
The server assigns you to play as X (white) or O (black)
When it's your turn, the AI will:
Analyze the current board state
Use Alpha-Beta pruning with iterative deepening to find the best move
Execute the move within a 3-second time limit
Game Features
Iterative Deepening: The AI searches deeper levels until a time limit is reached
Alpha-Beta Pruning: Optimizes the search by skipping branches that won't influence the final decision
Move Counting: Tracks the total number of moves played
Board Visualization: Displays the current state of the game board in the console
Implementation Details
BigBoard.java: Represents the 3×3 grid of smaller boards
Board.java: Represents a single 3×3 Tic-Tac-Toe board
CPUPlayer.java: Implements the AI logic using Minimax and Alpha-Beta pruning
Client.java: Handles communication with the server
Mark.java: Enum representing X, O, or empty cells
Move.java: Represents a move with row, column, and score
Performance
The AI is designed to make decisions within a 3-second time limit by:
Starting with a shallow search depth (4)
Incrementally increasing depth as time allows
Using effective pruning to explore more nodes
