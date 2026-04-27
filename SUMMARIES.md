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

## Chapter 5. Configuration and Plugin Basics

Chapter 5 explains LazyVim's multi-layered plugin management system, covering three categories of plugins (built-in, Lazy Extras, and third-party), and demonstrates how to install, disable, customize plugins, modify keybindings, and configure options through Lua files.

| Shortcut | Action |
|----------|--------|
| `x` (from dashboard) | Access Lazy Extras mode |
| `:LazyExtras` | Open Lazy Extras from Command mode |
| `:lua Snacks.dashboard()` | Show the dashboard |
| `c` (from dashboard) | Open config directory |
| `Space fc` | Find Config File |
| `x` (in LazyExtras) | Install/disable extra plugin |
| `:help lua` | Open Lua help documentation |
| `:help lua-guide-api` | Learn about Vim-specific Lua APIs |
| `:help plugin-name` | Get help for specific plugin |
| `Space qs` | Select from list of recent sessions |

## Chapter 6. Basic Editing

Chapter 6 covers the fundamental editing verbs in Vim (delete, change, repeat), character-level modifications, case manipulation, command recording and playback, and undo/redo functionality.

| Shortcut | Action |
|----------|--------|
| `d<motion>` | Delete text from cursor to motion destination |
| `dh` | Delete character to the left of cursor |
| `d3w` | Delete three words |
| `3dw` | Delete one word, three separate times |
| `d^` | Delete from cursor to beginning of line |
| `d$` | Delete from cursor to end of line |
| `d0` | Delete from cursor to first column of line |
| `dw` | Delete word |
| `db` | Delete word backward |
| `dj` | Delete down one line |
| `dk` | Delete up one line |
| `dd` | Delete entire line |
| `d3d` or `3dd` | Delete three lines |
| `D` | Delete from cursor to end of line (shortcut for `d$`) |
| `c<motion>` | Change text from cursor to motion destination (delete and enter Insert mode) |
| `cw` | Change word |
| `cc` | Change entire line |
| `c3c` or `3cc` | Change three lines |
| `C` | Change from cursor to end of line (shortcut for `c$`) |
| `x` | Delete character under cursor |
| `[count]x` | Delete multiple characters starting from cursor |
| `X` | Delete character before cursor |
| `[count]X` | Delete multiple characters to the left |
| `r<char>` | Replace character under cursor with `<char>` |
| `[count]r<char>` | Replace multiple characters with same character |
| `J` | Join current line with next line |
| `[count]J` | Join multiple lines |
| `gJ` | Join lines without modifying whitespace |
| `gU<motion>` | Convert text to UPPERCASE |
| `gUU` | Convert entire line to UPPERCASE |
| `gu<motion>` | Convert text to lowercase |
| `guu` | Convert entire line to lowercase |
| `~` | Toggle case of character under cursor |
| `[count]~` | Toggle case of multiple characters |
| `.` | Repeat last command (dot repeat) |
| `[count].` | Repeat last command with new count |
| `qq` | Start recording macro |
| `q` | Stop recording macro |
| `qQ` | Append to recording in append mode |
| `Q` | Play back most recent recording |
| `u` | Undo last change |
| `Control-r` | Redo (undo an undo) |

## Chapter 7. Objects and Operator-Pending Mode

Chapter 7 covers advanced text objects and operator-pending mode, including Unimpaired mode navigation (sentences, paragraphs, references, diagnostics, git hunks), text objects for words/brackets/language features, Seek surrounding objects, and the mini.surround plugin for manipulating surrounding pairs.

| Shortcut | Action |
|----------|--------|
| `(` / `)` | Jump to previous/next sentence |
| `{` / `}` | Jump to previous/next paragraph |
| `[count](` etc. | Use count to jump multiple sentences/paragraphs |
| `[(` / `](` / `[{` / `]}` / `[<` / `]>` | Jump to unmatched parenthesis/bracket/angle bracket (jump out) |
| `[%` / `]%` | Jump to beginning/end of current bracket pair |
| `[[` / `]]` | Jump to previous/next variable reference |
| `[c`/`]c`, `[f`/`]f`, `[m`/`]m` | Jump to previous/next class/function/method definition |
| `[C`/`]C`, `[F`/`]F`, `[M`/`]M` | Jump to end of previous/next class/function/method |
| `[i` / `]i` | Jump to top/bottom of current indentation level |
| `[d`/`]d`, `[e`/`]e`, `[w`/`]w` | Jump to previous/next diagnostic/error/warning |
| `[s` / `]s` | Jump to previous/next spelling error |
| `[t` / `]t` | Jump to previous/next TODO/FIXME comment |
| `[h` / `]h` | Jump to previous/next git hunk |
| `di`/`da` + `w`/`W`/`s`/`p` | Delete inside/around word/big-word/sentence/paragraph |
| `di`/`da` + `"`/`'`/`` ` `` / `q` | Delete inside/around quotes (specific or auto-detect) |
| `di`/`da` + `(`/`[`/`{`/`<`/`b` | Delete inside/around brackets (specific or nearest) |
| `di`/`da` + `*`/`_` | Delete inside/around markup (bold/italic) |
| `di`/`da` + `c`/`f`/`o`/`t`/`i` | Delete inside/around class/function/object/tag/indentation |
| `di`/`da` + `h` | Delete inside/around git hunk |
| `di`/`da` + `n`/`l` + object | Delete inside/around next/last text object |
| `dig` / `dag` | Delete inside/around entire buffer |
| `dS` / `cS` / `yS` | Act on surrounding object via Seek labels |
| `dR` / `cr` / `yr` | Act on object found via remote Seek |
| `%` | Jump between matching bracket pair |
| `g[(`/`g])`/`g[[`/`g]]` | Jump to nearest opening/closing bracket |
| `gsai(` / `gsai)` | Add surrounding parentheses around motion |
| `gsa` + motion + bracket/quote | Add surrounding pair around motion |
| `gsd` + bracket/quote | Delete surrounding pair |
| `2gsd` + bracket | Delete nth surrounding pair (with count) |
| `gsr` + old + new | Replace surrounding pair with new character |
| `gsf`/`gsF` + bracket | Navigate to opening/closing bracket |
| `gsh` + bracket | Highlight surrounding brackets |
| `gsaa` + object + `t` | Add surrounding HTML/XML tag around object |
| `c`/`y`/`d` + text object | Common verbs with text objects (change/yank/delete) |
