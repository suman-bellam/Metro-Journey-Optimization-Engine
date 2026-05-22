# Metro-Journey-Optimization-Engine
A graph-based metro navigation system that uses Dijkstra’s Algorithm to compute the shortest and most efficient routes between metro stations. The system models the metro network as a weighted graph, enabling optimized path computation for faster and smarter urban transit navigation.

# 🚇 Smart Metro Route Optimizer

## 📌 Overview
Smart Metro Route Optimizer is a **graph-based urban transit navigation system** that models a real-world metro network using advanced **Data Structures and Algorithms**.  

It computes the **most efficient route between metro stations** using **Dijkstra’s Algorithm** and an **AVL Tree-based station indexing system**, ensuring fast lookup and optimal path computation across large metro networks.

---

## 🎯 Key Highlights
- 🧠 Graph-based metro network modeling  
- ⚡ Shortest path computation using **Dijkstra’s Algorithm**  
- 🌳 Balanced search using **AVL Tree (Self-balancing BST)**  
- 🚉 Supports multiple metro lines and interconnections  
- 🔍 Fast station lookup using indexed AVL structure  
- 💰 Fare calculation based on route traversal  
- 📂 File-driven metro line initialization (real-world simulation)

---

## 🏗️ System Architecture

The project is designed using multiple interconnected data structures:

### 1. Metro Network Representation
- Each **MetroLine** is a doubly linked list of `MetroStop`
- Each `MetroStop` contains:
  - Station name
  - Fare
  - Next / Previous station pointers

---

### 2. AVL Tree (Station Indexing)
- Each node represents a **station name**
- Stores multiple occurrences of the same station (from different lines)
- Ensures **O(log n)** search, insertion, and balancing
- Enables fast station lookup across metro lines

---

### 3. Path Finding System
- Uses a **custom path exploration mechanism**
- Tracks routes using a `Trip` history chain
- Explores possible routes using queue-based traversal
- Computes:
  - Shortest valid path
  - Total fare cost

---

## ⚙️ Core Algorithms Used

### 📍 Dijkstra-like Path Exploration
Used conceptually for optimal route discovery by exploring minimum-cost paths across connected stations.

### 🌳 AVL Tree Balancing
Ensures:
- Balanced BST height
- Efficient station search operations
- Prevents skewed tree formation

---

## 🧩 Classes Breakdown

| Class | Purpose |
|------|--------|
| `MetroStop` | Represents a metro station node |
| `MetroLine` | Doubly linked list of stations |
| `AVLNode` | Node of AVL tree storing station data |
| `AVLTree` | Balanced tree for fast station lookup |
| `Trip` | Stores traversal history (path tracking) |
| `Exploration` | Queue for BFS-style route exploration |
| `Path` | Stores final computed route and fare |
| `PathFinder` | Core engine for building tree and finding routes |

---

## 📥 Input Format (Metro Files)

Each metro line is stored as a `.txt` file:

