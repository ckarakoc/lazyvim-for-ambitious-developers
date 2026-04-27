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

## Chapter 8. Clipboard, Registers, and Selection

Chapter 8 covers clipboard operations, Visual mode (character/line/block-wise selection), registers (named, clipboard, numbered, special), register recording and playback, editing recordings, and the yanky.nvim plugin for clipboard history management.

| Shortcut | Action |
|----------|--------|
| `p` | Paste clipboard contents after cursor |
| `P` | Paste clipboard contents before cursor |
| `[count]p` | Paste clipboard N times |
| `Control-r` (in Insert mode) | Paste from clipboard (shows register menu) |
| `y<motion>` | Yank (copy) text to clipboard |
| `yy` | Yank entire line |
| `Y` | Yank from cursor to end of line |
| `[count]y<motion>` | Yank with count |
| `v` | Enter Visual Character mode |
| `V` | Enter Visual Line mode |
| `Control-v` | Enter Visual Block mode |
| `Control-v$` | Visual Block mode extending to end of line |
| `j`, `k`, `h`, `l` (in Visual mode) | Move selection |
| `d`/`c`/`y`/`x` (in Visual mode) | Delete/change/yank/delete selection |
| `r<char>` (in Visual mode) | Replace all selected characters with char |
| `Escape` or `v` (in Visual mode) | Exit Visual mode |
| `gv` | Return to last Visual selection |
| `o` (in Visual mode) | Move cursor to opposite end of selection |
| `"` | Show all registers (Normal mode) |
| `"<register><verb>` | Operate using named register (e.g., `"ad3w`) |
| `"<REGISTER><verb>` | Append to named register (e.g., `"Ad3w`) |
| `"a` through `"z` | Access named registers (a-z) |
| `"*` | System clipboard register (Unix selection) |
| `"+` | System clipboard register (explicit copy) |
| `"_` | Black hole register (delete without copying) |
| `"0` | Last yanked text register |
| `".` | Last inserted text register |
| `"1` through `"9` | Numbered registers (most recent deletes) |
| `"-` | Small delete register (less than one line) |
| `"%` | Current filename register |
| `:let @a = @b` | Copy register b contents to register a |
| `Space s"` | Open picker to search and paste from registers |
| `Control-r` (Command mode) | Show registers menu |
| `qa` | Start recording to register a (q-z any letter) |
| `q` | Stop recording |
| `qA` | Append to recording in register a |
| `@a` | Play back recording from register a |
| `@@` | Play back most recently played recording |
| `Q` | Play back most recently recorded command |
| `"ap` | Paste register contents as text (to edit recording) |
| `f2` (after pasting recording) | Jump to character (for editing) |
| `r3` | Replace character (for editing recording) |
| `"ayiw` | Replace register contents with edited text |
| `Space p` | Open Yanky clipboard history picker |
| `[y` | Cycle backward through clipboard history (after paste) |
| `]y` | Cycle forward through clipboard history (after paste) |
| `[p` | Paste on line above with auto-indent |
| `]p` | Paste on line below with auto-indent |
| `>p`/`>P` | Paste with added indentation |
| `<p`/`<P` | Paste with removed indentation |

## Chapter 9. Buffers and Layouts

Chapter 9 covers buffer management (switching, closing, scratch buffers), window splits and navigation, tab layouts, code folding, and session management for preserving editor state across editing sessions.

