# Karabiner-Elements Multi-Layer Configuration

Advanced multi-layer keyboard system for macOS using Karabiner-Elements.

## Layer System

This configuration implements a **hold-to-activate layer system** where holding specific keys unlocks different functional layers:

| Layer | Trigger | Purpose |
|-------|---------|---------|
| **Q-Launcher** | Hold Q | Application launching |
| **W-Layer** | Hold W | Window management (via Raycast) |
| **F-Layer** | Hold F | Vim-style navigation + text formatting |
| **G-Layer** | Hold G | Command + arrow navigation |
| **T-Layer** | Hold T | Timestamps + tab navigation |
| **M-Layer** | Hold M | Mouse control |
| **R-Layer** | Hold R | Deletion operations |
| **V-Layer** | Hold V | Virtual numpad |
| **Space-Layer** | Hold Space | Brackets and delimiters |

## Key Features

### F-Layer (Navigation)
Hold `F` for Vim-style movement:
- `F+H/J/K/L` → Arrow keys
- `F+;` → End of line (Ctrl+E)
- `F+A` → Start of line (Ctrl+A)
- `F+U/I` → Page Up/Down
- `F+Y/O` → Home/End

### G-Layer (Command Navigation)
Hold `G` for command-modified arrows:
- `G+H/J/K/L` → Cmd+Arrow (line/document navigation)
- `G+N` → Cmd+Enter
- `G+U/I` → Shift+Up/Down (select lines)

### M-Layer (Mouse Control)
Hold `M` for mouse without leaving keyboard:
- `M+S/D/E/F` → Mouse movement
- `M+K/L` → Left/Right click
- `M+I/O` → Scroll down/up
- `M+C/V` → Previous/Next tab

### V-Layer (Numpad)
Hold `V` for numeric input:
```
U I O     →  7 8 9
J K L     →  4 5 6
M , .     →  1 2 3
N         →  0
```

### Space-Layer (Symbols)
Hold `Space` for quick bracket access:
- `Space+U/I` → `{ }`
- `Space+J/K` → `( )`
- `Space+M/,` → `[ ]`

## Layer Conflict Resolution

Layers use **mutual exclusion** to prevent conflicts:
- F-layer blocks Q, W, V, Space, R layers
- Q-launcher blocks G-layer activation

## Installation

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
2. Copy `karabiner.json` to `~/.config/karabiner/`
3. Karabiner auto-reloads on file change

## Customization

Edit `karabiner.json` using `jq` for safe JSON manipulation:

```bash
# List all rules
jq '[.profiles[0].complex_modifications.rules[].description]' karabiner.json

# Validate JSON
jq empty karabiner.json
```

## Global Parameters

- **Simultaneous threshold:** 25ms
- **To-if-alone timeout:** 200ms
- **Held-down threshold:** 300ms

## Requirements

- macOS
- [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
- [Raycast](https://raycast.com/) (optional, for app launching/window management)

## License

MIT
