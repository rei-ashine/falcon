# Falcon Theme for Visual Studio Code

A dark, easy on the eyes, fiery color scheme for Visual Studio Code.

![Falcon VS Code Theme](https://raw.githubusercontent.com/fenetikm/falcon/master/support/hero2.png)

## Installation

### Via VS Code Marketplace

1. Open **Extensions** sidebar panel in VS Code. `View → Extensions`
2. Search for `Falcon`
3. Click **Install** to install it
4. Click **Reload** to reload the editor
5. Code > Preferences > Color Theme > **Falcon**

### Via Command Palette

1. Open **Command Palette** with `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
2. Run `ext install falcon-color-theme`
3. Select **Falcon** from the color theme list

### Manual Installation

1. Download the `.vsix` file from the [releases page](https://github.com/fenetikm/falcon/releases)
2. Open **Command Palette** and run `Extensions: Install from VSIX...`
3. Select the downloaded file
4. Reload VS Code
5. Select **Falcon** from the color theme list

### Development Installation

1. Clone this repository
2. Open the `vscode` folder in VS Code
3. Press `F5` to open a new VS Code window with the extension loaded
4. Open **Command Palette** and run `Color Theme`
5. Select **Falcon** from the list

## Building the Extension

From the `vscode` directory:

```bash
# Install vsce (Visual Studio Code Extension manager)
npm install -g vsce

# Package the extension
vsce package

# This creates falcon-color-theme-2.0.0.vsix
```

## Color Palette

The theme uses colors from the main Falcon palette:

- Background: `#020221` - Deep dark blue
- Foreground: `#B4B4B9` - Light gray
- Keywords: `#FF761A` - Orange
- Strings: `#FFC552` - Yellow
- Functions: `#FFB07B` - Bright orange
- Types: `#8859FF` - Bright indigo
- Comments: `#787882` - Mid gray
- Variables: `#99A4BC` - Blue gray

## Screenshots

### JavaScript
![JavaScript](https://raw.githubusercontent.com/fenetikm/falcon/master/support/snaps/js.png)

### Python
![Python](https://raw.githubusercontent.com/fenetikm/falcon/master/support/snaps/python.png)

### Ruby
![Ruby](https://raw.githubusercontent.com/fenetikm/falcon/master/support/snaps/ruby.png)

## Contributing

If you find any issues or have suggestions, please open an issue on the [GitHub repository](https://github.com/fenetikm/falcon/issues).

## License

[MIT License](https://github.com/fenetikm/falcon/blob/master/LICENSE)