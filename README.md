# i3wm
slimi3wm

## menu

### rofi

```shell
sudo apt install rofi
rofi-theme-selector
# Arc-Dark
```

## keyboard

### switch layout / language

```shell
setxkbmap ro -variant std
setxkbmap us
```

### display layout / language

#### i3-keyboard-layout

https://github.com/porras/i3-keyboard-layout

```shell
chmod +x ~/Downloads/i3-keyboard-layout
sudo cp ~/Downloads/i3-keyboard-layout /usr/local/bin/
```


## config

### i3

```shell
# cp /etc/i3/config ~/.config/i3/config
...
# Font for window titles. Will also be used by the bar unless a different font
# is used in the bar {} block below.
font pango:JuliaMono Medium 13
...
# start dmenu (a program launcher)
# bindsym $mod+d exec --no-startup-id dmenu_run
# A more modern dmenu replacement is rofi:
# bindcode $mod+40 exec "rofi -modi drun,run -show drun"
bindcode $mod+40 exec "rofi -show combi -combi-modes 'window,drun' -modes combi"
...
# toggle tiling / floating
# bindsym $mod+Shift+space floating toggle

# change focus between tiling / floating windows
# bindsym $mod+space focus mode_toggle
...
bar {
#   status_command i3status
  status_command i3status | i3-keyboard-layout i3status
}

bindsym $mod+space exec i3-keyboard-layout cycle us "ro std"

workspace_layout tabbed
...
```

### i3status

```shell
# cp /etc/i3status.conf ~/.config/i3config/config
...
# order += "ipv6"
# order += "wireless _first_"
# order += "ethernet _first_"
# order += "battery all"
# order += "disk /"
# order += "load"
# order += "memory"
order += "tztime local"
...
tztime local {
        format = "%Y-%m-%d %H:%M"
}
...
```
