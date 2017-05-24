# Visual Studio Code

_Version 1.12.1_

## Extensions

* Markdown Shortcuts
* Markdown PDF
* Copy Markdown as HTML
* Visual Studio Keymap
* ~~vscode-icons~~
* file-icons

_Potentially_  
Currently has some issues with rules that aren't necessary.

* Markdown lint (_Usefull for making good markdown, might not be usefull all the time._)

### Note

Version 1.9 seems to be the last one working behind a proxy. Bug needs to be investigated further each update. For 1.9 some settings aren't saved to the json file. Theme should be set to Visual Studio Light, and icons to vscode-icons once plugin is installed.

Joining lines is now built in the editor since version 1.8. Shortcut needs to be assigned.
<!--TODO: Assing shortcut to join lines-->

## Settings file

```json
// Version 1.9 settings
{
    "update.channel": "none",
    "editor.fontSize": 14,
    "editor.wrappingColumn": 0,
    "markdown-pdf.type": "html",
    "[markdown]": {
        "editor.wordWrap": true,
        "editor.wrappingColumn": 120,
        "editor.quickSuggestions": false
    }
}
```

```json
// Version 1.12.1 and up
{
    "workbench.colorTheme": "Visual Studio Light",
    "workbench.iconTheme": "vs-minimal",
    "[markdown]": {
        "editor.wordWrap": "wordWrapColumn",
        "editor.wordWrapColumn": 120,
        "editor.quickSuggestions": false
    }
}
```

## Keybindings
The following keybinds define the command for collapsing all lines into one long string, in order to "minify" the html. The second one is for the extension copy markdown as html which allow the html render of the markdown file to be copied.

```json
[
    {
        "key": "ctrl+k ctrl+j",
        "command": "editor.action.joinLines",
        "when": "editorTextFocus"
    },
    {
        "key": "ctrl+k ctrl+l",
        "command": "extension.copyAsHtml",
        "when": "editorTextFocus"
    }
]
```
<!--TODO: Chage icon theme to file-icons-->
