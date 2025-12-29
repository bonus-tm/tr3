# Trivial Tree Traverse

A simple, single-file HTML application for visualizing directory tree structures from JSON files.

## Usage
1. Open `tree-viewer.html` in any modern web browser.
2. Drag and drop a JSON file containing the directory structure into the drop zone.

## Input Format
The application expects a JSON file with a recursive structure representing the file system. It handles standard directory structures and error states.

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
    },
    {
      "name": "restricted_folder",
      "type": "directory",
      "contents": [
        { "error": "error opening dir" }
      ]
    }
  ]
}
```

## Features
- **Drag & Drop Interface**: Global drop zone with visual feedback.
- **Two-State Interface**: Welcome screen with instructions vs. Tree visualization.
- **Interactive Tree**: Collapsible/expandable directory nodes.
- **File Metadata**: Displays dropped file name and formatted total size.
- **Dot Files Filtering**: Toggle visibility of hidden files (starting with dot).
- **Error Visualization**: Distinct styling for directories with access errors.
- **Dark Mode Support**: Automatically adapts to system color scheme.
- **No Dependencies**: Pure HTML, CSS, and Vanilla JavaScript.

## Code Structure
- **Single File**: All logic (HTML, CSS, JS) is contained in `tree-viewer.html`.
- **CSS**: 
  - Uses CSS variables for theming and `prefers-color-scheme` for dark mode.
  - **CSS Nesting**: Always use CSS nesting syntax for cleaner stylesheets.
- **JavaScript**:
  - Handles file reading (FileReader API) and JSON parsing.
  - Generates DOM elements recursively to build the tree.
  - Manages UI state (Welcome/Tree screens, loading spinner, error messages).
