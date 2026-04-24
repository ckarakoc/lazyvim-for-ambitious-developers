## Chapter 1. Introduction and Installation

Chapter 1 introduces LazyVim, Neovim, and Vim, explaining the benefits of modal editing and guiding through the installation process for various operating systems.

| Shortcut | Action |
|----------|--------|
| `Escape` followed by `:q!` then `Enter` | Exit Vim |
| `Escape` followed by `:Tutor` then `Enter` | Open interactive Neovim tutorial |
| `Space` | Enter Space mode |
| `l` (from dashboard or Space mode) | Open Lazy.nvim plugin manager |
| `Space-l` then `S` | Sync plugins (install, clean, update) |
| `q` | Quit Lazy.nvim plugin manager or dashboard |
| `G` (Shift+g) | Skip to end of plugin installation summary |

## Chapter 2. What is Modal Editing, Anyway?

Chapter 2 covers the core concept of modal editing in Vim, explaining Normal mode, Insert mode, Visual mode, and Command mode with their respective keybindings and use cases.

| Shortcut | Action |
|----------|--------|
| `Space` | Enter Space mode from Dashboard |
| `Escape` | Exit Space mode or Insert mode, return to Normal mode |
| `n` (from Dashboard) | Create a new empty buffer |
| `i` | Enter Insert mode before cursor |
| `a` | Enter Insert mode after cursor (Append) |
| `I` | Enter Insert mode at beginning of line |
| `A` | Enter Insert mode at end of line |
| `o` | Create new line below and enter Insert mode |
| `O` | Create new line above and enter Insert mode |
| `gi` | Go to last insertion point and enter Insert mode |
| `g` | Enter Go To mode (shows submenu) |
| `p` | Paste/put from clipboard |
| `Control-r` (in Insert mode) | Enter Registers mini-mode |
| `Control-r` (in Normal mode) | Redo (undo an undo) |
| `"` (Shift-apostrophe) (in Normal mode) | Enter Registers mode |
| `:` (Shift-semicolon) | Enter Command mode |
| `:q!` | Quit without saving |
| `:write` or `:w` | Write/save file |
| `:wq` or `:x` | Write and quit |
| `Tab` | Tab completion in Command mode |
| `Shift-Tab` | Cycle backward in Command mode menu |
| `Control-y` | Confirm selection and close Command menu |
| `Down` arrow | Move into selected directory (in Command mode completion) |
| `:help` | Open help documentation |

## Chapter 3. Getting Around

Chapter 3 covers efficient code navigation in LazyVim using Seek mode, scrolling commands, and various movement keybindings to navigate through files faster than traditional editors.

| Shortcut | Action |
|----------|--------|
| `s` | Enter Seek mode (seek text with labels) |
| `Control-d` | Scroll down by half screen |
| `Control-u` | Scroll up by half screen |
| `Control-f` | Scroll forward by full page |
| `Control-b` | Scroll backward by full page |
| `Control-y` | Scroll up by one line |
| `Control-e` | Scroll down by one line |
| `z` | Enter Z mode (cursor positioning and folding menu) |
| `zt` | Move current line to top of screen |
| `zb` | Move current line to bottom of screen |
| `zz` | Move current line to middle of screen |
| `0`, `zt0`, `zb0`, `zz0` | Move to start of line (with z commands) |
| `h`, `j`, `k`, `l` | Move left, down, up, right (replace arrow keys) |
| `[count]h/j/k/l` | Move cursor by count in respective directions |
| `f[char]` | Find character after cursor, jump to first match |
| `F[char]` | Find character before cursor (backward) |
| `[count]f/F[char]` | Find and jump to nth occurrence |
| `t[char]` | Find character before cursor position (To mode) |
| `T[char]` | Find character after cursor position (To mode backward) |
| `w` | Move to beginning of next word |
| `e` | Move to end of current/next word |
| `b` | Move to beginning of current/previous word |
| `ge` | Move to end of previous word |
| `W`, `E`, `B`, `gE` | Move by whitespace-delimited words (BIGGER words) |
| `^` | Move to first non-whitespace character of line |
| `$` | Move to end of line |
| `0` | Move to beginning of line (column 0) |
| `g_` | Move to last non-blank character of line |
| `[count]G` | Jump to specific line number |
| `gg` | Jump to beginning of file (line 1) |
| `G` (without count) | Jump to end of file |
| `Control-o` | Jump to previous location (jump history backward) |
| `Control-i` | Jump to next location (jump history forward) |

## Chapter 4. Opening Files

Chapter 4 introduces three different file management systems in LazyVim: the Snacks picker for fuzzy file search, the Snacks explorer for tree-view navigation, and mini.files for columnar file management with Vim-native keybindings.

| Shortcut | Action |
|----------|--------|
| `Space Space` or `Space ff` | Open Files In Current Project (Root Dir) |
| `Space fF` | Find Files (cwd) |
| `Alt-s` (in picker) | Show seek labels in picker |
| `Tab` (in picker) | Select file for multiple selection |
| `Enter` (in picker) | Open selected file(s) |
| `Control-d`, `Control-u` (in picker) | Scroll results window down/up |
| `Control-f`, `Control-b` (in picker) | Scroll preview window forward/backward |
| `Escape` twice (in picker) | Exit picker |
| `:cd path/to/directory` | Change directory |
| `:pwd` | Print working directory |
| `:lcd` | Local change directory (for current window only) |
| `Space e` | Explore Snacks (root directory) |
| `Space E` | Explore Snacks (cwd) |
| `q` or `Escape` (in explorer) | Hide explorer |
| `j`, `k` (in explorer) | Move up and down |
| `Enter` (in explorer) | Open file or expand folder |
| `Tab` (in explorer) | Select multiple files |
| `i` (in explorer) | Enter Insert mode to search |
| `Alt-s` (in explorer) | Seek to any line |
| `Backspace` (in explorer) | Navigate up the tree |
| `d` (in explorer) | Delete file |
| `a` (in explorer) | Add file or folder (trailing `/` for folder) |
| `r` (in explorer) | Rename file or folder |
| `y` (in explorer) | Yank (copy) file |
| `p` (in explorer) | Put (paste) file |
| `m` (in explorer) | Move file |
| `H` (in explorer) | Show/hide dotfiles |
| `I` (in explorer) | Show/hide gitignored files |
| `?` (in explorer) | Show help |
| `:LazyExtras` | Open LazyExtras menu |
| `x` (in LazyExtras) | Install/toggle extra |
| `Space fm` | Open mini.files (Directory of Current File) |
| `Space fM` | Open mini.files (cwd) |
| `j`, `k` (in mini.files) | Move up and down |
| `l` (in mini.files) | Move into folder or open file |
| `h` (in mini.files) | Move out of folder |
| `q` (in mini.files) | Close mini.files |
| `o` (in mini.files) | Create new file or folder |
| `dd` (in mini.files) | Delete file or folder |
| `yy` (in mini.files) | Yank (copy) file or folder |
| `p` (in mini.files) | Put (paste) file or folder |
| `=` (in mini.files) | Save filesystem changes |