| Shortcut | Action |
|----------|--------|
| `H` / `L` | Previous/next buffer (Shift+h/l) |
| `[b` / `]b` | Previous/next buffer (Unimpaired style) |
| `[count]H` / `[count]L` | Jump N buffers left/right (with config) |
| `Space <backtick>` | Switch to alternate (most recently open) buffer |
| `Space ,` | Open buffer picker (filterable list) |
| `Space bd` | Delete (close) current buffer |
| `Space bD` | Delete buffer and close its window split |
| `Space bl` | Close all buffers to the left |
| `Space br` | Close all buffers to the right |
| `Space bo` | Close all buffers except current one |
| `Space bp` | Toggle pin on current buffer |
| `Space bP` | Delete all non-pinned buffers |
| `Control-x` (in buffer picker) | Close buffer from picker |
| `Space .` | Open scratch buffer (floating window) |
| `Space S` | Open picker to browse all scratch buffers |
| `Space w` | Open window menu (submode) |
| `Control-w` | Alternative window menu access |
| `Space wv` | Create vertical split (left/right) |
| `Space ws` | Create horizontal split (above/below) |
| `Space \|` | Alternative vertical split keybinding |
| `Space -` | Alternative horizontal split keybinding |
| `Control-v` (in file explorers/pickers) | Open file in vertical split |
| `Control-s` (in file explorers/pickers) | Open file in horizontal split |
| `Control-h` / `Control-j` / `Control-k` / `Control-l` | Navigate between window splits |
| `[count]Control-h` etc. | Navigate by count |
| `Space wh` / `Space wj` / `Space wk` / `Space wl` | Navigate between windows (Space variant) |
| `Space wq` | Close window (or quit if last window) |
| `Space wc` | Close window (error if only window) |
| `Space wd` | Delete window (same as wc) |
| `Space wo` | Close all other windows (keep only active) |
| `Space w+` | Increase active window height |
| `Space w-` | Decrease active window height |
| `Space w>` | Increase active window width |
| `Space w<` | Decrease active window width |
| `Space w=` | Equalize all window sizes |
| `Space w Space` | Enter Hydra mode (pin window menu) |
| `Escape` (in Hydra mode) | Exit Hydra mode |
| `Space uz` | Toggle Zen mode (focus view) |
| `Space uZ` | Toggle Zoom mode (maximize single window) |
| `Space Tab` | Open tab menu |
| `Space Tab Tab` | Create new tab |
| `Space wT` | Move current window split to new tab |
| `gt` | Go to next tab |
| `gT` | Go to previous tab |
| `[count]gt` | Go to specific tab by number |
| `Space Tab [` | Go to previous tab (LazyVim variant) |
| `Space Tab ]` | Go to next tab (LazyVim variant) |
| `Space Tab d` | Close tab (closes windows but keeps buffers) |
| `Space wq` (last window in tab) | Close tab by closing its last window |
| `z` | Open fold mode menu |
| `zc` | Collapse fold at cursor |
| `zo` | Open fold at cursor |
| `za` | Toggle fold at cursor |
| `zR` | Open all folds (reduce folding big) |
| `zr` | Reduce folding level |
| `zO` | Open fold recursively (open nested folds) |
| `Space qq` | Quit Neovim (saves session) |
| `s` (from dashboard) | Open previous session |
| `Space qs` | Restore to previous session state |
| `Space qS` | Open session picker (browse recent projects) |
| `Space qd` | Don't save session on quit |
| `:cd <path>` | Change working directory (changes session) |

## Chapter 10. Programming Language Support

Chapter 10 introduces LazyVim's integrated Language Server Protocol support through language Lazy Extras and Mason.nvim, covering diagnostics, code actions, linting, and formatting configuration.

| Shortcut | Action |
|----------|--------|
| `Space cm` | Open Mason.nvim plugin manager |
| `Space sn` | Open Noice search menu (for notifications) |
| `Space sna` | View all recent Noice messages |
| `Space snl` | View last Noice message |
| `Space snd` | Dismiss current notifications |
| `Space cl` | Show LSP status and health picker |
| `[d` / `]d` | Jump to previous/next diagnostic |
| `[w` / `]w` | Jump to previous/next warning |
| `[e` / `]e` | Jump to previous/next error |
| `Space cd` | Show diagnostic details under cursor |
| `Space xx` | Open Trouble diagnostics (current file) |
| `Space xX` | Open Trouble diagnostics (all workspace) |
| `[q` / `]q` | Navigate Quick Fix/Trouble locations |
| `Control-q` (in picker) | Send picker results to Quick Fix |
| `Alt-t` (in picker) | Send picker results to Trouble window |
| `Space ca` | Open Code Actions menu |
| `Space cf` | Format code (manual invocation) |
| `:lsp restart` | Restart language server |
| `:checkhealth vim.lsp` | Check LSP health status |
| `:checkhealth mason` | Check Mason tools health |
| `:LazyHealth` | Show LazyVim-specific health info |

## Chapter 11. Navigating Source Files

Chapter 11 covers LSP-powered code navigation including go to definition, references, symbol search, and Vim marks for bookmarking locations in code.

