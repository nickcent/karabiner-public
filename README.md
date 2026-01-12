# Karabiner-Elements Multi-Layer Configuration

Advanced multi-layer keyboard system for macOS using Karabiner-Elements.

## Profiles

| Profile | Purpose |
|---------|---------|
| **default** | Primary daily driver |
| **cheapino** | Split keyboard layout |
| **Workshop** | Development/testing |
| **Disabled** | Minimal rules |

Switch profiles with **F-Layer**: `F+1` = Default, `F+2` = Cheapino, `F+3` = Workshop, `F+4` = Disabled

---

## Layer System

Hold-to-activate layers where holding specific keys unlocks different functionality:

| Layer | Trigger | Purpose |
|-------|---------|---------|
| **Q-Launcher** | Hold Q | Application launching via Raycast |
| **W-Layer** | Hold W | Window management (Raycast) |
| **F-Layer** | Hold F | Vim-style navigation + profile switching |
| **G-Layer** | Hold G | Command navigation (optimized for Logseq) |
| **T-Layer** | Hold T | Timestamps + tab navigation + Comet controls |
| **M-Layer** | Hold M | Mouse control (great for Chrome/Comet browser) |
| **R-Layer** | Hold R | Deletion operations |
| **V-Layer** | Hold V | Virtual numpad |
| **S-Layer** | Hold S | Punctuation symbols |
| **D-Layer** | Hold D | Arithmetic symbols |
| **Space-Layer** | Hold Space | Brackets and delimiters |

---

## Q-Launcher (Application Hotkeys)

Hold `Q` + key to launch apps via Raycast hotkeys:

### Core Apps
| Shortcut | Application |
|----------|-------------|
| **Q+W** | Warp |
| **Q+E** | Karabiner-EventViewer |
| **Q+S** | Signal |
| **Q+D** | DeepAgent |
| **Q+F** | Finder |
| **Q+G** | Ghostty |
| **Q+H** | LM Studio |
| **Q+J** | Jan |
| **Q+K** | Karabiner-Elements |
| **Q+L** | Logseq |

### Productivity & Dev
| Shortcut | Application |
|----------|-------------|
| **Q+R** | Raindrop.io |
| **Q+T** | Traktor |
| **Q+U** | DevUtils |
| **Q+Y** | SomaFM |
| **Q+I** | IINA |
| **Q+O** | Obsidian |
| **Q+P** | Paper |
| **Q+A** | Autodesk Fusion |
| **Q+;** | Sublime Text |
| **Q+Z** | Zed |
| **Q+V** | VS Code |

### AI & Utilities
| Shortcut | Application |
|----------|-------------|
| **Q+C** | Claude |
| **Q+B** | Comet |
| **Q+N** | Notes |
| **Q+M** | Mail |
| **Q+,** | Keyboard Maestro |
| **Q+.** | ProtonVPN |
| **Q+6** | Marked |
| **Q+7** | WhatsApp |
| **Q+8** | Perplexity |
| **Q+9** | Bitwarden |
| **Q+0** | Chrome |

---

## F-Layer (Navigation + Formatting)

Hold `F` for Vim-style movement:

| Shortcut | Action |
|----------|--------|
| **F+H/J/K/L** | Arrow keys (←↓↑→) |
| **F+;** | End of line (Ctrl+E) |
| **F+A** | Start of line (Ctrl+A) |
| **F+U/I** | Page Up/Down |
| **F+Y/O** | Home/End |
| **F+1/2/3/4** | Switch profiles |

---

## G-Layer (Command Navigation)

Hold `G` for command-modified navigation. **Optimized for Logseq** block editing:

| Shortcut | Action | Use Case |
|----------|--------|----------|
| **G+H** | Cmd+Left | Jump to line start / navigate back |
| **G+L** | Cmd+Right | Jump to line end / navigate forward |
| **G+K** | Cmd+Up | Start of document / previous block |
| **G+J** | Cmd+Down | End of document / next block |
| **G+N** | Cmd+Enter | Insert new block below |
| **G+U** | Shift+Down | Select line down |
| **G+I** | Shift+Up | Select line up |

---

## M-Layer (Mouse Control)

Hold `M` for full mouse control without leaving the keyboard. **Excellent for Chrome/Comet browser navigation:**

| Shortcut | Action |
|----------|--------|
| **M+S/D/E/F** | Mouse movement (left/down/up/right) |
| **M+K** | Left click |
| **M+L** | Right click |
| **M+Space** | Middle click |
| **M+I/O** | Scroll down/up |
| **M+,/.** | Scroll left/right |
| **M+B/N** | Browser back/forward |
| **M+C/V** | Previous/Next tab |
| **M+X** | Close tab (Cmd+W) |
| **M+T** | New tab (Cmd+T) |
| **M+R** | Restore closed tab (Cmd+Shift+T) |

---

## W-Layer (Window Management)

Hold `W` for window control via Raycast:

| Shortcut | Action |
|----------|--------|
| **W+H/L** | Snap left/right half |
| **W+K/J** | Snap top/bottom half |
| **W+F** | Fullscreen |
| **W+C** | Center window |
| **W+M** | Maximize |
| **W+N** | Minimize |
| **W+Q** | Close window |
| **W+U/I** | Move to previous/next display |

---

## V-Layer (Numpad)

Hold `V` for numeric input:

```
U I O     →  7 8 9
J K L     →  4 5 6
M , .     →  1 2 3
N         →  0
H         →  . (decimal)
P         →  +
;         →  -
/         →  Enter
```

---

## Space-Layer (Symbols)

Hold `Space` for quick bracket access:

| Shortcut | Output |
|----------|--------|
| **Space+U/I** | `{ }` |
| **Space+J/K** | `( )` |
| **Space+M/,** | `[ ]` |
| **Space+L** | `?` |
| **Space+O** | `!` |
| **Space+.** | `$` |

---

## Additional Features

### Caps Lock → Hyper/Escape
- **Hold**: Hyper key (Shift+Cmd+Opt+Ctrl)
- **Tap**: Escape

### Dual-Role Keys
- **A key**: Tap = A, Hold = Command
- **; key**: Tap = ;, Hold = Right Command

### Rotary Knob (if available)
- Default: Word navigation (Opt+←/→)
- With Control: Volume control
- With Shift: Word selection
- With Command: Window resize

---

## Layer Conflict Resolution

Layers use **mutual exclusion** to prevent conflicts:
- F-layer blocks Q, W, V, Space, R layers
- Q-launcher blocks G-layer activation

---

## Installation

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
2. Copy `karabiner.json` to `~/.config/karabiner/`
3. Karabiner auto-reloads on file change
4. Install [Raycast](https://raycast.com/) for app launching/window management

---

## Customization

Edit `karabiner.json` using `jq` for safe JSON manipulation:

```bash
# List all rules
jq '[.profiles[0].complex_modifications.rules[].description]' karabiner.json

# List all profiles
jq '[.profiles[].name]' karabiner.json

# Validate JSON
jq empty karabiner.json
```

---

## Global Parameters

- **Simultaneous threshold:** 25ms
- **To-if-alone timeout:** 200ms
- **Held-down threshold:** 300ms

---

## License

MIT
