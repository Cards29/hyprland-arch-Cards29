## My Hyprland Dotfiles Collection

This repo contains all my configurations for a Hyprland-based setup in Arch Linux.


## 🛠️ Prerequisites

Before you dive in, make sure you have the following packages installed on your Arch Linux system:

```bash
sudo pacman -S \
  hyprland \
  waybar \
  kitty \
  rofi \
  swww \
  swayosd
```

Also, make a directory named `~/Pictures/wallpapers` and add some wallpapers in there for the swww script to work.

```bash
mkdir -p ~/Pictures/wallpapers
```


## 📦 Using GNU Stow

The repo is structured for your dotfiles to be managed with [GNU Stow](https://www.gnu.org/software/stow/). If you don't know what GNU Stow is, it's basically an easy way to symlink your configs into `~/.config/` effortlessly.


To download GNU Stow:
```bash
sudo pacman -S stow
```


## 📥 Cloning the Repo

It is **very important** to clone this repository directly into your **home directory** to ensure all the stow commands given below work correctly.

```bash
cd ~
git clone https://github.com/Cards29/hyprland-arch-Cards29.git
cd "hyprland-arch-Cards29"
```



## 🚀 Stow Commands

Once you’ve cloned this repo, cd into it and run Stow for the components you want:

```bash
stow hyprland
stow waybar
stow kitty
```

For **Rofi**, please follow the  [adi1090x/rofi](https://github.com/adi1090x/rofi) repository.


## 🌄 Changing Wallpapers with Swww

Use the `swww_random_wallpaper.sh` script in the **Scripts/** folder. Add it to your Hyprland key bindings to cycle wallpapers on the fly:

```ini
# Example in your Hyprland keybinds (e.g., hyprland.conf)
bind = SUPER, w, exec, $HOME/hyprland-arch-Cards29/Scripts/swww_random_wallpaper.sh
```

Now you can hit **Super + W** to refresh your background instantly.

---

Thanks for visiting!
