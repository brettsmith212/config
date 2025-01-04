# My Config

- nvim
- yabai
- skhd
- tmux
- vscode configs
- ghostty

## Ubuntu Omakub Notes
- To map caps lock to control
```
gsettings set org.gnome.desktop.input-sources xkb-options "[]"
gsettings set org.gnome.desktop.input-sources xkb-options "['ctrl:nocaps']"
```

- To change super+workspace-number to ctrl+workspace-number
```
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-1 "['<Ctrl>1']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-2 "['<Ctrl>2']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-3 "['<Ctrl>3']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-4 "['<Ctrl>4']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-5 "['<Ctrl>5']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-6 "['<Ctrl>6']"
```
