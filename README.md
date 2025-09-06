## Paste this JSON config in User Settings (JSON) in VS code/Cursor IDE for black background theme with dim white text
```json
{
    "workbench.colorTheme": "Default High Contrast",
    "editor.fontSize": 18,
    "editor.wordWrap": "on",
    "files.autoSave": "afterDelay",
    "editor.tokenColorCustomizations": {
        "[Default High Contrast]": {
            "textMateRules": [
                {
                    "scope": [
                        "source",
                        "variable",
                        "meta.function-call.generic",
                        "support.variable"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "variable.other.constant.python"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "entity.name.function",
                        "support.function",
                        "punctuation",
                        "entity.name.function.decorator"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "keyword.operator"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "meta.paragraph.markdown",
                        "markup.inline.raw.string.markdown"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "markup.inserted.diff",
                        "markup.deleted.diff"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                // --- FINAL COMPREHENSIVE FIX for code in Markdown ---
                {
                    "scope": [
                        "fenced_code.block.language.markdown",      // For the 'diff' keyword
                        "markup.fenced_code.block.markdown keyword",  // For keywords like 'from', 'import'
                        "markup.fenced_code.block.markdown storage.type", // For types like 'str', 'Optional'
                        "markup.fenced_code.block.markdown constant.language", // For 'None', 'True'
                        "markup.fenced_code.block.markdown support.type" // For built-in types like 'List'
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "meta.diff.header",
                        "meta.diff.index",
                        "meta.diff.header.from-file",
                        "meta.diff.header.to-file",
                        "meta.diff.range"
                    ],
                    "settings": {
                        "foreground": "#88ddff"
                    }
                },
                {
                    "scope": [
                        "meta.tag.jsx.children",
                        "string.unquoted.plain.in.jsx"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                },
                {
                    "scope": [
                        "text.html.derivative"
                    ],
                    "settings": {
                        "foreground": "#b4b4b4"
                    }
                }
            ]
        }
    },
    "workbench.colorCustomizations": {
        "[Default High Contrast]": {
            "foreground": "#CCCCCC",
            "sideBar.foreground": "#CCCCCC",
            "sideBarTitle.foreground": "#CCCCCC",
            "menu.foreground": "#CCCCCC",
            "icon.foreground": "#CCCCCC",
            "statusBar.foreground": "#b4b4b4",
            "statusBar.noFolderForeground": "#b4b4b4",
            "editor.foreground": "#b4b4b4",
            "terminal.foreground": "#b4b4b4",
            "editor.selectionBackground": "#555555",
            "terminal.selectionBackground": "#555555",
            "editorLineNumber.foreground": "#AAAAAA",
            "editorLineNumber.activeForeground": "#D6D6D6",
            "tab.activeForeground": "#E0E0E0",
            "tab.inactiveForeground": "#A0A0A0",
            "panelTitle.activeForeground": "#E0E0E0",
            "panelTitle.inactiveForeground": "#A0A0A0",
            "breadcrumb.foreground": "#f8f8f8",
            "breadcrumb.focusForeground": "#FFFFFF",
            "breadcrumb.activeSelectionForeground": "#FFFFFF",
            "breadcrumb.background": "#000000",
            "editorIndentGuide.background1": "#404040",
            "editorIndentGuide.activeBackground1": "#707070",
            "terminal.ansiBrightWhite": "#b4b4b4",
            "terminal.ansiWhite": "#b4b4b4",
            "diffEditor.insertedTextForeground": "#b4b4b4",
            "diffEditor.removedTextForeground": "#b4b4b4"
        }
    },
    "cursor.composer.shouldQueueWhenGenerating": false,
    "cursor.composer.textSizeScale": 1.15,
    "terminal.integrated.defaultProfile.windows": "Git Bash",
    //created for claude code
    "terminal.integrated.env.linux": {
        "FORCE_COLOR": "0"
    },
    "roo-cline.allowedCommands": [
        "npm test",
        "npm install",
        "tsc",
        "git log",
        "git diff",
        "git show"
    ],
    "roo-cline.deniedCommands": [],
    "git.autofetch": true
}
```
