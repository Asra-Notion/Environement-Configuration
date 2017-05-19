# Visual Studio Code

Version _1.12.1_

## Extensions

* Markdown Shortcuts
* Markdown PDF
* Copy Markdown as HTML
* Visual Studio Keymap
* vscode-icons


* Markdown lint (_Usefull for making good markdown, might not be usefull all the time._)

### Note

Version 1.9 seems to be the last one working behind a proxy. Bug needs to be investigated further each update. For 1.9 some settings aren't saved to the json file. Theme should be set to Visual Studio Light, and icons to vscode-icons once plugin is installed.

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

<!--TODO: Chage icon theme to vscode-icons-->
