# Visual Studio Code

_Version 1.16.1_

## Extensions

* Markdown Shortcuts
* Markdown PDF
* Copy Markdown as HTML
* Code Spellchecker `cspell`
* vscode-pandoc

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

## Vscode Pandoc
The extension allows seemless use of pandoc to render pdf files. This setting can be set per workspace or globaly. In addition of using pandoc to render your pdf, the extension also allows for use of command line arguments. Adding the following setting will ensure that the paper size is letter and that the margins are smaller than pandoc's default.

```json
{
    "pandoc.pdfOptString": "-V geometry:letterpaper -V geometry:margin=3cm"
}
```

## Markdown PDF Extension
The markdown pdf extension offers a lot of customization options. Customizing them allows for a "perfect" markdown experience.

### Workspace / user settings
The settings can be set per workspace or globally, for markdown, workspace / repo settings could be preferred. Here are the "common" settings, *based on Terra-Nova git repository configuration*.

```json
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
	font-family: "Segoe WPC", "Segoe UI", "SFUIText-Light", 
    "HelveticaNeue-Light", sans-serif, "Droid Sans Fallback";
	color: #4080D0;
	font-weight: normal;
}
```

## Markdown custom snippets

Here are 2 snippets useful for pandoc markdown files. Here is the content of the custom user snippet `markdown.json` file.

```json
{
	"Fancy YAML Header": {
		"prefix": "fancy head",
		"body": [
			"---",
			"title: \"$1 : $2\"",
			"author: $3",
			"date: $4",
			"header-includes:",
			"    - \\usepackage{fancyhdr}",
			"    - \\pagestyle{fancy}",
			"    - \\fancyhead{}",
			"    - \\fancyhead[LO,LE]{$1}",
			"    - \\fancyhead[RO,RE]{$2}",
			"    - \\fancyfoot{}",
			"    - \\fancyfoot[LO,LE]{$3}",
			"    - \\fancyfoot[RO,RE]{\\thepage}",
			"---",
			"$0"
		],
		"description": "Yaml header for pandoc class notes"
	},
	"Simple YAML Header": {
		"prefix": "head",
		"body": [
			"---",
			"title: \"$1\"",
			"author: $2",
			"date: $3",
			"---",
			"$0"
		],
		"description": "Yaml header for simple pandoc document"
	}
}
```
