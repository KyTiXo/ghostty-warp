# Ghostty Warp — Modern Terminal Configuration

A modern terminal setup using **Ghostty** with curated open-source tools. Originally inspired by Warp Terminal's productivity features, rebuilt fully open source for **Linux** (CachyOS/Arch + Hyprland).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform: Linux](https://img.shields.io/badge/Platform-Linux-blue.svg)]()
[![WM: Hyprland](https://img.shields.io/badge/WM-Hyprland-cyan.svg)]()

## Why This Exists

Get Warp's productivity features without proprietary software, telemetry, cloud dependency, or subscription fees.

## Features

### Core Productivity

- **Auto-suggestions** (zsh-autosuggestions) — Fish-like command suggestions
- **Syntax highlighting** (zsh-syntax-highlighting) — Real-time validation
- **Fuzzy search** (fzf) — Fast history and file search
- **Smart navigation** (zoxide) — Jump to directories instantly
- **Beautiful prompt** (starship) — Git integration & modern styling
- **Session management** (tmux) — Splits, panes, persistent sessions

### Customization

- **4 Presets**: Cyberpunk Dev, Minimal Focus, Cozy Coding, Professional Elegant
- **5 Themes**: Tokyo Night, Catppuccin Mocha, Dracula, Nord, Gruvbox
- **5 Fonts**: JetBrains Mono, Fira Code, Cascadia Code, Iosevka, Monaspace Neon

## Quick Start

```bash
# Clone
git clone https://github.com/Arakiss/ghostty-warp.git
cd ghostty-warp

# Copy to ghostty config
cp -r themes presets fonts tmux gconfig ~/.config/ghostty/
chmod +x ~/.config/ghostty/gconfig

# Add to PATH
ln -sf ~/.config/ghostty/gconfig ~/.local/bin/gconfig
```

**Prerequisites**: Linux, [Ghostty](https://ghostty.org), Nerd Fonts (JetBrainsMono recommended)

## Usage

### Switch Presets (full theme + font combos)

```bash
gconfig cyber       # Tokyo Night + Fira Code (futuristic)
gconfig minimal     # Nord + Iosevka (distraction-free)
gconfig cozy        # Gruvbox + JetBrains Mono (comfortable)
gconfig pro         # Dracula + Cascadia Code (professional)
```

### Switch Themes

```bash
gconfig theme tokyo-night
gconfig theme catppuccin-mocha
gconfig theme dracula
gconfig theme nord
gconfig theme gruvbox
```

### Switch Fonts

```bash
gconfig font jetbrains-mono
gconfig font fira-code
gconfig font cascadia-code
gconfig font iosevka
gconfig font monaspace-neon
```

### Other Commands

```bash
gconfig status      # Show current configuration
gconfig reset       # Restore default config
gconfig             # Show help
```

### Keyboard Shortcuts (Linux)

**Clipboard**

- `Ctrl+Shift+C` — Copy
- `Ctrl+Shift+V` — Paste

**Tabs**

- `Ctrl+Shift+T` — New tab
- `Ctrl+Shift+W` — Close tab
- `Ctrl+Shift+1-9` — Jump to tab
- `Ctrl+Tab` / `Ctrl+Shift+Tab` — Cycle tabs

**Splits**

- `Ctrl+Shift+D` — Vertical split
- `Ctrl+Shift+O` — Horizontal split
- `Ctrl+Shift+Z` — Toggle zoom
- `Ctrl+Shift+Arrow` — Navigate splits

**Font Size**

- `Ctrl++` / `Ctrl+-` — Increase/Decrease
- `Ctrl+0` — Reset

## tmux Integration

A matching tmux config with Tokyo Night colors and Wayland clipboard support:

```bash
ln -sf ~/.config/ghostty/tmux/tmux.conf ~/.tmux.conf
```

Features: vim keybindings, `|` and `-` for splits, mouse support, `wl-copy` integration.

## Hyprland Notes

The config includes `async-backend = epoll` to fix rendering performance issues with Ghostty on Hyprland. See [ghostty#3224](https://github.com/ghostty-org/ghostty/discussions/3224).

## Comparison with Warp

| Feature             | Warp         | Ghostty Warp     |
| ------------------- | ------------ | ---------------- |
| Auto-suggestions    | Yes          | Yes (zsh plugin) |
| Syntax highlighting | Yes          | Yes (zsh plugin) |
| Fuzzy history       | Cloud        | Local (fzf)      |
| Session management  | Yes          | Yes (tmux)       |
| Open source         | No           | Yes              |
| Offline             | No           | Yes              |
| Telemetry           | Yes          | None             |
| Cost                | Subscription | Free             |

## Tech Stack

- [Ghostty](https://ghostty.org) — Terminal emulator
- [Starship](https://starship.rs) — Prompt
- [fzf](https://github.com/junegunn/fzf) — Fuzzy finder
- [zoxide](https://github.com/ajeetdsouza/zoxide) — Smart cd
- [tmux](https://github.com/tmux/tmux) — Terminal multiplexer
- [Nerd Fonts](https://www.nerdfonts.com) — Patched fonts with icons

## License

MIT — Use however you want.

---

**Built for productivity.** Open source. Privacy-first. Linux-native.
