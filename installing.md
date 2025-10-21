# Packages to install

```bash
sudo pacman -S xorg i3 stow lsd tmux dmenu flameshot pavucontrol zip unzip ufw xorg-xinit ttf-jetbrains-mono-nerd usbutils timeshift xclip bluez bluez-utils pipewire pipewire-audio pipewire-pulse pipewire-alsa pipewire-jack wireplumber ripgrep zsh-syntax-highlighting
```

Installing Brave browser

```bash
yay -S brave-bin
```

**NB**! Don't forget to enable pipewire

```bash
systemctl --user enable --now pipewire pipewire-pulse wireplumber
```

And don't forget to enable the `ufw` firewall, steps in [README.md](https://github.com/luddekn/dotfileslaptop/blob/main/README.md#firewall)

# Installing development stuff

```bash
# Essentials
sudo pacman -S git github-cli mariadb

# NodeJS
sudo pacman -S nodejs-lts-jod npm

# Dotnet
sudo pacman -S dotnet-sdk aspnet-runtime-9.0
```

# Installing essentials for ThinkPad

```bash
sudo pacman -S intel-ucode mesa libva-intel-driver vulkan-intel xf86-input-libinput acpi acpid
```

Auto-cpufreq switches power modes depending on if we are charging or not

```bash
yay -S auto-cpufreq
```

# Disable bluetooth for saving power

```bash
sudo systemctl disable --now bluetooth.service
sudo auto-cpufreq --bluetooth_boot_off
```

# Disable cpu turbo mode

```bash
echo 1 > /sys/devices/system/cpu/intel_pstate/no_turbo
```
