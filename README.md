# **TicTacToeBig**  
**Ultimate Tic-Tac-Toe Game – AI Player**

This repository contains an implementation of an AI player for the *Ultimate Tic-Tac-Toe* game, using the Minimax algorithm with Alpha-Beta pruning.

---

## **🧩 Overview**

Ultimate Tic-Tac-Toe is played on a 3×3 grid of smaller 3×3 Tic-Tac-Toe boards.  
The goal is to win three small boards in a row.  
The twist: the position of your move determines which board your opponent must play in next.

---

## **🤖 AI Features**

The AI player includes:

- **Minimax algorithm** with **Alpha-Beta pruning**
- **Iterative deepening** with time limits
- **Heuristic board evaluation** for decision-making

---

## **🚀 Getting Started**

### ✅ **Prerequisites**

- Java JDK 8 or higher  
- A game server that follows the protocol implemented in this client

---

### 🛠️ **Running the Application**

1. **Compile the Java files:**

   ```bash
   javac src/*.java
   ```
2. **Run the client:**
  ```bash
   java -cp src Client [IP_ADDRESS] [PORT]
   ```
---

## **🌐 Connection Options**

When you run the client, you can:

- Connect to **localhost** (`127.0.0.1`)
- Provide a **custom IP address and port**

If you run the client without arguments, you'll be prompted to choose one of these options.  
Alternatively, you can provide the IP address and port as command-line arguments:
---

## **⚙️ How It Works**

- The client connects to a game server that manages the game state  
- The server assigns you to play as **X (white)** or **O (black)**  
- When it's your turn, the AI will:
  - Analyze the current board state
  - Use **Alpha-Beta pruning** with **iterative deepening** to find the best move
  - Execute the move within a **3-second time limit**

---

## **🎮 Game Features**

- **Iterative Deepening**: The AI explores increasingly deeper levels as long as time allows  
- **Alpha-Beta Pruning**: Improves performance by skipping unpromising branches  
- **Move Counting**: Tracks the number of moves played throughout the game  
- **Board Visualization**: Renders the current state of the board in the console for easy tracking

---

## **📁 Implementation Details**

| **File**         | **Description**                                               |
|------------------|---------------------------------------------------------------|
| `BigBoard.java`  | Represents the 3×3 grid of smaller boards                     |
| `Board.java`     | Represents a single 3×3 Tic-Tac-Toe board                     |
| `CPUPlayer.java` | Implements the AI logic using Minimax and Alpha-Beta pruning |
| `Client.java`    | Handles communication with the game server                    |
| `Mark.java`      | Enum for cell values: X, O, or empty                          |
| `Move.java`      | Represents a move with row, column, and score                 |

---

## **⏱️ Performance**

The AI is optimized to respond within a **3-second time limit** by:

- Starting with a shallow search depth (e.g., 4)
- Increasing depth using **iterative deepening**
- Leveraging **Alpha-Beta pruning** to evaluate more positions in less time

---

## ✅ **Example Usage**

1. **Compile the source files:**
```bash
   javac src/*.java
  java -cp src Client 127.0.0.1 12345
```
If no arguments are provided, the program will prompt you to select a connection method (localhost or custom).

---

## 📌 **Notes**

- Make sure the **game server is running** before starting the client.
- The AI’s strength and behavior can be adjusted by editing heuristics and search depth in `CPUPlayer.java`.
- Console output includes a visualization of the current game board for easier debugging and tracking.
- The AI makes decisions under a **3-second time limit** using iterative deepening, which balances performance and depth of analysis.

---

## 📄 **License**

This project is licensed under the [MIT License](LICENSE).  
You are free to use, modify, and distribute this project under the terms of this license.

---

## 🙌 **Acknowledgments**

Huge thanks to my amazing teammates **Henri** and **Arnaud** for their collaboration, ideas, and dedication throughout this project.

Additional thanks to the open-source community for providing resources and inspiration related to:

- Game tree search algorithms
- Minimax and Alpha-Beta pruning optimizations
- Real-time decision-making techniques in AI

Your contributions made this project possible and more enjoyable!


