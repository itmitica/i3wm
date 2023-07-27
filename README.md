# i3wm
rice

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
