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

https://github.com/basecamp/omarchy/issues/73#issuecomment-3052709335

## Remove Apps

```
yay -Rns zoom
yay -Rns signal-desktop
```

## Edit Hyprland Config

```
code ~/.config/hypr
```

- Edit `monitors.conf` to set the resolution and refresh rate.
- Edit `hyprland.conf` to change the `GDK_SCALE` to 1 and change `kb_layout` to gb. Also enable `natural_scroll` when on a laptop.

