# Deck Editor

A lightweight, browser-based code editor designed for working with structured code blocks inside files. It combines a familiar editing experience with a focused layer of block awareness, making it easier to navigate, inspect, and manipulate logically grouped sections of code.

---

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Block Syntax](#block-syntax)
* [Usage](#usage)
* [Keyboard Shortcuts](#keyboard-shortcuts)
* [Browser Support](#browser-support)
* [Design Philosophy](#design-philosophy)
* [Prompting AI for Best Results](#prompting-ai-for-best-results)
* [Limitations](#limitations)
* [Contributing](#contributing)
* [License](#license)

---

## Project Structure

```id="u2p0w3"
.
├── deck-editor.html   # Main application (editor, UI, logic)
└── README.md          # Project documentation
```

The project is intentionally minimal. All functionality lives in a single file, making it easy to inspect, modify, and extend without setup overhead.

---

## Overview

Deck Editor is built for scenarios where code is not just written linearly, but organized into meaningful sections. By recognizing specially formatted block markers, it introduces structure without requiring a custom syntax or tooling.

It remains a plain-text editor at its core, with an additional layer that helps you reason about grouped code.

---

## Features

* Block-aware editing with automatic detection
* Hierarchical block tree with nesting support
* Visual highlighting of selected blocks
* Multi-tab file editing
* Local file system integration (where supported)
* Zero dependencies, no build process
* Keyboard-driven workflow

---

## Block Syntax

Blocks are defined using comment-based markers compatible with common languages.

### JavaScript / Generic

```js id="4kg6vd"
// [[ Block Name ]]
...code...
// [[/ Block Name ]]
```

### HTML

```html id="9mzzxq"
<!-- [[ Block Name ]] -->
...code...
<!-- [[/ Block Name ]] -->
```

### CSS

```css id="0z22dz"
/* [[ Block Name ]] */
...code...
/* [[/ Block Name ]] */
```

Blocks can be nested, and the editor reflects this hierarchy in the side panel.

---

## Usage

1. Open `deck-editor.html` in a modern browser
2. Load a folder or individual files
3. Edit code normally
4. Use the block panel to navigate sections
5. Save changes back to disk or download files

---

## Keyboard Shortcuts

* `Ctrl + S` — Save current file
* `Ctrl + O` — Open files
* `Ctrl + W` — Close active tab
* `Ctrl + Tab` — Switch tabs
* `Ctrl + Shift + E` — Toggle file explorer

---

## Browser Support

Direct file system access depends on the File System Access API.

* Supported: Chrome, Edge (Chromium-based)
* Fallback: File upload/download in other browsers

---

## Design Philosophy

This project prioritizes clarity and directness over abstraction.

* No frameworks
* No build tools
* No hidden layers

Everything is contained in a single, readable file. The goal is to keep the mental model simple while still providing meaningful structure through block awareness.

---

## Prompting AI for Best Results

When using AI to extend or modify this project, clarity in prompting makes a significant difference.

### Principles

* Be specific about what should change
* Provide constraints (e.g., no frameworks, single-file architecture)
* Focus on one problem at a time
* Ask for minimal, targeted output

### Example Prompt

```id="2b0t7p"
You are working on a single-file browser-based code editor.

Constraints:
- No external libraries
- Keep code readable and minimal
- Preserve existing behavior

Task:
Improve the block parsing logic to handle edge cases like unmatched or nested blocks without breaking current functionality.

Output:
- Updated function only
- Short explanation of changes
```

Well-scoped prompts tend to produce more usable results than broad or ambiguous requests.

---

## Limitations

* Not a full IDE (no language server or deep syntax parsing)
* Requires manual block annotations
* File system features depend on browser support

---

## Contributing

Contributions should align with the core direction of the project:

* Maintain simplicity
* Avoid unnecessary dependencies
* Keep code readable and direct

If a change increases complexity, it should clearly justify its value.
