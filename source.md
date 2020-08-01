### Build and install themes from source

Yaru-macOS is fork of [Yaru](https://github.com/ubuntu/yaru)

This installation method is to try out the theme while developing it. If you're not a developer, follow the instructions in the [README.md](./README.md).

### Prerequisite:
```bash
sudo apt install libgtk-3-dev git meson 
```
### Prerequisite for Icon-theme modification (Optional):
```bash
# Additionally installs packages needed to work on the icon theme
sudo apt install libgtk-3-dev git meson sassc inkscape optipng ruby
```

### Install:

```bash
git clone https://github.com/Muqtxdir/yaru-macos.git

cd yaru-macos

# Initialize build system (only required once per repo)
meson build

cd build

# Build and install
sudo ninja install
```

### Applying Theme manually:

Selecting the GTK theme via:

```bash
# set the icon theme as Yaru-macOS
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-macOS"
```

```bash
# set the icon theme as Yaru-macOS-dark
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-macOS-dark"
```

```bash
# set the icon theme as Yaru-macOS-light
gsettings set org.gnome.desktop.interface gtk-theme "Yaru-macOS-light"
```
The Yaru-macOS-theme files go into `/usr/local/share/themes/Yaru-macOS`.

The Yaru-macOS-dark-theme files go into `/usr/local/share/themes/Yaru-macOS-dark`.

The Yaru-macOS-light-theme files go into `/usr/local/share/themes/Yaru-macOS-light`.

### Uninstall:

To uninstall all Yaru-macOS, simply run the following.

```bash
cd yaru-macOS

cd build

sudo ninja uninstall
```

Once uninstalled you can reset your GTK and icon theme to the default setting by running the following.

```bash
# reset gtk theme to default
gsettings reset org.gnome.desktop.interface gtk-theme
```
