# AlgoPulse — DSA Visualizer

A lightweight web-based DSA visualization project focused on making sorting algorithms easier to understand through live animations and interactive controls.

## Project Status

This repository currently contains the implemented landing page and the sorting visualizer workspace. The project is actively built around the sorting module, and the remaining DSA visualizer modules mentioned in older docs are planned for future work.

## Implemented So Far

### 1. Modern landing hub
- Dark-themed responsive landing page
- Floating navigation dock
- Bento-grid module cards
- Hero section and design system styling
- Links to the sorting workspace

### 2. Sorting visualizer workspace
- Bar-based sorting visualization
- Custom array input via number boxes
- Randomize and reset controls
- Adjustable array size and animation speed
- Real-time status log

### 3. Sorting algorithms included
- Bubble Sort
- Insertion Sort
- Heap Sort
- Merge Sort
- Quick Sort

### 4. User interaction features
- Custom numerical array creation
- Speed control for animation timing
- Visual comparison and swap highlighting
- Color-coded sorted states

## Current Project Structure

```text
AlgoPulse-DSA_Visualizer/
├── index.html
├── README.md
├── package.json
├── package-lock.json
├── css/
│   └── modern_theme.css
├── js/
│   └── hero_canvas.js
├── Sorting-Visualizer-Project/
│   ├── sort.html
│   ├── css/
│   │   └── sort_style.css
│   └── js/
│       ├── sort_script.js
│       └── sort_script2.js
└── .git/
```

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- D3.js (installed in package.json, currently not the main active visualizer dependency for the implemented features)

## How to Run

### Option 1: Open directly
Open `index.html` in a browser.

### Option 2: Use a local server
```bash
npm install
npx serve .
```
Then open the local server URL in the browser.

## Planned Additions

The following modules are planned for future implementation:
- Binary Search visualizer
- Linked List visualizer
- Binary Tree / BST visualizer
- Stack visualizer
- Pathfinding / graph visualizers

## Notes

The earlier README content referenced additional visualizer modules that are not currently present in this repository. This README reflects the actual implemented state of the project as it exists today.

## Future Scope

The project is designed to grow into a larger DSA learning platform, with additional modules planned in the roadmap.

