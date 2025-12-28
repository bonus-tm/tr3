# Trivial Tree Traverse

A simple, single-file HTML application for visualizing directory tree structures from JSON files.

## Usage
1. Open `tree-viewer.html` in any modern web browser.
2. Drag and drop a JSON file containing the directory structure into the drop zone.

## Input Format
The application expects a JSON file with a recursive structure representing the file system.

Example structure:
```json
{
  "name": "root",
  "type": "directory",
  "contents": [
    {
      "name": "file.txt",
      "type": "file",
      "size": "10KB"
    },
    {
      "name": "folder",
      "type": "directory",
      "contents": []
    }
  ]
}
```

## Features
- **Drag & Drop Interface**: Easy file loading.
- **Interactive Tree**: Collapsible/expandable directory nodes.
- **Dark Mode Support**: Automatically adapts to system color scheme.
- **No Dependencies**: Pure HTML, CSS, and Vanilla JavaScript.

## Code Structure
- **Single File**: All logic (HTML, CSS, JS) is contained in `tree-viewer.html`.
- **CSS**: Uses CSS variables for theming and `prefers-color-scheme` for dark mode.
- **JavaScript**:
  - Handles file reading (FileReader API) and JSON parsing.
  - Generates DOM elements recursively to build the tree.
  - Manages UI state (loading spinner, error messages, toggling folders).

