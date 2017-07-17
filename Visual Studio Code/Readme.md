# Visual Studio Code

_Version 1.14.0_

## Extensions

* Markdown Shortcuts
* Markdown PDF
* Copy Markdown as HTML
* Visual Studio Keymap
* Code Spellchecker

### Note
_Issue is fixed in 1.15 insider preview_

Version 1.9 seems to be the last one working behind a proxy. Bug needs to be investigated further each update. For 1.9 some settings aren't saved to the json file. Theme should be set to Visual Studio Light, and icons to vscode-icons once plugin is installed.

Joining lines is now built in the editor since version 1.8. Shortcut needs to be assigned.

## Settings file

```json
// Version 1.12.1 and up
{
    "workbench.colorTheme": "Visual Studio Light",
    "[markdown]": {
        "editor.wordWrap": "wordWrapColumn",
        "editor.wordWrapColumn": 120,
        "editor.quickSuggestions": false
    }
}
```

## Keybindings
The following keybindings define the command for collapsing all lines into one long string, in order to "minify" the html. The second one is for the extension copy markdown as html which allow the html render of the markdown file to be copied.

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

## Markdown PDF Extension
The markdown pdf extension offers a lot of customization options. Customizing them allows for a "perfect" markdown experience.

### Workspace / user settings
The settings can be set per workspace or globally, for markdown, workspace / repo settings could be preferred. Here are the "common" settings, *based on Terra-Nova git repository configuration*.

```js
{
    "markdown-pdf.format": "Letter",
    "markdown-pdf.type": "pdf",
    "markdown-pdf.border.top": "2cm",
    "markdown-pdf.border.bottom": "2cm",
    "markdown-pdf.border.right": "2cm",
    "markdown-pdf.border.left": "2cm",
    "markdown-pdf.header.contents": "",
    "markdown-pdf.header.height": "",
    "markdown-pdf.footer.contents": "",
    "markdown-pdf.footer.height": "",
    "markdown-pdf.styles": [
        ".vscode/style.css"
    ],
    "cSpell.enabled": true
}
```

### Pdf styling
The pdf export can also be customized, fonts etc. Doing so should be done per workspace for better customization of the exported file.

_Here is an example config based on Terra-Nova project_.

```css
body {
	font-family: "Cambria", 'Times New Roman', Times, serif;
	font-size: 12px;
	padding: 0 12px;
	line-height: 18px;
	word-wrap: break-word;
}

h1, h2, h3, h4, h5, h6 {
	font-family: "Segoe WPC", "Segoe UI", "SFUIText-Light", "HelveticaNeue-Light", sans-serif, "Droid Sans Fallback";
	color: #4080D0;
	font-weight: normal;
}
```
