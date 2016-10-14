GNOME Shell Extension Installer
===============================

[![asciicast](https://asciinema.org/a/2kkzsbsd9k4x9xtn028q7w3dn.png)](https://asciinema.org/a/2kkzsbsd9k4x9xtn028q7w3dn)

A bash script to install and search extensions from [extensions.gnome.org](https://extensions.gnome.org/).

By default extensions are installed in `$HOME/.local/share/gnome-shell/extensions/`,
except if the script is run with super user permission
(then, it will be installed in `/usr/share/gnome-shell/extensions/`).

## Help

```
Usage: gnome-shell-extension-installer EXTENSION_ID [ EXTENSION_ID... ] [ GNOME_VERSION ] [ OPTIONS ]
 
Options: 
  -s or --search  [ STRING ]       Interactive search.
  --yes                            Skip all prompts.
  --no-install                     Saves the extension(s) in the current directory.
  --restart-shell                  Restart GNOME Shell after the extensions are installed.
  -h or --help                     Print this message.
 
Usage examples: 
  # Install "Small Panel Icon" for GNOME Shell 3.12 answering yes to all questions: 
  gnome-shell-extension-installer 861 3.12 --yes
 
  # Search for extensions matching "User Themes": 
  gnome-shell-extension-installer -s "User Themes"
```

## Installation

### Manual installation

Dependencies:

- `bash`
- `curl`
- `glib2`
- `gnome-shell`
- `less` (optional)

```
$ wget -O gnome-shell-extension-installer "https://github.com/brunelli/gnome-shell-extension-installer/raw/master/gnome-shell-extension-installer"
$ chmod +x gnome-shell-extension-installer
$ mv gnome-shell-extension-installer /usr/bin/
```

### AUR (Arch Linux)

Available in the AUR as [gnome-shell-extension-installer](https://aur.archlinux.org/packages/gnome-shell-extension-installer).