| Shortcut | Action |
|----------|--------|
| `gd` | Go to definition (jump to symbol definition) |
| `gr` | Go to references (open picker with references) |
| `Space sR` | Resume previous picker search (references) |
| `K` | Show hover documentation/help for symbol |
| `Space ss` | Search symbols in current file |
| `Space sS` | Search symbols in entire project/workspace |
| `Control-q` (in picker) | Send symbols to Quick Fix |
| `Alt-t` (in picker) | Send symbols to Trouble window |
| `Space cs` | Open Trouble symbols outline sidebar |
| `Space w<` / `Space w>` | Resize Trouble symbols window |
| `s` (Seek mode) | Jump to visible window (including Trouble) |
| `Space ut` | Toggle TreeSitter context display |
| `m[letter]` | Set local mark at letter (a-z) |
| `'[letter]` | Jump to local mark in current file |
| `m[LETTER]` | Set global mark at letter (A-Z) |
| `'[LETTER]` | Jump to global mark from any file |
| `'` | Open marks menu/picker |
| `Space sm` | Search marks in picker |
| `:delmarks [mark]` | Delete specific mark |
| `:delm [mark]` | Delete mark (shorthand) |
| `'a,'b` (in command) | Range between two marks |
| `'<,'>` (in command) | Range of last visual selection |
| `'.` | Jump to last insertion/change point |

## Chapter 12. Searching

Chapter 12 covers searching in Vim including in-file search with `/`, project-wide search with ripgrep, case sensitivity handling, and regular expression patterns.

| Shortcut | Action |
|----------|--------|
| `/[pattern]` | Search in current file (forward) |
| `?[pattern]` | Search in current file (backward) |
| `n` | Jump to next search result |
| `N` | Jump to previous search result |
| `[count]n` / `[count]N` | Jump by count through results |
| `[count]/[pattern]` | Jump to nth occurrence of pattern |
| `Space /` | Search in entire project (live grep) |
| `Alt-s` (in picker) | Add Seek labels to picker results |
| `Alt-t` (in picker) | Send search results to Trouble window |
| `\C` (in search) | Force case sensitivity for search |
| `\c` (in search) | Force case insensitivity for search |
| `:set noignorecase` | Disable smart case (temporary) |
| `:set ignorecase` | Enable smart case |
| `.` (regex) | Match any single character |
| `\S` (regex) | Match any non-whitespace character |
| `*` (regex) | Match preceding expression 0+ times |
| `\+` (regex) | Match preceding expression 1+ times |
| `\=` or `\?` (regex) | Match preceding expression 0 or 1 time |
| `\\` (regex) | Match literal backslash |
| `\/` (regex) | Match literal forward slash |
| `\V` (regex) | Disable regex matching (very nomagic) |

## Chapter 13. And Replacing

Chapter 13 covers find and replace operations including the nvim-rip-substitute plugin for user-friendly substitution, Vim's native `:substitute` command with ranges and flags, project-wide replacement with Grug-far, text case manipulation with text-case.nvim, and bulk editing with `:norm` and `:global`.

| Shortcut | Action |
|----------|--------|
| `g/` | Open rip-substitute find/replace widget |
| `Escape` (in rip-substitute) | Switch to Normal mode |
| `R` (in rip-substitute) | Open current regex in regex101.com |
| `j` / `k` (in rip-substitute) | Switch between search/replace fields |
| `o` (in rip-substitute) | Enter insert mode on next line |
| `Enter` / `Control-Enter` | Execute substitution (rip-substitute) |
| `Up` / `Down` (in rip-substitute) | Cycle through substitution history |
| `:s/pattern/replacement` | Substitute first match on current line |
| `:%s/pattern/replacement` | Substitute all in file (must add /g) |
| `:s/pattern/replacement/g` | Substitute all matches on line (global) |
| `:s/pattern/replacement/gc` | Substitute with confirmation on each |
| `:s/pattern/replacement/i` / `/I` | Case insensitive/sensitive |
| `:.s/` | Substitute current line (dot range) |
| `:%s/` | Substitute entire file (percent range) |
| `:3,8s/pattern/replacement` | Substitute lines 3-8 |
| `:'<,'>s/pattern/replacement` | Substitute visual selection |
| `:,/pattern/s/old/new` | Substitute from current to pattern match |
| `:s//replacement/` | Reuse last search pattern |
| `:s///` | Repeat last substitution exactly |
| `:%sg` | Repeat last substitution globally on all file |
| `'<,'>sg` | Repeat last substitution in visual selection |
| `\0` (in replacement) | Insert entire matched pattern |
| `\1` through `\9` (in replacement) | Insert capture group 1-9 |
| `\(` / `\)` (in pattern) | Define capture group |
| `Space sr` | Open Grug-far project-wide find/replace |
| `j` / `k` (in Grug-far) | Navigate between form fields |
| `Escape` (in Grug-far) | Return to Normal mode |
| `\r` (in Grug-far) | Execute replacement on all matches |
| `dd` (in Grug-far preview) | Delete specific match from replacement |
| `\s` (in Grug-far) | Sync edited preview to source files |
| `Enter` (in Grug-far preview) | Jump to source file of result |
| `\t` (in Grug-far) | Show recent search/replace history |
| `g?` (in Grug-far) | Show Grug-far help menu |
| `ga` | Open text-case menu (requires text-case plugin) |
| `gap` / `gaP` / `gas` | Change text case (pascal/screaming/snake/etc) |
| `gao` | Enter operator-pending mode for case change |
| `:Subs/old/new` | Case-aware substitution (text-case plugin) |
| `:%norm <commands>` | Apply Normal mode commands to all lines |
| `Control-v Escape` | Insert literal escape in command line |
| `q:` | Open command-line history editor window |
| `Control-f` (in cmdline) | Open command-line editor from search |
| `Control-u` (in cmdline window) | Scroll up through command history |
| `?` (in cmdline window) | Search backward in command history |
| `:q` (in cmdline window) | Close command-line history window |
| `:%g/pattern/d` | Delete all lines matching pattern (global) |
| `:%g/pattern/s/old/new` | Substitute only on matching lines |
| `:%g/pattern/norm <commands>` | Apply Normal commands to matching lines |
| `:%g!/pattern/d` | Delete all lines NOT matching pattern |

## Chapter 14. Miscellaneous Editing Tips

Chapter 14 covers miscellaneous editing features including word counts, character transposition, code commenting, number incrementing/decrementing, indentation management, text reflowing, spell checking, abbreviations, and snippets with blink.cmp.

| Shortcut | Action |
|----------|--------|
| `g<Control-g>` | Show word count and cursor position statistics |
| `xp` | Transpose two characters (swap with next char) |
| `gc<motion>` | Comment/uncomment text (e.g., `gc5j`, `gcap`) |
| `gcc` | Comment current line (toggle) |
| `[count]gcc` | Comment multiple lines |
| `gco` / `gcO` | Add comment line below/above current |
| `V5j gc` | Comment in Visual mode (5 lines) |
| `Control-a` | Increment number under cursor |
| `Control-x` | Decrement number under cursor |
| `g<Control-a>` | Increment on selected lines with offset |
| `g<Control-x>` | Decrement on selected lines with offset |
| `>>` | Indent current line |
| `<<` | Dedent current line |
| `>Sx` | Indent TreeSitter entity by label `x` |
| `>ap` | Indent paragraph |
| `v5>` | Indent current line by 5 levels (Visual mode) |
| `va{5>` | Indent entire block 5 levels |
| `gq<motion>` | Reflow text at textwidth (wrap text) |
| `gqw` | Reflow current line |
| `gqip` | Reflow paragraph |
| `gwig` | Reflow entire file |
| `=<motion>` | Apply indentation engine to text |
| `gqag` | Format entire file |
| `Control-t` (Insert mode) | Indent current line while inserting |
| `Control-d` (Insert mode) | Dedent current line while inserting |
| `!'<,'>!<command>` (Visual) | Pipe selection through external command |
| `Space us` | Toggle spell check |
| `[s` / `]s` | Jump between spelling errors |
| `z=` | Show spelling suggestions menu |
| `Control-o` (Insert mode) | Perform one Normal mode command, stay in Insert |
| `Control-a` (Insert mode) | Insert text from previous Insert mode session |
| `Control-r` (Insert mode) | Access registers menu |
| `Control-r+` (Insert mode) | Paste from system clipboard |
| `Control-u` (Insert mode) | Delete all text on current line since Insert start |
| `:iabbr shortcut expansion` | Create abbreviation (Insert mode) |
| `Control-]` (Insert mode) | Trigger abbreviation without space |
| `Escape` (after abbr) | Insert abbreviation text without expanding |
| `Tab` (in snippet) | Jump to next snippet tab stop |
| `Control-y` / `Enter` | Confirm and insert snippet |

## Chapter 15. Source Control

Chapter 15 covers Git integration including checking git status, interacting with GitHub issues and PRs, staging hunks, git blame, integrated terminal, Lazygit, diff mode with side-by-side viewing, merge conflict resolution, and git-conflict.nvim.

| Shortcut | Action |
|----------|--------|
| `Control-/` | Toggle integrated terminal (floating window) |
| `Escape Escape` | Exit terminal mode to Normal mode |
| `Control-\ Control-n` | Exit terminal mode (default keybinding) |
| `a` / `i` (in terminal) | Enter terminal mode (send keystrokes) |
| `Space gs` | Git status picker (modified files list) |
| `Tab` (in git status) | Stage/unstage file |
| `Space gl` | Git log picker (commit history) |
| `:lua Snacks.picker.git_branches()` | Show git branches picker |
| `Space gi` | List open GitHub issues |
| `Space gI` | List all GitHub issues (including closed) |
| `Enter` (in issue picker) | Show actions menu for issue |
| `i` (in issue buffer) | Edit issue title and body |
| `a` (in issue buffer) | Add new comment to issue |
| `c` (in issue buffer) | Close issue |
| `o` (in issue buffer) | Reopen closed issue |
| `Space gp` | List open pull requests |
| `Space gP` | List all pull requests (including closed) |
| `Enter` (in PR picker) | Show actions menu for PR |
| `alt-w` (in PR diff preview) | Focus preview area for navigation |
| `Control-s` (in PR comment) | Submit review comment |
| `Space gh` | Git hunks menu (staging/blame operations) |
| `Space ghs` | Stage current hunk |
| `Space ghS` | Stage entire file |
| `[h` / `]h` | Jump to previous/next hunk |
| `Space ghr` | Reset hunk to last commit state |
| `Space ghR` | Reset entire file to last commit |
| `Space ghu` | Unstage hunk (keep changes) |
| `Space ghb` | Show blame line (last commit and author) |
| `Space ghp` | Preview hunk (show before/after side-by-side) |
| `Space ghd` | Show diff against git index |
| `Space ghD` | Show diff against last commit |
| `Space gg` | Open Lazygit terminal UI |
| `:diffoff` | Disable diff mode view for current buffer |
| `zo` | Open folded identical code sections |
| `dp` | Diff put (make other window same as current) |
| `do` | Diff obtain (make current same as other) |
| `[c` / `]c` | Jump between changes (diff mode only) |
| `:diffg [#]` / `:diffget` | Get changes from specified buffer |
| `:diffp [#]` / `:diffput` | Put changes to specified buffer |
| `Space gx` | List all conflict markers in file |
| `Space gr` | Refresh conflict detection |
| `[x` / `]x` | Jump between conflict markers |
| `Space ho` | Choose ours (top/local version) |
| `Space ht` | Choose theirs (bottom/remote version) |
| `Space hb` | Choose both versions |
| `Space h0` | Choose base/middle version |

## Chapter 16. Configuring Artificial Intelligence

Chapter 16 covers AI integration options including Sidekick.nvim for next-edit suggestions and CLI tool wrapping, Copilot Chat for interactive chat-based coding, and overview of other AI plugins and external tools available for LazyVim.

### AI Tools and Plugins Available

| Tool/Plugin | Purpose |
|-------------|---------|
| Sidekick.nvim | Official LazyVim plugin for CLI tool management and next-edit suggestions |
| Copilot Chat | In-editor chat interface with GitHub Copilot models |
| Claude Code | External CLI tool by Anthropic (recommended for best performance) |
| Codex (OpenAI) | External CLI tool for AI-driven coding |
| Gemini CLI | Google's AI CLI tool for coding assistance |
| Avante.nvim | Attempts Cursor-like automated coding experience (experimental) |
| Code Companion.nvim | Well-maintained alternative with more model providers |
| claudecode.nvim | Emulates VSCode plugin via websocket connection |
| supermaven-nvim | Legacy AI completion plugin (outdated) |
| codeium | Legacy completion plugin (outdated) |
| tabnine | Legacy completion plugin (outdated) |
| Exa API | Web search integration for AI context |
| Tavily API | Web search integration for AI context |
| Firecrawl API | Web search integration for AI context |

### Key Keybindings

| Shortcut | Action |
|----------|--------|
| `:LspCopilotSignIn` | Authenticate with GitHub Copilot |
| `Space aa` | Toggle Copilot Chat / Show available AI tools menu |
| `Control-s` (Insert) / `Enter` (Normal) | Send message in Copilot Chat |
| `#` (in chat) | Add resource to chat message (shows menu) |
| `#file:path` | Include specific file in chat context |
| `#buffer:active` | Include most recently active buffer |
| `#buffer:visible` | Include all visible buffers in chat |
| `#selection` | Include most recent visual selection |
| `#url:<url>` | Fetch and include web content in chat |
| `>` (prefix) | Make resource sticky (persist across messages) |
| `$` (in chat) | Change AI model for single message |
| `/` (in chat) | Access predefined prompt templates |
| `@` (in chat) | Enable tools for LLM invocation |
| `@bash` | Enable bash tool specifically |
| `> @copilot` | Enable all default tools (sticky) |
| `Space af` | Send current filename to AI tool |
| `Space av` | Send visual selection to AI tool |
| `Space at` | Send cursor position to AI tool |
| `Space ap` | Use stored prompts menu |

## Chapter 17. Debugging

Chapter 17 covers the Debug Adapter Protocol (DAP) integration including setting breakpoints, stepping through code, viewing variables and locals, conditional breakpoints, remote debugging in containers, and Chrome browser debugging.

| Shortcut | Action |
|----------|--------|
| `Space d` | Open debug menu and commands |
| `Space db` | Set breakpoint at cursor line |
| `Space dB` | Set conditional breakpoint (enter condition) |
| `Space da` | Start debugger (select run environment/config) |
| `Space dl` | Run last debug configuration (no prompts) |
| `Space dc` | Continue execution to next breakpoint |
| `Space dO` | Step over (execute next line, skip function calls) |
| `Space di` | Step into (enter function being called) |
| `Space do` | Step out (exit current function, go to caller) |
| `Space du` | Toggle DAP UI visibility (show/hide sidebar) |
| `s` (Seek mode) | Jump to DAP sidebar from editor |
| `Enter` (in locals/watches) | Expand variable/expression to see children |
| `e` (in locals window) | Edit variable value live during debugging |
| `i` (in watches window) | Enter Insert mode to add new watch expression |
| `j` / `k` (in sidebar) | Navigate between locals, watches, stack, breakpoints |
| `Space cm` | Open Mason to install debug adapters |
| `i` (in Mason) | Install debug adapter for language |
| `Space qq` | Quit Neovim (save debug session state) |
| `s` (from dashboard) | Restore previous session with debugger state |

## Chapter 18. Testing

Chapter 18 covers the Neotest plugin for running tests, viewing results, managing test summary window, watch mode, configuring test runners for different languages, and implementing custom test adapters.

| Shortcut | Action |
|----------|--------|
| `Space t` | Open test menu (shows all test commands) |
| `Space tt` | Run tests in current file |
| `Space tr` | Run single test under cursor |
| `Space tT` | Run all tests in project (capital T) |
| `Space to` | Show test output in floating window |
| `Space tO` | Show test output in pane (better with edgy extra) |
| `q` (in output) | Close test output floating window |
| `[q` / `]q` | Jump between failing tests (via Trouble) |
| `Space ts` | Toggle test summary sidebar window |
| `?` (in summary) | Show all keybindings available in summary |
| `J` / `K` (in summary) | Jump up/down in summary (large movements) |
| `j` / `k` (in summary) | Navigate between tests line-by-line |
| `m` (in summary) | Mark test as "of interest" |
| `M` (in summary) | Clear all marks |
| `R` (in summary) | Run only marked tests |
| `Space tw` | Toggle watch mode (auto-rerun on file save) |
| `Space td` | Debug test (stops at first failure) |
| `Space cm` | Open Mason to install test runners |
| `i` (in Mason) | Install test adapter/runner for language |

