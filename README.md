// src/App.js
import React, { useState } from 'react';
import { marked } from 'marked';
import './App.css';

function App() {
  // State to hold the markdown input
  const [markdown, setMarkdown] = useState(defaultMarkdown);

  // Handler for textarea changes
  const handleChange = (e) => {
    setMarkdown(e.target.value);
  };

  // Convert markdown to HTML using Marked
  const getMarkdownText = () => {
    const rawMarkup = marked(markdown, { breaks: true, gfm: true });
    return { __html: rawMarkup };
  };

  return (
    <div className="App">
      <h1>📄 Markdown Previewer</h1>
      <div className="container">
        <textarea
          id="editor"
          value={markdown}
          onChange={handleChange}
          placeholder="Enter your markdown here..."
          aria-label="Markdown Editor"
        />
        <div
          id="preview"
          dangerouslySetInnerHTML={getMarkdownText()}
          aria-label="Markdown Preview"
        ></div>
      </div>
    </div>
  );
}

// Default markdown to fulfill User Story #5 and #6
const defaultMarkdown = `# Welcome to the Markdown Previewer!

## This is a sub-heading

### And here's some other cool stuff:

Here's some inline code: \`<div></div>\`

\`\`\`javascript
// This is a multi-line code block:
function greet(name) {
  return \`Hello, \${name}!\`;
}
\`\`\`

- And of course, there are lists.
  - Some are bulleted.
     - With different indentation levels.

> Block Quotes are awesome!

You can also add images:

![React Logo](https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg)

**Bolded text** is also supported!
`;

export default App;
/* src/App.css */

.App {
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f0f0f0;
  min-height: 100vh;
  padding: 2rem;
}

h1 {
  margin-bottom: 2rem;
  color: #333;
}

.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

textarea#editor {
  width: 45%;
  height: 70vh;
  padding: 1rem;
  border: 2px solid #ccc;
  border-radius: 5px;
  resize: none;
  font-size: 1rem;
  font-family: 'Courier New', Courier, monospace;
}

#preview {
  width: 45%;
  height: 70vh;
  padding: 1rem;
  border: 2px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
  overflow-y: auto;
  text-align: left;
}

#preview img {
  max-width: 100%;
  height: auto;
}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  textarea#editor,
  #preview {
    width: 90%;
    height: 50vh;
  }
}
// src/index.js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

// Render the App component into the root div
ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
/* src/index.css */

body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
{
  "name": "markdown-previewer",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "marked": "^4.3.0",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "5.0.1"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  }
}
{
  "name": "markdown-previewer",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://<your-username>.github.io/markdown-previewer",
  "dependencies": {
    "marked": "^4.3.0",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "5.0.1"
  },
  "devDependencies": {
    "gh-pages": "^4.0.0"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  }
}
{
  "name": "markdown-previewer",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://<your-username>.github.io/markdown-previewer",
  "dependencies": {
    "marked": "^4.3.0",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "5.0.1"
  },
  "devDependencies": {
    "gh-pages": "^4.0.0"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  }
}
