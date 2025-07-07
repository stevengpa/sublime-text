## Sublime Text Shortcuts

---

### Panels

|   Plugin   | Shortcut                         | Action                                    |
| :--------: | -------------------------------- | ----------------------------------------- |
|  Origami   | ctrl/cmd+k, →                    | Create/Focus panel to the right           |
|  Origami   | ctrl/cmd+k, ←                    | Create/Focus panel to the left            |
|  Origami   | ctrl/cmd+k, ctrl/cmd+arrow       | Create an adjacent panel                  |
|  Origami   | ctrl/cmd+k, ctrl/cmd+shift+arrow | Destroy an adjacent panel                 |
|  Origami   | ctrl/cmd+k, shift+arrow          | Move the current file to the destination  |
|  Origami   | ctrl/cmd+k,  alt/option+arrow    | Clone the current file to the destination |
| **Native** | cmd+k, cmd + b                   | Open explore panel                        |
|  Terminus  | ctrl/cmd+shift+t                 | Toogle Terminal                           |
|            |                                  |                                           |

### Code Navigation

|   Plugin   | Shortcut           | Action                          |
| :--------: | ------------------ | ------------------------------- |
| **Native** | ctrl+g             | Go to line                      |
|   CTags    | ctrl+t, ctrl+t     | Go to definition                |
|   CTags    | ctrl+t, ctrl+b     | Jump back                       |
|   CTags    | alt/option+shift+s | Show Symbols (All files)        |
|   CTags    | alt/option+s       | Show Symbols (In open tab)      |
| **Native** | crtl/cmd+r         | Show Symbols (In open tab)      |
| **Native** | ctrl/cmd+shift+r   | Show Symbols (In open tabs)     |
| **Native** | ctrl+l             | Position view at center of line |
| **Native** | ctrl+minus         | Jump Back                       |
| **Native** | ctrl+shift+minus   | Jump Forward                    |
|            |                    |                                 |

### View/Line modification

