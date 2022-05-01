# Binarix
Use this to lock your Linux console. Even TTY switching will be prevented.
# Installation
Update Makefile to change installation prefix.  To install run the following commands:
```bash
make
su -c "make install"
```
To uninstall run:
```bash
su -c "make uninstall"
```

# Screenshot
![Binarix Demonstration](/binarix_screenshot.png?raw=true "Binarix")

# Usage in tmux

Assuming binarix is in your $PATH, placing the following in your ~/.tmux.conf file will bind the shortcut Meta-X to lock tmux.

# Screen lock
```bash
bind-key -n M-x lock-server
set-option -g   lock-after-time 0
set-option -g   lock-server on
set-option -g   lock-command "binarix"
```