## Chapter 19: Comprehensive Guide to LazyVim Configuration

**Summary**: Comprehensive guide covering plugin directory structure, plugin specifications, lifecycle methods, options configuration, color schemes, lazy loading, filetype-specific configurations, and per-project customization for extending LazyVim.

| Shortcut | Action |
| -- | -- |
| `Space fc` | Find/open plugin configuration files |
| `Space ub` | Toggle background (light/dark) |
| `Space uC` | Open color scheme picker |
| `:set ft` | Display current buffer filetype |
| `:help option-list` | View all Vim options |
| `:help events` | View all Neovim events for lazy loading |
| `:help autocmd-events` | View all autocommand events |
| `.lazy.lua` | Create project-specific LazyVim config file |
| `vim.opt.<option>` | Set Vim option (in Lua config) |
| `vim.g.<varname>` | Set global variable (in Lua config) |
| `lua/plugins` | Plugin directory (auto-loaded by Lazy) |
| `lua/config/options.lua` | Global Vim options configuration file |
| `lua/config/autocmds.lua` | Autocommands configuration file |
| `require('plugin').setup({...})` | Standard plugin setup pattern |
| `opts = function(_, opts)` | Modify options in-place with function |
| `build` option | Run command on plugin install/update |
| `config` option | Run Lua function when plugin loads |
| `init` option | Run Lua function during program startup |
| `lazy = false` | Force plugin to load on startup |
| `ft` key in spec | Lazy load plugin only for specific filetypes |
| `cmd` key in spec | Lazy load plugin only when commands used |
| `branch`, `tag`, `commit` | Pin plugin to specific version |
| `colorscheme` opt | Set color scheme in LazyVim config |

## Chapter 20: Where to Go Next

**Summary**: Resource guide for continuing your LazyVim and Neovim learning journey, including documentation, community discussions, plugin discovery, notable dotfiles, and GUI options.

### Key Resources

| Resource | URL/Description |
| -- | -- |
| **This Book (Latest)** | https://lazyvim-ambitious-devs.phillips.codes |
| **Official Website** | https://www.lazyvim.org (comprehensive plugin reference) |
| **Neovim Help** | `:help` or `:help user-manual` (in Neovim) |
| **Neovim Docs (Web)** | https://neovim.io/doc/user/usr_toc.html |
| **LazyVim Discussions** | https://github.com/LazyVim/LazyVim/discussions |
| **Awesome Neovim** | https://github.com/rockerBOO/awesome-neovim (plugin discovery) |
| **Neovimcraft** | https://neovimcraft.com (plugin discovery) |
| **LazyVim Recipes** | https://www.lazyvim.org/configuration/recipes |

### Notable Dotfiles & Contributors

| Person | Link | Notable For |
| -- | -- | -- |
| **Folke Lemaitre** | https://github.com/folke/dot | LazyVim creator, plugin author |
| **Evgeni Chasnovski** | https://github.com/echasnovski/nvim/ | mini.nvim author, Neovim core contributor |
| **Iordanis Petkakis** | https://github.com/dpetka2001/dotfiles | Active in LazyVim discussions |
| **Dusty Phillips** | https://github.com/dusty-phillips/dotfiles/ | This book's author |

### Recommended Neovim GUIs

| GUI | Platform | Best For |
| -- | -- | -- |
| **Vimr** | macOS | macOS integrations |
| **Neovide** | Cross-platform | Smooth animations & scrolling |
| **Goneovim** | Cross-platform | Solid alternative to Neovide |

### Learning Tips

- **Reread this book** to catch interesting details missed on first pass
- **Handwrite a cheat sheet** of "cool but won't memorize" keybindings for better retention
- **Use `:help` documentation** extensively—it's comprehensive and interlinked like a wiki
- **Use `Control-]`** to follow wiki-style links in help documentation
- **Check LazyVim website** when tweaking plugin configurations (Options & Full Spec tabs)
- **Create minimal repro** with `repro.lua` when filing GitHub issues for bugs
- **Look at other users' dotfiles** for configuration inspiration and plugin discovery