|   Plugin   | Shortcut               | Action            |
| :--------: | ---------------------- | ----------------- |
| **Native** | ctrl+cmd+up/down       | Swap line         |
| **Native** | ctrl/cmd+k, ctrl/cmd+1 | Fold level 1      |
| **Native** | ctrl/cmd+k, ctrl/cmd+3 | Unfold level 1    |
| **Native** | ctrl/cmd+k, ctrl/cmd+u | Uppercase         |
| **Native** | ctrl/cmd+k, ctrl/cmd+l | Lowercase         |
| **Native** | ctrl/cmd+]             | Indent line right |
| **Native** | ctrl/cmd+[             | Indent line left  |
|            |                        |                   |

### Bookmarks

|    Plugin     | Shortcut        | Action                          |
| :-----------: | --------------- | ------------------------------- |
|  **Native**   | ctrl+shift+b, m | Toggle Bookmark                 |
|  **Native**   | ctrl+shift+b, ↓ | Next Bookmark                   |
|  **Native**   | ctrl+shift+b, ↑ | Previous Bookmark               |
|  **Native**   | ctrl+shift+b, c | Clear All Bookmarks in open tab |
| RoadBookmarks | ctrl+shift+b, a | Show All Global Bookmarks panel |



### Settings

Sublime Text > Settings > Settings

```json
{
	"font_size": 18,
	"tab_size": 2,
	"ignored_packages":
	[
		"Vintage",
	],
	"theme": "One.sublime-theme",
	"color_scheme": "Nord.sublime-color-scheme",
	"index_files": false,
	"ui_scale": 1.2,
}
```



### Keybindings

Sublime Text > Settings > Keybindings

```json
[
    // Goto Definition
    {
        "keys": [
            "super+b"
        ],
        "command": "lsp_symbol_definition",
        "args": {
            "side_by_side": false,
            "force_group": true,
            "fallback": false,
            "group": -1
        },
        "context": [
            {
                "key": "lsp.session_with_capability",
                "operand": "definitionProvider"
            },
            {
                "key": "auto_complete_visible",
                "operand": false
            }
        ]
    },
    // Find References (side-by-side)
    {
        "keys": [
            "primary+shift+f"
        ],
        "command": "lsp_symbol_references",
        "args": {
            "side_by_side": true,
            "force_group": true,
            "fallback": false,
            "group": -1
        },
        "context": [
            {
                "key": "lsp.session_with_capability",
                "operand": "referencesProvider"
            }
        ]
    },
    // Save all open files with lsp_save
    {
        "keys": [
            "super+s"
        ],
        "command": "lsp_save_all"
    },
    // Rename
    {
        "keys": [
            "primary+alt+r"
        ],
        "command": "lsp_symbol_rename",
        "context": [
            {
                "key": "lsp.session_with_capability",
                "operand": "renameProvider"
            }
        ]
    },
    // Toggle the default shell in panel
    {
        "keys": [
            "primary+shift+t"
        ],
        "command": "toggle_terminus_panel"
    },
    // ** BOOKMARKS **
    // Toggle a bookmark at the current line
    {
        "keys": [
            "ctrl+shift+b",
            "m"
        ],
        "command": "toggle_bookmark",
        "args": {
            "toggle_line": true
        }
    },
    // Jump to the next bookmark
    {
        "keys": [
            "ctrl+shift+b",
            "down"
        ],
        "command": "next_bookmark"
    },
    // Jump to the previous bookmark
    {
        "keys": [
            "ctrl+shift+b",
            "up"
        ],
        "command": "prev_bookmark"
    },
    // Clear all bookmarks
    {
        "keys": [
            "ctrl+shift+b",
            "c"
        ],
        "command": "clear_bookmarks"
    },
    // Show all bookmarks
    {
        "keys": [
            "ctrl+shift+b",
            "a"
        ],
        "command": "road_bookmarks_panel"
    },
]
```



### (ctrl/cmd+p) Preferences: LSP Settings

```json
// Settings in here override those in "LSP/LSP.sublime-settings"
{
	"lsp_save_all": {
		"only_files": true
	},
	"lsp_format_on_save": true,
	"lsp_format_on_paste": true,
	"only_show_lsp_completions": true
}
```

### Installed Packages

Sublime Text > Settings > Package Settings > Package Control > Settings

```json
{
	"bootstrapped": true,
	"in_process_packages":
	[
	],
	"installed_packages":
	[
		"A File Icon",
		"AutoPEP8",
		"BracketHighlighter",
		"ChannelRepositoryTools",
		"CodeMap",
		"CTags",
		"Djaneiro",
		"DotENV",
		"Emmet",
		"GenerateUUID",
		"Git Conflict Resolver",
		"GitDiffView",
		"Gitignore",
		"GitSavvy",
		"Laravel Blade",
		"LSP",
		"LSP-clangd",
		"LSP-css",
		"LSP-Deno",
		"LSP-dockerfile",
		"LSP-eslint",
		"LSP-file-watcher-chokidar",
		"LSP-gopls",
		"LSP-html",
		"LSP-json",
		"LSP-pyright",
		"LSP-stylelint",
		"LSP-tailwindcss",
		"LSP-typescript",
		"LSP-vue",
		"LSP-yaml",
		"MarkdownPreview",
		"Nord",
		"Origami",
		"Package Control",
		"PackageDev",
		"Python 3",
		"Python Fix Imports",
		"SideBarEnhancements",
		"TabTeleport",
		"Terminus",
		"Theme - One",
	],
}

```



### CTags

```shell
brew install ctags
```

```shell
sudo dnf install ctags
```

Preferences → Package Settings → CTags → CTags Settings

```json
{
  "command": "/opt/homebrew/bin/ctags",
  "tag_file": "tags",
  "autocomplete": true,
  "auto_reload_tags_file": true
}
```

- ctrl/cmd + p - CTags Rebuild



### Sublime Text - Fedora Installation

Add import

```shell
sudo dnf config-manager addrepo --from-repofile=https://download.sublimetext.com/rpm/dev/x86_64/sublime-text.repo
```

Install

````shell
sudo dnf install sublime-text
````

