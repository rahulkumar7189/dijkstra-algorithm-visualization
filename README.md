# 🗺️ Dijkstra's Algorithm Visualization

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen.svg)](https://rahulkumar7189.github.io/dijkstra-algorithm-visualization/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

An interactive browser-based visualization tool that demonstrates how Dijkstra's shortest path algorithm works in real-time. This project provides an intuitive and engaging way to understand one of the most fundamental algorithms in computer science and graph theory.

![Dijkstra's Algorithm in Action](https://via.placeholder.com/800x400/4CAF50/FFFFFF?text=Dijkstra%27s+Algorithm+Visualization)

## 🎯 Overview

This project provides a complete browser-based implementation of Dijkstra's shortest path algorithm with animated visualizations. It allows users to:

- Create custom graphs by adding nodes and edges
- Set weights for edges to simulate different path costs
- Select start and end nodes
- Watch the algorithm execute step-by-step with smooth animations
- Understand the algorithm's decision-making process through visual feedback

Perfect for students, educators, and anyone interested in learning about pathfinding algorithms!

## ✨ Features

### Core Features
- **Interactive Graph Builder**: Create custom graphs with drag-and-drop functionality
- **Real-time Visualization**: Watch the algorithm explore paths with animated transitions
- **Step-by-Step Execution**: See each decision the algorithm makes
- **Weighted Edges**: Support for weighted graphs to demonstrate realistic pathfinding scenarios
- **Shortest Path Highlighting**: Final path is highlighted upon completion
- **Distance Display**: Real-time display of calculated distances to each node

### User Interface
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Intuitive Controls**: Easy-to-use interface for graph manipulation
- **Detailed Instructions**: Built-in guide explaining how to use the tool
- **Smooth Animations**: GSAP-powered animations for fluid visual transitions
- **Clean Aesthetics**: Modern, minimalist design focused on clarity

### Educational Benefits
- Understand algorithm complexity visually
- Observe priority queue operations
- See distance relaxation in action
- Compare different graph structures
- Learn through interactive experimentation

## 🎮 Demo

Visit the live demo: [Dijkstra's Algorithm Visualization](https://dijkstra-algorithm-visualization.vercel.app/)

### Quick Start Guide
1. Open the application in your browser
2. Click on the canvas to create nodes
3. Click and drag from one node to another to create edges
4. Enter edge weights when prompted
5. Select your start and destination nodes
6. Click "Run Algorithm" to watch the visualization
7. Observe the shortest path being calculated and highlighted

## 🚀 Installation

### Option 1: Clone the Repository

```bash
# Clone this repository
git clone https://github.com/rahulkumar7189/dijkstra-algorithm-visualization.git

# Navigate to the project directory
cd dijkstra-algorithm-visualization

# Open index.html in your browser
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

### Option 2: Direct Download

1. Download the ZIP file from the [repository](https://github.com/rahulkumar7189/dijkstra-algorithm-visualization)
2. Extract the contents
3. Open `index.html` in any modern web browser

### Option 3: GitHub Pages

Simply visit the hosted version at the link above - no installation required!

## 📖 Usage

### Basic Usage

1. **Creating Nodes**
   - Click anywhere on the canvas to place a node
   - Nodes are automatically labeled (A, B, C, etc.)

2. **Creating Edges**
   - Click on a node and drag to another node to create an edge
   - Enter the weight (distance/cost) when prompted
   - Edges are bidirectional by default

3. **Selecting Start and End Points**
   - Use the dropdown menus or click on nodes to set start/end points
   - Start node is typically highlighted in green
   - End node is typically highlighted in red

4. **Running the Algorithm**
   - Click the "Run" or "Start Algorithm" button
   - Watch as the algorithm explores different paths
   - Visited nodes change color to indicate exploration
   - The shortest path is highlighted at the end

5. **Resetting**
   - Use the "Reset" button to clear the current execution
   - Use "Clear All" to start with a blank canvas

### Advanced Features

- **Edit Mode**: Modify existing graphs by adding/removing nodes and edges
- **Weight Adjustment**: Update edge weights to see how paths change
- **Speed Control**: Adjust animation speed for faster or slower visualization
- **Instructions Page**: Access detailed help via `instructions.html`

## 📁 File Structure

```
dijkstra-algorithm-visualization/
│
├── index.html                    # Main application page
├── instructions.html             # User guide and help documentation
├── README.md                     # Project documentation (this file)
│
├── script.js                     # Core algorithm implementation and visualization logic
├── style.css                     # Styling and responsive design
├── gsap.js                       # GreenSock Animation Platform library
│
└── swastika-svgrepo-com.svg     # SVG icon/graphic asset
```

### File Descriptions

- **index.html**: The main HTML file containing the application structure, canvas element, and UI controls
- **instructions.html**: Comprehensive guide explaining how to use the visualization tool
- **script.js**: Contains the Dijkstra's algorithm implementation, graph data structure, event handlers, and visualization logic
- **style.css**: All styling including responsive design, animations, and theme customization
- **gsap.js**: GreenSock Animation Platform for smooth, performant animations
- **swastika-svgrepo-com.svg**: Vector graphic asset used in the UI

## 🧠 Algorithm Explanation

### What is Dijkstra's Algorithm?

Dijkstra's algorithm is a graph search algorithm that solves the single-source shortest path problem for a graph with non-negative edge weights. It was conceived by computer scientist Edsger W. Dijkstra in 1956.

### How It Works

1. **Initialization**
   - Set the distance to the start node as 0
   - Set all other distances to infinity
   - Mark all nodes as unvisited
   - Set start node as current

2. **Main Loop**
   - For the current node, examine all unvisited neighbors
   - Calculate tentative distances through the current node
   - If a calculated distance is less than the known distance, update it
   - Mark the current node as visited
   - Select the unvisited node with the smallest distance as the new current node

3. **Termination**
   - Algorithm terminates when the destination is reached
   - Or when all reachable nodes have been visited

4. **Path Reconstruction**
   - Backtrack from destination to source using recorded predecessors
   - This gives the shortest path

### Time Complexity

- **With Min-Priority Queue**: O((V + E) log V)
- **With Array**: O(V²)

Where V is the number of vertices and E is the number of edges.

### Space Complexity

- **O(V)**: For storing distances and visited nodes

### Visualization Benefits

This implementation visualizes:
- **Node exploration** (which nodes are being examined)
- **Distance updates** (when shorter paths are found)
- **Priority queue operations** (which node is selected next)
- **Path reconstruction** (final shortest path)

## 🛠️ Technologies Used

### Core Technologies
- **HTML5**: Semantic markup and Canvas API for rendering
- **CSS3**: Modern styling with Flexbox/Grid, animations, and transitions
- **JavaScript (ES6+)**: Algorithm implementation and DOM manipulation

### Libraries & Frameworks
- **[GSAP (GreenSock Animation Platform)](https://greensock.com/gsap/)**: Professional-grade animation library for smooth, performant transitions

### Development Tools
- **Git**: Version control
- **GitHub Pages**: Hosting and deployment

### Key JavaScript Features Used
- Classes and Object-Oriented Programming
- Array methods (map, filter, reduce)
- Event listeners and handlers
- Canvas API for graphics rendering
- Promise-based animations

## 🔧 How It Works

### Graph Representation

The graph is represented using an adjacency list:

```javascript
graph = {
  'A': [{'node': 'B', 'weight': 4}, {'node': 'C', 'weight': 2}],
  'B': [{'node': 'A', 'weight': 4}, {'node': 'D', 'weight': 5}],
  // ...
}
```

### Algorithm Implementation

The core algorithm uses:
1. **Priority Queue**: To efficiently select the node with minimum distance
2. **Distance Array**: Tracks shortest known distance to each node
3. **Predecessor Array**: Records path for reconstruction
4. **Visited Set**: Prevents re-processing of nodes

### Visualization Pipeline

1. **Event Detection**: User interactions trigger graph modifications
2. **State Update**: Graph data structure is updated
3. **Rendering**: Canvas is redrawn to reflect changes
4. **Animation**: GSAP animates transitions between states
5. **Algorithm Execution**: Step-by-step with visual feedback

## 🎨 Customization

### Modifying Colors

Edit `style.css` to change the color scheme:

```css
:root {
  --primary-color: #4CAF50;
  --secondary-color: #2196F3;
  --visited-color: #FFC107;
  --path-color: #F44336;
}
```

### Adjusting Animation Speed

In `script.js`, modify the animation duration:

```javascript
const ANIMATION_SPEED = 500; // milliseconds
```

### Changing Graph Styles

Customize node and edge appearance in `script.js`:

```javascript
const NODE_RADIUS = 20;
const EDGE_WIDTH = 2;
const NODE_COLOR = '#4CAF50';
```

## 🌐 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Opera 76+

**Note**: Requires a modern browser with ES6+ support and Canvas API.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Ideas for Contributions

- Add A* algorithm visualization
- Implement Bellman-Ford algorithm
- Add preset graph templates
- Improve mobile responsiveness
- Add dark mode toggle
- Create tutorial mode
- Add graph export/import functionality
- Implement undo/redo functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### MIT License Summary

You are free to:
- ✅ Use commercially
- ✅ Modify
- ✅ Distribute
- ✅ Private use

Under the condition that:
- ℹ️ License and copyright notice must be included

## 👏 Credits

### Algorithm
- **Edsger W. Dijkstra**: For inventing the algorithm in 1956

### Libraries
- **[GSAP](https://greensock.com/)**: GreenSock Animation Platform for smooth animations

### Resources
- Graph theory concepts and educational resources
- SVG icons from [SVG Repo](https://www.svgrepo.com/)

### Inspiration
- Various algorithm visualization tools and educational platforms
- Computer science education community

## 📧 Contact

**Rahul Kumar**

- GitHub: [@rahulkumar7189](https://github.com/rahulkumar7189)
- Project Link: [https://github.com/rahulkumar7189/dijkstra-algorithm-visualization](https://github.com/rahulkumar7189/dijkstra-algorithm-visualization)

## 🙏 Acknowledgments

- Thanks to all contributors who have helped improve this project
- Special thanks to the computer science education community
- Inspired by similar algorithm visualization projects

---

### 🌟 If you found this helpful, please consider giving it a star!

**Made with ❤️ for learning and education**
