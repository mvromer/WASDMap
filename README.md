# WASDMap
Keymap extension for keyboard navigation, selection, and window splitting and navigation based on WASD.

## Requirements
This requires at least version 1.25 of Visual Studio Code to fully work.

## Features
This adds a number of keyboard shortcuts for performing the following tasks without having to really move your hands from home row:

* Moving the cursor in the active editor
* Making selections within the active editor
* Splitting the current editor group in arbitrary directions
* Moving and cloning documents from one editor group to another
* Changing the active editor group

This also adds one custom command that acts sort of like the `kill-line` command in Emacs.

Keyboard shortcuts are based around WASD, a key layout common to many modern PC games. All keyboard shortcuts were selected to minimize conflicts with the default Visual Studio Code shortcuts as well as shortcuts provided by a number of popular extensions (e.g., GitLens, various language extensions).

## Keyboard Shortcuts
### Cursor Navigation
The following shortcuts are for moving the cursor throughout the current active editor.

| Shortcut | Action |
|----------|--------|
| `Alt+W`  | Move cursor up |
| `Alt+A`  | Move cursor left |
| `Alt+S`  | Move cursor right |
| `Alt+D`  | Move cursor down |
| `Alt+F`  | Move cursor forward one word |
| `Alt+B`  | Move cursor backward one word |
| `Alt+N`  | Move cursor down one page |
| `Alt+P`  | Move cursor up one page |
| `Alt+J`  | Move cursor to start of current line |
| `Alt+K`  | Move cursor to end of current line|

### Selection
The following shortcuts are for making selections within the current active editor.

| Shortcut       | Action |
|----------------|--------|
| `Shift+Alt+W`  | Move selection cursor up |
| `Shift+Alt+A`  | Move selection cursor left |
| `Shift+Alt+S`  | Move selection cursor right |
| `Shift+Alt+D`  | Move selection cursor down |
| `Shift+Alt+F`  | Move selection cursor forward one word |
| `Shift+Alt+B`  | Move selection cursor backward one word |
| `Shift+Alt+N`  | Move selection cursor down one page |
| `Shift+Alt+P`  | Move selection cursor up one page |

### Line Killing
The following shortcut runs a custom command that partially mimics the `kill-line` command from Emacs.

With no selection active, this custom command will effectively cut the contents of the current line starting from the cursor's position to the end of the line. The removed contents are placed on the clipboard, making them available via a paste operation.

With an active selection, this command will cut the current selection, adding its contents to the clipboard.

| Shortcut      | Action |
|---------------|--------|
| `Shift+Alt+K` | Kill line |

### Editor Group Navigation
The following shortcuts are for navigating between different editor groups that may be present in the editor.

| Shortcut | Action |
|-----------|--------|
| `Ctrl+Alt+W` | Focus on editor group above the active group |
| `Ctrl+Alt+A` | Focus on editor group to the left of the active group |
| `Ctrl+Alt+S` | Focus on editor group to the right of the active group |
| `Ctrl+Alt+D` | Focus on editor group below the active group |

### New Editor Group Creation
The following shortcuts are for creating new editor groups within the editor.

| Shortcut | Action |
|-----------|--------|
| `Ctrl+K Ctrl+Alt+W` | Create new editor group above the active group |
| `Ctrl+K Ctrl+Alt+A` | Create new editor group to the left of the active group |
| `Ctrl+K Ctrl+Alt+S` | Create new editor group to the right of the active group |
| `Ctrl+K Ctrl+Alt+D` | Create new editor group below the active group |

### Splitting Editor Groups
The following shortcuts are for splitting existing editor groups. When an editor group is split, a new editor group is formed, and the current document in the editor group that was split is duplicated in the new editor group. These are useful for opening up additional views to the same file.

| Shortcut | Action |
|-----------|--------|
| `Ctrl+K Alt+W` | Split the active editor group and place the new group above |
| `Ctrl+K Alt+A` | Split the active editor group and place the new group to the left |
| `Ctrl+K Alt+S` | Split the active editor group and place the new group to the right |
| `Ctrl+K Alt+D` | Split the active editor group and place the new group below |

### Moving Documents between Editor Groups
The following shortcuts are for moving a document from one editor group to another editor group.

| Shortcut | Action |
|-----------|--------|
| `Ctrl+K Shift+Alt+W` | Move current document in active editor group to the group above |
| `Ctrl+K Shift+Alt+A` | Move current document in active editor group to the group to the left |
| `Ctrl+K Shift+Alt+S` | Move current document in active editor group to the group to the right |
| `Ctrl+K Shift+Alt+D` | Move current document in active editor group to the group below |

## Background
In a prior life, I was an Emacs junkie. With every year I sunk into using that editor, the faster my fingers flew across the keyboard pounding out crazy key chords for all manners of tasks.

Then one day I stopped being a Linux developer and took a job working 100% on a Microsoft stack. I tried emacs for Windows, but the impedance mismatch was too great, and plus, there were too many productivity gains I'd be leaving on the table by not embracing Visual Studio.

Despite growing accustomed to my new development digs, I ended up missing two main features from my Emacs days:

1. Slick navigation throughout the editor using key combinations that didn't force me to move away from home row.
2. Arbitrarily splitting my editor into any arrangement of vertical and horizontal panes, again all from home row.

I eventually moved to Sublime for anything that wasn't heavily C++ or C# based, and I thought I had found the holy grail there. With some custom extensions and additional hacking, I was able to recreate many of the navigation and window splitting features I missed from Emacs.

Fast forward to July 2018, and Visual Studio Code comes out with features in the box for performing the exact same set of window splitting tasks as I had grown to love in both Emacs and Sublime. This was the missing piece that had otherwise prevented me from switching from Sublime to VS Code. This immediately led to the creation of a keymap that made it efficient for me to access these window splitting and editor navigation commands.

In creating this keymap, I wanted to fulfill two goals:

1. Not force myself off home row in order to access these commands (e.g., don't be forced to use the arrow keys).
2. Avoid conflicts as much as possible with default shortcuts for commands provided by Visual Studio Code.

The end result of that effort is this keymap extension.

## License
[MIT](https://github.com/mvromer/WASDMap/blob/master/LICENSE) © Michael Romer
