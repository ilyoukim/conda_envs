### opengl error with wayland

```sh
## error message
Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome.
Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
```

replace wayland to x11

```bash
#!/bin/sh
if [ -n "$XDG_SESSION_TYPE" ]; then
    if [ "$XDG_SESSION_TYPE" = "wayland" ]; then
        echo "XDG Session set to x11"
        export XDG_SESSION_TYPE='x11'
    fi
fi

python xxx.py
```
