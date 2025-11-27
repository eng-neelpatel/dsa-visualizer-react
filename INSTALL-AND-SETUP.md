# Complete Setup Guide: DSA Visualizer React

## Quick Start (3 Steps)

### Step 1: Create React App
```bash
npx create-react-app dsa-visualizer-react
cd dsa-visualizer-react
```

### Step 2: Install Dependencies
```bash
npm install lucide-react
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Step 3: Copy Files Below and Deploy

Folders needed:
```
src/
├── App.jsx
├── index.css
├── index.js
public/
├── index.html
```

## File Contents

### 1. src/tailwind.config.js
```javascript
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 2. src/index.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 3. src/App.jsx - MAIN APPLICATION (See React component from earlier)

Copy the complete React component code from the previous message into `src/App.jsx`

### 4. package.json modifications

Update your package.json:
```json
{
  "name": "dsa-visualizer-react",
  "version": "1.0.0",
  "homepage": "https://eng-neelpatel.github.io/dsa-visualizer-react",
  "private": true,
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "lucide-react": "^latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  },
  "devDependencies": {
    "react-scripts": "5.0.1",
    "tailwindcss": "^latest",
    "postcss": "^latest",
    "autoprefixer": "^latest",
    "gh-pages": "^latest"
  }
}
```

## Deploy to GitHub Pages

### Step 1: Install gh-pages
```bash
npm install --save-dev gh-pages
```

### Step 2: Update package.json
Add these to package.json scripts section:
```json
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
```

### Step 3: Deploy
```bash
npm run deploy
```

### Step 4: Enable GitHub Pages
1. Go to Settings tab on your GitHub repository
2. Scroll to "GitHub Pages"
3. Select "Deploy from a branch"
4. Select "gh-pages" branch and "/root" folder
5. Save

Your app will be live at: `https://eng-neelpatel.github.io/dsa-visualizer-react/`

## Local Development

```bash
npm start
```

App opens at http://localhost:3000

## Features Already Included

✅ 2 Pre-built Visualizations:
- Bubble Sort (Array: [5, 1, 4, 2, 8])
- Linked List Traversal

✅ Full CRUD Operations:
- Create new topics
- Edit existing topics
- Delete topics
- Add/remove visualization steps

✅ Interactive Controls:
- Play/Pause auto-play
- Next/Previous step navigation
- Progress bar scrubbing
- Step details and explanations

✅ Data Visualizations:
- Array visualization (bar chart style)
- Linked list visualization (node-based)

## Customization

### Add More Pre-built Algorithms

Edit the `initialTopics` array in App.jsx:

```javascript
const initialTopics = [
  {
    id: 1,
    title: 'Your Algorithm Name',
    description: 'Description here',
    steps: [
      { 
        id: 1, 
        action: 'Initial State', 
        explanation: 'Starting...', 
        dataState: [5, 3, 1] 
      },
      { 
        id: 2, 
        action: 'Compare 5 and 3, Swap', 
        explanation: 'Since 5 > 3, swap...', 
        dataState: [3, 5, 1] 
      },
      // Add more steps...
    ],
  },
]
```

### Add LocalStorage Persistence

Add this to App.jsx after state declarations:

```javascript
// Load from localStorage
useEffect(() => {
  const saved = localStorage.getItem('dsaTopics');
  if (saved) setTopics(JSON.parse(saved));
}, []);

// Save to localStorage when topics change
useEffect(() => {
  localStorage.setItem('dsaTopics', JSON.stringify(topics));
}, [topics]);
```

## Troubleshooting

### Port 3000 already in use
```bash
# Use a different port
PORT=3001 npm start
```

### Build size too large
```bash
# Check what's in build
cd build
duplicate-package-checker ../package.json
```

### GitHub Pages not updating
```bash
# Force clean deploy
rm -rf node_modules/.cache
npm run deploy
```

## Next Steps

1. Add more algorithm templates
2. Add animation speed control
3. Implement tree/graph visualizations  
4. Add dark mode
5. Export/import visualization data

## Support

For issues, check:
- README.md in the repo
- GitHub Issues section
- React documentation: https://react.dev/
- Tailwind documentation: https://tailwindcss.com/

**Your React DSA Visualizer is ready to code! 🚀**
