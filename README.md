<p align="center">
  <img src="https://img.shields.io/badge/Status-Active%20Development-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Version-1.0.0-818cf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-ISC-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Deployed-Vercel-black?style=for-the-badge&logo=vercel" />
</p>

<h1 align="center">⚡ AlgoPulse — DSA Visualizer</h1>

<p align="center">
  <strong>An interactive, real-time Data Structures & Algorithms visualization suite</strong><br/>
  Built with HTML5, CSS3, JavaScript, D3.js & jQuery
</p>

<p align="center">
  <a href="#-live-demo">Live Demo</a> •
  <a href="#-features">Features</a> •
  <a href="#%EF%B8%8F-architecture">Architecture</a> •
  <a href="#-modules">Modules</a> •
  <a href="#-progress-tracker">Progress</a> •
  <a href="#-getting-started">Setup</a>
</p>

---

## 🎯 About The Project

**AlgoPulse** is a modular web application that transforms abstract algorithmic execution steps into intuitive, real-time visual animations. Instead of memorizing pseudocode, students can *see* how sorting partitions work, *watch* pointers traverse linked lists, and *observe* tree nodes being inserted into BSTs — all step-by-step with color-coded highlights.

> The goal is to bridge the gap between theoretical DSA concepts and practical understanding through interactive, animated visualizations.

### 🔑 Key Highlights
- 🎨 **Modern Dark Theme UI** — Glassmorphism-inspired bento grid layout with smooth animations
- ⚡ **Real-Time Step-by-Step Execution** — Async/await-based animation engine with adjustable speed
- 📊 **5 Independent Visualizer Modules** — Sorting, Binary Search, Linked List, Binary Tree & Stack
- 🧮 **15+ Algorithms Visualized** — From Bubble Sort to Dijkstra's Pathfinding
- 📱 **Fully Responsive** — Works on desktop, tablet, and mobile viewports
- 🚀 **Zero Build Step** — Pure HTML/CSS/JS, no framework dependencies

---

## 🌐 Live Demo

