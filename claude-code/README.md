# Falcon Theme for Claude Code

This directory contains a Falcon color theme for Claude Code, prepared for when custom theme support is added.

## Current Status

⚠️ **Note**: Claude Code does not currently support custom themes. This theme file is created in anticipation of future support.

As of now, Claude Code:
- Uses built-in themes selectable via the `/config` command
- Does not support custom theme files in JSON, CSS, or other formats
- Relies on terminal theme settings with some overrides

## Theme File

`falcon.json` - A comprehensive theme file following the VS Code theme format, which includes:
- Editor colors (background, foreground, selection, etc.)
- Syntax highlighting for various programming languages
- UI element colors (sidebar, status bar, tabs, etc.)
- Terminal colors (16 ANSI colors)

## How to Use (When Support is Added)

Once Claude Code adds custom theme support:
1. The theme file will likely need to be placed in a specific directory
2. Configuration may be done through `settings.json` or a dedicated theme command
3. Check the Claude Code documentation for the exact process

## Theme Preview

The Falcon theme features:
- **Background**: Deep dark blue (#020221)
- **Foreground**: Light gray (#B4B4B9)
- **Syntax Highlighting**:
  - Keywords: Orange (#FF761A)
  - Strings: Yellow (#FFC552)
  - Functions: Bright orange (#FFB07B)
  - Types: Bright indigo (#8859FF)
  - Comments: Mid gray (#787882)
  - Variables: Blue gray (#99A4BC)

## Contributing

To track progress on custom theme support:
- GitHub Issue: [#1302](https://github.com/anthropics/claude-code/issues/1302)
- Feature requests can be submitted to the Claude Code repository

## Testing

To test the color scheme visually:
1. Use the color values in your terminal emulator
2. Apply similar colors in other editors that support the theme format
3. Reference the main Falcon theme files in this repository