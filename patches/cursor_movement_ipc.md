### This patch let's you subscribe to cursor movement on sway ipc and let's you track whenever your mouse moves

Simple usage:
```bash
swaymsg -t subscribe -m '[ "cursor_movement" ]' | jq
```
