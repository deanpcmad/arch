# Arch Setup

1. Install Arch
2. Install [Omarchy](https://omarchy.org/)

## Other Software

```
# Tools
sudo pacman -S nano htop

# VS Code
yay -S --noconfirm visual-studio-code-bin

# Extras
yay -S firefox ghostty discord

# Allow SMB locations on Nautilus
yay -S gvfs-smb

# Tailscale
curl -fsSL https://tailscale.com/install.sh | sh
```

## Change Default Browser

```
xdg-settings set default-web-browser firefox.desktop
xdg-mime default firefox.desktop x-scheme-handler/http
xdg-mime default firefox.desktop x-scheme-handler/https
```

## Setup Keyring

1Password and VS Code's sync system require this to be setup.

```
# Test that it works and create a default keyring
secret-tool store --label="test" testkey testvalue
secret-tool lookup testkey testvalue
secret-tool clear testkey testvalue
```

## Edit Hyprland Config

```
code ~/.config/hypr
```

### hyprland.conf

- Rename the default browser to Firefox and add a chromium option for webapps

```
$browser = firefox --new-window
$chromium = chromium --new-window --ozone-platform=wayland
$webapp = $chromium --app
```

- Change `GDK_SCALE` to 1 or 2 depending on the display
- Add `env = XDG_CURRENT_DESKTOP,Hyprland:GNOME` below `GDK_SCALE`
- Set `kb_layout` to `gb`
- Enable `natural_scroll` when on a laptop

### monitors.conf

Edit to set the resolution and refresh rate.

```
# For example
monitor = eDP-1, 1920x1080@60.00, auto, 1
```

## Remove Apps

```
yay -Rns zoom
yay -Rns signal-desktop
```