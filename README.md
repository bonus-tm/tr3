# Trivial Tree Traverse

A simple, single-file HTML application for visualizing directory tree structures from JSON files.

## Usage

1. Install `tree` command if necessary.
2. Create json file with it.
3. Open `tree-viewer.html` in any modern web browser, it will show you an example of the `tree` command.
4. Drag and drop resulting json file on the opened page.

### Input Format

The application expects a JSON file with a recursive directory structure:

```json
{
  "name": "root",
  "type": "directory",
  "contents": [
    { "name": "file.txt", "type": "file", "size": "10KB" },
    { "name": "folder", "type": "directory", "contents": [] }
  ]
}
```

