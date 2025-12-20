# Requirements
```
i3-wm
rofi
feh
picom
alacritty
clipcat
i3-restore (at ~/i3-restore)
```
---
# Set up
## 0. Preinstallation
Install the requirements listed above; for example, on Debian-based system: `sudo apt install i3-wm rofi feh picom alacritty clipcat`.

For i3-restore, run `git clone https://github.com/jdholtz/i3-restore.git ~/i3-restore` and add `~/i3-restore` to PATH

## 1. Installation
Copy the configs in directory `i3`, `i3status`, `picom` and `rofi` to their expected config path.
* For example `~/.config/i3/`, `~/.config/i3status/`, `~/.config/picom/picom/` and `~/.config/rofi/`

Copy scripts in `scripts` to `~/script`

## 2. Configure
You can customize the start menu by adding `.start_list` to `~/scripts`.

You add 1 entry per line; Its name and its command separated by `|`

Example:
```
Firefox | firefox
Neovim | alacritty -e nvim
```
The Start Menu will show both the name and the command
---
# Keybind (modified from default i3 keybinds)
| keybind | usage |
| --- | --- |
| `super` | Show start menu |
| `super+a` | Show app menu |
| `super+r` | Show run menu |
| `super+v` | Show clipboard |
| `super+tab` | Show windows |
| `super+delete` | Start firefox |
| `super+shift+h` | Hide current windows |
| `super+shift+s` | Show recently hidden windows |
| `super+shift+e` | Show power menu |
| `super+shift+f` | Start file explorer |
| `super+control+r` | Resize window, `control+r` to exit |
