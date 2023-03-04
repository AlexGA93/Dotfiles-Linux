# Personal Dotfiles

## Images


## Content
Content Table:

|           Name            |          Description          | Config Path                       |
|---------------------------|-------------------------------|-----------------------------------|
|   [i3](#i3)                  |      Tilling Window Manager   |      ~/.config/i3                 |
|   [Bumblebee-status bar](#bumblebee-status-bar)|      Status Bar               |      ~/.config/bumblebee-status   |
|   [Alacritty](#alacritty)          |      Terminal                 |      ~/.config/alacritty          |
|   [Rofi](#rofi)                |      App Searcher             |      ~/.config/rofi               |
|   [Thunar](#file-manager---thunar)              |      File Manager             |      ~/.config/thunar             |
|   [LxAppearance](#system-theme-manager---lxappearance)        |      Theme Manager            |                                   |
|   [Fonts](#fonts---nerd-fonts)               |      JetBrainsMono Nerd Fonts |                                   |
|   [Theme](#theme)               |      Global Arco Linux Theme  |                                   |

## I3
Installation Path
```
sudo pacman -S i3
```
Check if i3 has created the main directory with the order **whereis package_name**.
If the package is not in **/.config** folder then move it here.
```
sudo mv actual_folder_path ~/.config
```
## Bumblebee-Status Bar
- Installation.
    ```
    cd ~/Downloads
    git clone https://github.com/tobi-wan-kenobi/bumblebee-status.git
    cp -a bumblebee-status ~/.config
    ```
- Configuration.
    We must add in our i3 folder the following code to generate our status bar.
    ```
    bar {

        # BUMBLEBEE-STATUS BAR
        status_command ~/.config/bumblebee-status/bumblebee-status \
        -m arch_update spacer brightness spacer datetime spacer disk spacer xrandr spacer memory spacer pasource spacer pasink spacer spotify  \
        -t iceberg-rainbow \
        -p cpu.warning:85% \
        -p cpu.critical:90% \
        -p cpu.percpu: true \
    ...

    }
    ```
## Alacritty
Move folder into **~/.config**.

## Rofi
- Installation
    ```
    sudo pacman -S rofi
    ```
- Configuration 
    We will bind a keyboard shortcut in our i3 config file:
    ```
    # start rofi
    bindsym $mod+d exec --no-startup-id "rofi -show-icons -font 'JetBrainsMonoNL Nerd Font Mono 13' -theme ~/.config/rofi/themes/rounded-red-dark.rasi -show drun"

    # rofi theme selector
    bindsym control+mod1+r exec --no-startup-id rofi-theme-selector

    ```
    We can see all the rofi themes at the folder **~/.config/rofi/themes**.

## File Manager - Thunar
- Installation
    ```
    sudo pacman -S thunar
    ```
- Configuration
    ```
    # File Manager
    bindsym $mod+F2 exec --no-startup-id thunar;focus
    ```

## System Theme Manager - Lxappearance
- Installation
    ```
    sudo pacman -S lxappearance
    ```
## Fonts - Nerd Fonts
Download a favorite font from the [official site](https://www.nerdfonts.com/) and install it with **laxappearance**.

## Theme
Arco Linux has a tool name **Arch Linux Tweak Tool** where we can select the theme and color combination that user wants.

