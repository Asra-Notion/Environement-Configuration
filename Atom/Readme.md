# Atom configuration

## Extensions
List of extensions for atom.

For now, see [this post](https://svens.blog/2016/06/15/my-complete-atom-io-package-list-for-writing-markdown/) for packages

### Themes
* ~~github-atom-light-syntax~~
* ~~atom-visual-studio-code-light-ui~~
* ~~kary-foundation-light~~
* github-atom-light-syntax

- [x] TODO: Fix github-atom-light-syntax theme so it's not depricated.

### Packages
* advanced-open-file
* file-icons
* markdown-deluxe
* markdown-pdf
* markdown-writer
* tool-bar
* tool-bar-main
* tool-bar-markdown-writer
* uglify-html
* ~~flex-tool-bar~~
* ~~linter-markdown~~

Modifications have been made to 2 packages, tool-bar-main and tool-bar-markdown-writer. The files \*.coffee are to replace the files in the package folder located at : `$Home/.atom/packages/<Package Name>`.

## Package configuration
Several packages have some specific configuration. Here are the different settings.

### Markdown preview
* Check the use github.com style.
* Add the folowing css to the `styles.less`.

```css
.markdown-preview.markdown-preview {
  font-family: 'Segoe UI'
}
```

### Markdown deluxe config
* **Font**: Segoe UI (_Windows_), sans-serif (_Mac OS_)
* **Width**: 60em (_45em, default, for 1080p screen._)

### Toolbar Config
* **Icon size**: 16 px

- [ ] Todo, find a way to sync packages across multiple installs.

### UI config
* **Theme**: One Light
* **Font Size**: 13
* **Layout mode**: Compact

### Markdown PDF
* **Margin**: 20mm (_2cm_)
* **Page Format**: Letter

## Keymaps
The `keymap.cson` provides all the custom keymaps to be copied in the `.atom` folder.

## Future extensions
The following extensions could prove useful, further investigation is required before selecting them.

- project-manager
- linter-write-good
- linter
- atom-beautify
