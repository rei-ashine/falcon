# Testing the Falcon VS Code Theme

This document provides instructions for testing the Falcon color theme in VS Code.

## Development Testing

### 1. Local Extension Testing

1. Open VS Code
2. Navigate to the `vscode/` directory
3. Press `F5` to launch a new Extension Development Host window
4. In the new window, open Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
5. Run `Preferences: Color Theme`
6. Select **Falcon** from the list

### 2. Package and Install Testing

```bash
# From the vscode/ directory
npm install -g vsce
vsce package
```

This creates `falcon-color-theme-2.0.0.vsix`. Install it:

1. Open Command Palette in VS Code
2. Run `Extensions: Install from VSIX...`
3. Select the `.vsix` file
4. Reload VS Code and select the Falcon theme

## Visual Testing

### Test Files

Use the sample files from the `corpus/` directory in the root of the repository to test syntax highlighting:

- `corpus/javascript.js` - JavaScript syntax
- `corpus/python.py` - Python syntax
- `corpus/ruby.rb` - Ruby syntax
- `corpus/go.go` - Go syntax
- `corpus/c.c` - C syntax
- `corpus/cpp.cpp` - C++ syntax
- `corpus/css.css` - CSS syntax
- `corpus/html.html` - HTML syntax
- `corpus/markdown.md` - Markdown syntax
- `corpus/yaml.yml` - YAML syntax

### Color Verification

Verify these key colors are displaying correctly:

| Element | Expected Color | Hex Code |
|---------|---------------|----------|
| Background | Deep dark blue | `#020221` |
| Foreground | Light gray | `#B4B4B9` |
| Keywords (if, class, function) | Orange | `#FF761A` |
| Strings | Yellow | `#FFC552` |
| Comments | Mid gray italic | `#787882` |
| Numbers | Orange | `#FF761A` |
| Functions | Bright orange | `#FFB07B` |
| Types/Classes | Bright indigo | `#8859FF` |
| Variables | Blue gray | `#99A4BC` |

### UI Element Testing

Check these UI elements have proper theming:

- [ ] Editor background and text
- [ ] Sidebar (Explorer, Search, etc.)
- [ ] Activity bar (left side icons)
- [ ] Status bar (bottom)
- [ ] Tabs
- [ ] Command palette
- [ ] Settings UI
- [ ] Terminal colors
- [ ] Search highlighting
- [ ] Selection highlighting
- [ ] Error/warning underlines

## Sample Code for Testing

### JavaScript Example
```javascript
// Test JavaScript syntax highlighting
import React, { useState } from 'react';

const App = () => {
  const [count, setCount] = useState(0);
  
  // This is a comment
  const handleClick = () => {
    setCount(count + 1);
  };
  
  return (
    <div className="app">
      <h1>Count: {count}</h1>
      <button onClick={handleClick}>
        Increment
      </button>
    </div>
  );
};

export default App;
```

### Python Example
```python
# Test Python syntax highlighting  
class Calculator:
    def __init__(self):
        self.result = 0
    
    def add(self, number):
        """Add a number to the result"""
        self.result += number
        return self.result
    
    def multiply(self, number):
        self.result *= number
        return self.result

# Usage
calc = Calculator()
print(f"Result: {calc.add(5)}")
print(f"Result: {calc.multiply(3)}")
```

### CSS Example
```css
/* Test CSS syntax highlighting */
.container {
  background-color: #020221;
  color: #B4B4B9;
  font-family: 'Monaco', monospace;
  padding: 20px;
  margin: 0 auto;
  max-width: 800px;
}

.button {
  background: linear-gradient(45deg, #FF761A, #FFB07B);
  border: none;
  border-radius: 4px;
  color: white;
  padding: 10px 20px;
  transition: all 0.3s ease;
}

.button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(255, 118, 26, 0.3);
}
```

## Automated Testing

### Extension Testing Commands

From the `vscode/` directory:

```bash
# Install dependencies
npm install

# Run tests (if test framework is set up)
npm test

# Package extension
vsce package

# Publish to marketplace (requires authentication)
vsce publish
```

### Manual Checklist

- [ ] Extension loads without errors
- [ ] Theme appears in theme selection list
- [ ] All syntax highlighting colors are correct
- [ ] UI elements are properly themed
- [ ] Terminal colors work correctly
- [ ] No contrast issues (readable text)
- [ ] Theme works with different file types
- [ ] No performance issues when switching themes

## Troubleshooting

### Common Issues

1. **Theme not appearing**: Ensure `package.json` has correct theme contribution
2. **Colors not loading**: Check theme file JSON syntax
3. **Extension not loading**: Verify VS Code version compatibility
4. **Package fails**: Install `vsce` globally and check file permissions

### Debug Steps

1. Open VS Code Developer Console (`Help > Toggle Developer Tools`)
2. Check for extension loading errors
3. Verify theme file path is correct
4. Test with minimal theme first, then add complexity