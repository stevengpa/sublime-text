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

```jsonc
{
    "font_size": 18,
    "tab_size": 2,
    "ignored_packages": [
        "Vintage",
    ],
    "theme": "One.sublime-theme",
    "color_scheme": "Nord.sublime-color-scheme",
    "index_files": true,
    "ui_scale": 1.2,
    "trim_trailing_white_space_on_save": "all",
}
```



### Keybindings

Sublime Text > Settings > Keybindings

```jsonc
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
    {
        "keys": [
            "ctrl+shift+s",
            "z"
        ],
        "command": "toggle_distraction_free"
    }
]
```

### Installed Packages

Sublime Text > Settings > Package Settings > Package Control > Settings

```jsonc
{
    "bootstrapped": true,
    "in_process_packages": [
    ],
    "installed_packages": [
        "A File Icon",
        "AdvancedNewFile",
        "AsciiDoc",
        "AutoPEP8",
        "AutoSetSyntax",
        "BracketHighlighter",
        "ChannelRepositoryTools",
        "CodeMap",
        "ColorHelper",
        "Containerfile",
        "Crontab",
        "CTags",
        "Debian Syntax",
        "Djaneiro",
        "DotENV",
        "Emmet",
        "Formatter",
        "GenerateUUID",
        "Git badges like VS Code",
        "Git Conflict Resolver",
        "GitDiffView",
        "Gitignore",
        "GitSavvy",
        "Hosts",
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
        "LSP-rust-analyzer",
        "LSP-stylelint",
        "LSP-tailwindcss",
        "LSP-typescript",
        "LSP-vue",
        "LSP-yaml",
        "MarkdownPreview",
        "Material Theme",
        "Nord",
        "Origami",
        "Package Control",
        "PackageDev",
        "Python 3",
        "Python Fix Imports",
        "SideBarEnhancements",
        "SSH Config",
        "Status Bar Time",
        "Statusbar Path",
        "SublimeLinter",
        "SublimeLinter-annotations",
        "SublimeLinter-contrib-sublime-syntax",
        "SublimeLinter-eslint",
        "SublimeLinter-php",
        "SublimeLinter-php-cs-fixer",
        "SublimeLinter-phpcs",
        "TabTeleport",
        "Terminus",
        "Terraform",
        "Theme - One",
        "YamlPipelines",
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

Sublime Text > Settings > Package Settings > CTags > CTags Settings

```jsonc
{
  "command": "/opt/homebrew/bin/ctags",
  "tag_file": "tags",
  "autocomplete": true,
  "auto_reload_tags_file": true
}
```

### Status Bar Time

Sublime Text > Settings > Package Settings > StatusBarTime > User - Settings

```jsonc
{
    "StatusBarClock_display_onlyinview": true,
    "StatusBarTime_format": "%I:%M %p"
}
```

- ctrl/cmd + p - CTags Rebuild

## PHP Configs

### PHP CS Fixer

```bash
composer global require friendsofphp/php-cs-fixer
```

```bash
php-cs-fixer --version
```

.zshrc or .bashrc

```bash
export PATH="$HOME/.config/composer/vendor/bin:$PATH"

//or

export PATH="$HOME/.composer/vendor/bin:$PATH"
```

### PHP CODE SNIFFER


```bash
composer global require "squizlabs/php_codesniffer=*"
```

```bash
phpcs --version
```

In case of issues with `which` command:

```bash
composer global config bin-dir --absolute
```

```bash
source ~/.zshrc
```

### Sublime Config

Palette → “Preferences: SublimeLinter Settings”

```bash
which phpcs
```

```bash
which eslint
```

```bash
which dirname $(which node)
```

```jsonc
// SublimeLinter Settings - User
{
    // "debug": true,
    "linters": {
        "phpcs": {
            "executable": "<path_to>/phpcs",
            "standard": "PSR2", // or "PSR2", "PEAR", custom ruleset path, etc.
            "args": [
                "--exclude=PEAR.Commenting.ClassComment.Missing"
            ]
        },
        "eslint": {
            "prefer_eslint_d": false,
            "executable": "${folder}/node_modules/.bin/eslint",
            "env": {
                "PATH": "<path_to_node>/bin:$PATH"
            },
            "excludes": [
                "*.php",
                "*.md",
                "*.json",
                "*.sublime-settings",
                "*.yml",
                "*.yaml"
            ]
        }
    },
    "show_panel_on_save": "view"
}
```

### Formatter

Palette -> "Preferences: Formatter Settings"


```bash
which phpcbf
```

```jsonc
{
    "auto_format": {
        "config": {
            "format_on_save": true,
            "format_on_paste": true
        },
        "php": {
            "uid": "phpcbf"
        }
    },
    "formatters": {
        "phpcbf": {
            "enable": true,
            "format_on_save": true,
            "format_on_paste": true,
            "executable_path": "<path_to>/phpcbf"
        }
    }
}
```

### Rust Enhanced

Sublime Text > Settings > Package Settings > Rust Enhanced > Settings


```bash
which cargo
```


```jsonc
{
    // These are the folders opened in the project.
    "folders": [
        {
            "path": "."
        }
    ],
    "settings": {
        "rust_syntax_checking": true,
        "rust_syntax_checking_method": "clippy",
        "rust_syntax_checking_include_tests": true,
        "rust_env": {
            "PATH": "$PATH:$HOME/.cargo/bin"
        }
    }
}
```


### Sublime Text - Fedora Installation

Add import

```shell
sudo dnf config-manager addrepo --from-repofile=https://download.sublimetext.com/rpm/dev/x86_64/sublime-text.repo
```

Install

````shell
sudo dnf install sublime-text
````
