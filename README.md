# gDE: Gusza's Desktop Environment
An i3-based lightweight desktop environment (Only consumes ~1GiB of ram on idle)

# Features
- Runs on i3 window manager
- Rofi-based Navigation (start menu, app menu, power menu, etc)
- Session restoration (via i3-restore)
- Clipboard (via clipcat)

# Requirements
```
i3-wm
rofi
feh
picom
alacritty
clipcat
dunst
nemo
polybar
firefox
i3-restore (at ~/i3-restore)
```
---

# Set up
## 0. Preinstallation
Install the requirements listed above; for example, on Debian-based system: `sudo apt install i3-wm rofi feh picom alacritty dunst nemo polybar firefox-esr`.

To install i3-restore, run `git clone https://github.com/jdholtz/i3-restore.git ~/i3-restore` and add `~/i3-restore` to PATH

To install clipcat see [its installation instruction](https://github.com/xrelkd/clipcat/blob/develop/docs/INSTALL.md)

## 1. Installation
Copy the configs to their expected config path.
* For example `~/.config/i3/`, `~/.config/i3status/`, `~/.config/clipcat`, `~/.config/picom/` and `~/.config/rofi/`

Copy scripts in `scripts` to **`~/scripts`**

## 2. Configure
You can customize the start menu by adding `.start_list` to `~/scripts`.

You add 1 entry per line; Its name and its command separated by `|`

Example:
```
Firefox | firefox
Neovim | alacritty -e nvim
```
The Start Menu will show both the name and the command

adding an image file named `bg` to `~/bg/bg` will set that image as the wallpaper

---
# Keybinds (modified from default i3 keybinds)
| keybind | usage |
| --- | --- |
| `super` | Show start menu |
| `super+z` (hold) | show bar |
| `super+a` | Show app menu |
| `super+r` | Show run menu |
| `super+v` | Show clipboard |
| `super+tab` | Show windows |
| `super+delete` | Start firefox |
| `super+shift+h` | Hide current window |
| `super+shift+s` | Show recently hidden window |
| `super+shift+e` | Show power menu |
| `super+shift+f` | Start file explorer |

* if these keybind collides with another command in the original i3 configs, that command will be adjusted to use `shift`, `ctrl` or rarely completely removed (vertical tile and horizontal tile command)
