# Metro-Journey-Optimization-Engine
## 📌 Overview
A graph-based metro navigation system that uses Dijkstra’s Algorithm to compute the shortest and most efficient routes between metro stations. The system models the metro network as a weighted graph, enabling optimized path computation for faster and smarter urban transit navigation.
--

## 🎯 Key Highlights
- 🧠 Graph-based metro network modeling  
- ⚡ Shortest path computation using **Dijkstra’s Algorithm**  
- 🌳 Balanced search using **AVL Tree (Self-balancing BST)**  
- 🚉 Supports multiple metro lines and interconnections  
- 🔍 Fast station lookup using indexed AVL structure  
- 💰 Fare calculation based on route traversal  
- 📂 File-driven metro line initialization (real-world simulation)

--

## 🏗️ System Architecture

The project is designed using multiple interconnected data structures:

### 1. Metro Network Representation
- Each **MetroLine** is a doubly linked list of `MetroStop`
- Each `MetroStop` contains:
  - Station name
  - Fare
  - Next / Previous station pointers

--

### 2. AVL Tree (Station Indexing)
- Each node represents a **station name**
- Stores multiple occurrences of the same station (from different lines)
- Ensures **O(log n)** search, insertion, and balancing
- Enables fast station lookup across metro lines

--

### 3. Path Finding System
- Uses a **custom path exploration mechanism**
- Tracks routes using a `Trip` history chain
- Explores possible routes using queue-based traversal
- Computes:
  - Shortest valid path
  - Total fare cost

--

## ⚙️ Core Algorithms Used

### 📍 Dijkstra-like Path Exploration
Used conceptually for optimal route discovery by exploring minimum-cost paths across connected stations.

### 🌳 AVL Tree Balancing
Ensures:
- Balanced BST height
- Efficient station search operations
- Prevents skewed tree formation
--

## 📥 Input Format (Metro Files)

Each metro line is stored as a `.txt` file:

