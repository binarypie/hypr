# Hyprland Configuration

This is my personal Hyperland configuration that I also use in BinaryOS.

## 🎨 Features

- **Tokyo Night Theme**: Gorgeous color palette with blue/purple gradient borders
- **Vim-like Navigation**: Use `h/j/k/l` for intuitive window management
- **Auto-lock & Idle Management**: Automatic screen dimming, locking, and suspend
- **Smooth Animations**: Carefully tuned bezier curves for fluid transitions
- **OSD Notifications**: Volume and brightness controls with on-screen display
- **Wallpaper Management**: Hyprpaper integration for beautiful backgrounds

## 📦 Dependencies

### Required
- `hyprland` - The Wayland compositor
- `ashell` - Wayland status bar
- `walker` - Application launcher
- `hyprpaper` - Wallpaper daemon
- `hypridle` - Idle management daemon
- `hyprlock` - Screen locker
- `swayosd-server` - On-screen display for volume/brightness

## 🚀 Installation

1. Clone this repository to your Hyprland config directory:
```bash
git clone git@github.com:binarypie/hypr.git ~/.config/hypr
```

2. Install required dependencies (example for Arch Linux):
```bash
yay -S hyprland kitty walker hyprpaper hypridle hyprlock swayosd dolphin playerctl brightnessctl
```

3. Enable the Elephant service (required for Walker):
```bash
systemctl --user enable elephant.service
systemctl --user start elephant.service
```

4. Replace `background.webp` with your preferred wallpaper or update the path in:
   - `hyprlock.conf`
   - `hyprpaper.conf`

5. Reload Hyprland or log out and back in

## ⌨️ Keybindings

### General
| Keybinding | Action |
|------------|--------|
| `SUPER + Q` | Open terminal (Kitty) |
| `SUPER + C` | Close active window |
| `SUPER + E` | Open file manager (Dolphin) |
| `SUPER + R` | Open application launcher (Walker) |
| `SUPER + V` | Toggle floating mode |
| `SUPER + F` | Toggle fullscreen |
| `SUPER + P` | Toggle pseudotile (dwindle) |
| `SUPER + S` | Toggle split (dwindle) |
| `SUPER + SHIFT + L` | Lock screen |

### Window Navigation (Vim-style)
| Keybinding | Action |
|------------|--------|
| `SUPER + H` | Move focus left |
| `SUPER + J` | Move focus down |
| `SUPER + K` | Move focus up |
| `SUPER + L` | Move focus right |

### Window Movement
| Keybinding | Action |
|------------|--------|
| `SUPER + SHIFT + H` | Move window left |
| `SUPER + SHIFT + J` | Move window down |
| `SUPER + SHIFT + K` | Move window up |
| `SUPER + SHIFT + L` | Move window right |

### Window Resizing
| Keybinding | Action |
|------------|--------|
| `SUPER + CTRL + H` | Resize window left (-50px) |
| `SUPER + CTRL + J` | Resize window down (+50px) |
| `SUPER + CTRL + K` | Resize window up (-50px) |
| `SUPER + CTRL + L` | Resize window right (+50px) |

### Workspaces
| Keybinding | Action |
|------------|--------|
| `SUPER + [1-9,0]` | Switch to workspace 1-10 |
| `SUPER + SHIFT + [1-9,0]` | Move window to workspace 1-10 |
| `SUPER + T` | Toggle special workspace (scratchpad) |
| `SUPER + SHIFT + T` | Move window to special workspace |
| `SUPER + Mouse Wheel` | Scroll through workspaces |

### Media Controls
| Keybinding | Action |
|------------|--------|
| `XF86AudioRaiseVolume` | Increase volume |
| `XF86AudioLowerVolume` | Decrease volume |
| `XF86AudioMute` | Toggle mute |
| `XF86AudioMicMute` | Toggle microphone mute |
| `XF86MonBrightnessUp` | Increase brightness |
| `XF86MonBrightnessDown` | Decrease brightness |
| `XF86AudioPlay/Pause` | Play/Pause media |
| `XF86AudioNext` | Next track |
| `XF86AudioPrev` | Previous track |

## 🎨 Tokyo Night Color Palette

- **Background**: `#1a1b26`
- **Foreground**: `#c0caf5`
- **Blue (accent)**: `#7aa2f7`
- **Purple (accent)**: `#bb9af7`
- **Cyan**: `#7dcfff`
- **Green**: `#9ece6a`
- **Red**: `#f7768e`
- **Border inactive**: `#414868`

## 🔒 Idle & Lock Configuration

The configuration includes automatic power management:

- **2.5 minutes**: Screen dims to 10% brightness, keyboard backlight turns off
- **5 minutes**: Screen locks (hyprlock)
- **5.5 minutes**: Display turns off
- **30 minutes**: System suspends

Edit `hypridle.conf` to customize these timeouts.

## 📝 Customization

### Change Wallpaper
Update the wallpaper path in:
- `hyprpaper.conf` (line 5 and 9)
- `hyprlock.conf` (line 14)

### Modify Theme Colors
Edit the color values in `hyprland.conf` under the `general` and `decoration` sections.

### Adjust Animations
Customize animation speeds and curves in the `animations` section of `hyprland.conf`.

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Charles Christolini

## 🙏 Acknowledgments

- [Hyprland](https://hyprland.org/) - Amazing Wayland compositor
- [Tokyo Night](https://github.com/enkia/tokyo-night-vscode-theme) - Beautiful color scheme

