##**My Hyprland Dotfiles Collection**

This repo contains all my configurations for a Hyprland-based setup in Arch Linux.

---

## 🛠️ Prerequisites

Before you dive in, make sure you have the following packages installed on your Arch Linux system:

```bash
sudo pacman -S \
  hyprland \
  waybar \
  kitty \
  rofi-wayland \
  swww
```

---

## 📦 Using GNU Stow

To keep things tidy, I've structured the repo so you can manage your dotfiles with [GNU Stow](https://www.gnu.org/software/stow/). If you don't know what GNU Stow is, it's basically an easy way to symlink your configs into `~/.config/` effortlessly!


To download GNU Stow:
```bash
sudo pacman -S stow
```

---

## 📥 Cloning the Repo

It is **very important** to clone this repository directly into your **home directory** to ensure all the stow commands given below work correctly.

```bash
cd ~
git clone https://github.com/Cards29/arch-hyprland-config.git
cd ""
```

---


## 🚀 Stow Commands

Once you’ve cloned this repo, cd into it and run Stow for the components you want:

```bash
# In your dotfiles root directory:

# Hyprland config
stow hyprland

# Waybar config
stow waybar

# Kitty terminal config
stow kitty
```

For **Rofi**, please follow the  [adi1090x/rofi](https://github.com/adi1090x/rofi) repository for themes and additional setup!

---

## 🌄 Changing Wallpapers with Swww

Use the `swww_random_wallpaper.sh` script in the **Scripts/** folder. Add it to your Hyprland key bindings to cycle wallpapers on the fly:

```ini
# Example in your Hyprland keybinds (e.g., hyprland.conf)
bind = SUPER, w, exec, $HOME/dotfiles/Scripts/swww_random_wallpaper.sh
```

Now you can hit **Super + W** to refresh your background instantly!

---

Thanks for visiting!
