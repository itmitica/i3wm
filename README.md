# i3wm
rice

## keyboard

### layout / language

```shell
setxkbmap ro -variant std
setxkbmap us
```

### display
https://github.com/porras/i3-keyboard-layout


## config

```shell
# cp /etc/i3/config ~/.config/i3/config
...
workspace_layout tabbed
...
```

```shell
# cp /etc/i3status.conf ~/.config/i3config/config
...
# order += "ipv6"
order += "wireless _first_"
order += "ethernet _first_"
order += "battery all"
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
