# DSA Master Visualizer - React

[![Live Demo](https://img.shields.io/badge/Live-Demo-blue)](https://eng-neelpatel.github.io/dsa-visualizer-react/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-18.x-blue?logo=react)](https://react.dev/)

An interactive, full-featured DSA (Data Structure & Algorithm) visualizer built with React. Create, visualize, and animate algorithm steps with complete CRUD operations. Perfect for learning, teaching, and interviewing!

## Features

### Core Functionality
- **Interactive CRUD Operations**: Create, Read, Update, and Delete DSA topics
- **Step-by-Step Execution**: Animate algorithm progression with detailed explanations
- **Multiple Visualizations**: Support for arrays, linked lists, trees, graphs, and more
- **Real-time Updates**: Watch data structures transform as algorithms execute
- **Progress Tracking**: Visual progress bar showing algorithm completion
- **Playback Controls**: Play, pause, forward, backward navigation

### Pre-built Algorithm Templates
- Bubble Sort
- Binary Search
- Linked List Traversal
- Quick Sort (coming soon)
- Merge Sort (coming soon)
- BST Operations (coming soon)
- Heap Operations (coming soon)

### User Experience
- **Modal-based Editor**: Intuitive topic and step configuration
- **Responsive Design**: Works seamlessly on desktop and mobile
- **Professional UI**: Built with Tailwind CSS for modern aesthetics
- **Keyboard Shortcuts**: Fast navigation through visualizations
- **Auto-play**: Automatic step progression with adjustable timing

## Tech Stack

- **Frontend**: React 18+
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **State Management**: React Hooks
- **Build Tool**: Vite / Create React App
- **Deployment**: GitHub Pages

## Quick Start

### Local Development

```bash
# Clone the repository
git clone https://github.com/eng-neelpatel/dsa-visualizer-react.git
cd dsa-visualizer-react

# Install dependencies
npm install

# Start development server
npm start

# Open browser to http://localhost:3000
```

### Build for Production

```bash
npm run build
```

## Usage

### Creating a New Visualization

1. Click the '+' button in the DSA Topics sidebar
2. Enter topic title and description
3. Add visualization steps:
   - **Action**: Brief description of what happens
   - **Explanation**: Detailed explanation of the step
   - **Data State**: Current state of the data structure (array or linked list format)
4. Save the topic

### Running a Visualization

1. Select a topic from the sidebar
2. Use playback controls:
   - **Play/Pause**: Auto-play through steps
   - **Next/Previous**: Manual step navigation
   - **Progress Bar**: Jump to any step
3. Read explanations in the step details panel

### Data Format Examples

**Arrays/Sorting:**
```
5,1,4,2,8
1,2,4,5,8 (sorted)
```

**Linked Lists:**
```
A -> B -> C -> D
A -> [B] -> C -> D (B is current)
```

## Project Structure

```
src/
├── App.jsx                 # Main application component
├── components/
│   ├── DataVisualization.jsx
│   ├── Modal.jsx
│   └── Controls.jsx
├── styles/
│   └── index.css          # Tailwind CSS imports
└── index.js               # React DOM render
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Roadmap

- [ ] Add more pre-built algorithm templates
- [ ] Animation speed control
- [ ] Tree and Graph visualizations
- [ ] Export/Import visualization data
- [ ] Code generation from visualizations
- [ ] Multi-language support
- [ ] Dark mode toggle

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Neel Patel ([@eng-neelpatel](https://github.com/eng-neelpatel))

## Support

If you found this project helpful, please consider:
- Starring the repository ⭐
- Sharing it with others 🚀
- Contributing improvements 🤝

---

**Made with ❤️ for the developer community**