> 🔗 **[Launch AlgoPulse →](#)** *(Deployed on Vercel)*

---

## ✨ Features

### 🔄 Sorting Algorithms Visualizer
| Algorithm | Time (Best / Avg / Worst) | Space | Visual Style |
|:---|:---|:---|:---|
| **Bubble Sort** | O(n) / O(n²) / O(n²) | O(1) | Aqua → Red (swap) → Green (sorted) |
| **Insertion Sort** | O(n) / O(n²) / O(n²) | O(1) | Red (shifting) → Green (placed) |
| **Heap Sort** | O(n log n) / O(n log n) / O(n log n) | O(1) | Yellow (root) → Pink (children) → Red (swap) |
| **Merge Sort** | O(n log n) / O(n log n) / O(n log n) | O(n) | Light Green (merge) → Yellow (sub-array) |
| **Quick Sort** | O(n log n) / O(n log n) / O(n²) | O(log n) | Red (pivot) → Green (partition boundary) |

### 🔍 Binary Search Engine
- Logarithmic bisection search on sorted arrays
- Step-by-step boundary elimination with highlighted `low`, `mid`, `high` pointers
- Real-time search path visualization

### 🔗 Linked List Operations
| Operation | Time Complexity | Animation |
|:---|:---|:---|
| Insert at Head | O(1) | Scale-grow keyframe with pointer update |
| Insert at Index | O(n) | Traversal highlight → shift → insert |
| Delete at Index | O(n) | Shrink/fade keyframe → shift left |
| Traversal | O(n) | Sequential node-by-node highlight |

### 🌳 Binary Tree & BST Visualizer
- **D3.js-powered SVG canvas** with dynamic tree layout rendering
- BST insertion with left/right comparison traversal
- **Node Search Visualizer** — Gold (search path) → Green (found) → Gray (pruned)
- Mouse panning & scroll wheel zooming on the tree canvas

### 📚 Stack Operations (LIFO)
| Operation | Complexity | Description |
|:---|:---|:---|
| Push | O(1) | Inserts element on top, checks overflow (max 8) |
| Pop | O(1) | Removes top element, checks underflow |
| Peek | O(1) | Returns current top element value |
| **Interactive Quiz** | — | Auto-triggers quiz modals after 3 operations |

### 🧩 Bonus: Sudoku Solver Visualizer
- Backtracking algorithm visualization on a 9×9 grid
- Generate random puzzles or input custom boards
- Watch the solver fill cells in real-time

### 🗺️ Pathfinding & Graph Algorithms
| Algorithm | Strategy | Visualization |
|:---|:---|:---|
| **Dijkstra's** | Shortest path (weighted) | Expanding wavefront → blue retrace path |
| **BFS** | Breadth-first exploration | Layer-by-layer grid flood |
| **DFS** | Depth-first exploration | Deep path probe with backtracking |
| **Maze Generation** | Recursive backtracker + random | Wall removal animation |

---

## 🏗️ Architecture

```
AlgoPulse (DSA-Visualizer-main/)
│
├── index.html                              # 🏠 Landing Page — Bento Grid Hub
├── css/modern_theme.css                    # 🎨 Global Design System (Dark Theme)
├── js/hero_canvas.js                       # ✨ Animated Background Canvas
│
├── Sorting-Visualizer-Project/             # 📊 MODULE 01: Sorting Suite
│   ├── sort.html                           #    Sorting workspace UI
│   ├── js/sort_script.js                   #    Bar-based: Bubble, Insertion, Heap, Merge, Quick
│   ├── js/sort_script2.js                  #    Box-based: Custom user array input
│   ├── js/renderSudoku.js                  #    Sudoku solver backtracking engine
│   └── css/sort_style.css                  #    Sorting page styles
│
├── Pathfinding-Visualiser-Project-master/  # 🗺️ MODULE 02: Binary Search & Pathfinding
│   ├── index.html                          #    Grid canvas & algorithm menu
│   ├── js/main.js                          #    Controller & grid setup
│   └── js/algoriithms/
│       ├── pathfinding algorithms/         #    Dijkstra, BFS, DFS
│       └── maze generation algorithm/      #    Recursive backtracker, Random maze
│
├── Linked-List-Visualization-master/       # 🔗 MODULE 03: Linked List
│   ├── index.html                          #    Linked list visualizer UI
│   └── js/
│       ├── LinkedList.js                   #    DOM node creation, pointers & animations
│       ├── main.js                         #    UI event listeners & form handlers
│       ├── settings.js                     #    Configuration controls
│       └── theme.js                        #    Theme toggle support
│
├── Binary-Tree-Visualization-master/       # 🌳 MODULE 04: Binary Tree & BST
│   ├── index.html                          #    Tree visualizer UI
│   ├── style.css                           #    SVG canvas & controls styling
│   └── js/
│       ├── binaryTree.js                   #    Tree data model & insertion logic
│       ├── draw.js                         #    D3.js rendering & layout generation
│       └── index.js                        #    User interaction, search & zoom
│
├── visualising-stack-implementation-master/ # 📚 MODULE 05: Stack
│   ├── index.html                          #    Stack visualizer UI + quiz modals
│   └── js/
│       ├── script.js                       #    Push/Pop/Peek logic & interactive quiz
│       └── jquery-3.5.1.min.js             #    DOM helper library
│
├── package.json                            # 📦 Dependencies (D3.js v7.8.5)
└── vercel.json                             # 🚀 Vercel deployment configuration
```

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|:---|:---|:---|
| **Structure** | HTML5 | Semantic page structure & Canvas elements |
| **Styling** | CSS3 | Glassmorphism dark theme, keyframe animations, bento grid |
| **Logic** | Vanilla JavaScript (ES6+) | Algorithm implementation, DOM manipulation, async animations |
| **Tree Rendering** | D3.js v7 | SVG hierarchical tree layout & dynamic node positioning |
| **DOM Utilities** | jQuery 3.5.1 | Stack module DOM helpers |
| **Deployment** | Vercel | Zero-config static site hosting |

### ⚙️ Core Animation Engine
The visualizer uses an `async/await` wrapper over `Promise` + `setTimeout` to create step-by-step delays without freezing the browser:

```javascript
function sleep(ms) {
    return new Promise((resolve) => setTimeout(resolve, ms));
}

// Inside sorting loops:
bars[j].style.backgroundColor = "red";      // Highlight comparison
await sleep(ms);                              // Yield control to browser for re-render
bars[j].style.backgroundColor = "green";     // Mark as sorted
```

---

## 📋 Progress Tracker

### ✅ Completed Features

| # | Task | Module | Status |
|:---:|:---|:---|:---:|
| 1 | Landing page with bento grid layout | Hub | ✅ Done |
| 2 | Global dark theme design system (`modern_theme.css`) | Hub | ✅ Done |
| 3 | Animated hero background canvas | Hub | ✅ Done |
| 4 | Floating navigation dock (all pages) | Hub | ✅ Done |
| 5 | Technical specifications matrix (tabbed view) | Hub | ✅ Done |
| 6 | Professional multi-column footer | Hub | ✅ Done |
| 7 | Bubble Sort visualization (bar-based) | Sorting | ✅ Done |
| 8 | Insertion Sort visualization (bar-based) | Sorting | ✅ Done |
| 9 | Heap Sort visualization (bar-based) | Sorting | ✅ Done |
| 10 | Merge Sort visualization (bar-based) | Sorting | ✅ Done |
| 11 | Quick Sort visualization (bar-based) | Sorting | ✅ Done |
| 12 | Box-based sorting with custom user input | Sorting | ✅ Done |
| 13 | Adjustable speed & array size controls | Sorting | ✅ Done |
| 14 | Sudoku solver backtracking visualizer | Sorting | ✅ Done |
| 15 | Binary Search step-by-step visualization | Binary Search | ✅ Done |
| 16 | Dijkstra's shortest path algorithm | Pathfinding | ✅ Done |
| 17 | BFS pathfinding visualization | Pathfinding | ✅ Done |
| 18 | DFS pathfinding visualization | Pathfinding | ✅ Done |
| 19 | Maze generation (recursive + random) | Pathfinding | ✅ Done |
| 20 | Drawable wall obstacles on grid | Pathfinding | ✅ Done |
| 21 | Linked List — Insert at head/index | Linked List | ✅ Done |
| 22 | Linked List — Delete at index | Linked List | ✅ Done |
| 23 | Linked List — Traversal animation | Linked List | ✅ Done |
| 24 | Linked List — Theme toggle | Linked List | ✅ Done |
| 25 | BST node insertion with comparison traversal | Binary Tree | ✅ Done |
| 26 | D3.js SVG tree rendering & layout | Binary Tree | ✅ Done |
| 27 | Node search visualizer (Gold/Green/Gray) | Binary Tree | ✅ Done |
| 28 | Mouse panning & scroll zoom on canvas | Binary Tree | ✅ Done |
| 29 | Stack Push operation with overflow check | Stack | ✅ Done |
| 30 | Stack Pop operation with underflow check | Stack | ✅ Done |
| 31 | Stack Peek operation | Stack | ✅ Done |
| 32 | Interactive quiz after stack operations | Stack | ✅ Done |
| 33 | Vercel deployment configuration | DevOps | ✅ Done |
| 34 | Responsive design (mobile/tablet/desktop) | All | ✅ Done |

### 🔲 Planned Enhancements (Future Scope)

| # | Task | Module | Status |
|:---:|:---|:---|:---:|
| 1 | Selection Sort algorithm visualization | Sorting | 🔲 Planned |
| 2 | Counting Sort / Radix Sort visualization | Sorting | 🔲 Planned |
| 3 | A* pathfinding algorithm | Pathfinding | 🔲 Planned |
| 4 | Greedy Best-First Search | Pathfinding | 🔲 Planned |
| 5 | Queue (FIFO) operations visualizer | New Module | 🔲 Planned |
| 6 | Doubly Linked List support | Linked List | 🔲 Planned |
| 7 | AVL Tree / Red-Black Tree balancing | Binary Tree | 🔲 Planned |
| 8 | Graph adjacency list visualizer | New Module | 🔲 Planned |
| 9 | Time complexity comparison charts | Hub | 🔲 Planned |
| 10 | Algorithm execution step counter | All | 🔲 Planned |

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- [Node.js](https://nodejs.org/) (optional, only for D3.js dependency management)

### Installation

```bash
# Clone the repository
git clone https://github.com/150202-Pratham/AlgoPulse-DSA_Visualizer.git

# Navigate to project directory
cd AlgoPulse-DSA_Visualizer

# Install dependencies (optional — for D3.js)
npm install

# Open in browser
# Simply open index.html in your browser, or use a live server:
npx serve .
```

### Quick Start
1. Open `index.html` — the **AlgoPulse Hub** landing page
2. Select any module card (Sorting, Binary Search, Linked List, Binary Tree, Stack)
3. Interact with the controls (adjust speed, input values, select algorithms)
4. Watch the algorithm execute step-by-step with color-coded animations

---

## 📸 Screenshots

| Landing Page Hub | Sorting Visualizer |
|:---:|:---:|
| *Bento grid layout with module cards* | *Bar-chart sorting with speed controls* |

| Binary Tree & BST | Stack Operations |
|:---:|:---:|
| *D3.js SVG tree with search visualization* | *LIFO push/pop with interactive quiz* |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](#).

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the **ISC License**. See `LICENSE` for more information.

---

## 👨‍💻 Author

**Pratham Garg**
- GitHub: [@150202-Pratham](https://github.com/150202-Pratham)
- Email: prathamgarg1502@gmail.com

---

<p align="center">
  <strong>⭐ If you found this project helpful, please give it a star! ⭐</strong>
</p>
