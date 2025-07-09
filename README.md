# Arch Setup

1. Install Arch
2. Install [Omarchy](https://omarchy.org/)

## Other Software

```
# Tools
sudo pacman -S nano htop

# VS Code
sudo pacman -S vscode

# Firefox
yay -S firefox

# Ghostty
yay -S ghostty
```

## Remove Apps

```
yay -Rns zoom
```

## Edit Hyprland Config

```
code ~/.config/hypr
```

- Edit `monitors.conf` to set the resolution and refresh rate.
- Edit `hyprland.conf` to change the `GDK_SCALE` to 1 and change `kb_layout` to gb. Also enable `natural_scroll` when on a laptop.

## Allow SMB locations on Nautilus

```
sudo pacman -S gvfs-smb
```
