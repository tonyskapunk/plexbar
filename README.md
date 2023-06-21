# plexbar
A PlexAmp plugin for waybar

## Demo

[![Demo of plexbar in waybar](https://github.com/tonyskapunk/plexbar/assets/116447/5eb65acc-a4c4-4d2f-addf-328858a5ab1c)](https://github.com/tonyskapunk/plexbar/assets/116447/bbf16b44-3306-4b81-bf67-94441751a1a9)

## Example

Place the plexbar script under `~/.config/waybar/custom/plexbar/plexbar`

And here an example on how to configure in waybar

`~/.config/waybar/config`

```json

    "modules-right": [
        "custom/plexbar",
        ...
...
      "custom/plexbar": {
        "format": "{} ♪",
        "max-length": 60,
        "interval": 30,
        "return-type": "json",
        "exec": "~/.config/waybar/custom/plexbar/plexbar",
        "signal": 5,
        "smooth-scrolling-threshold": 1.0,
        "exec-if": "pgrep plexamp"
    },  
```

`~/.config/waybar/style.css`

```JavaScript
@define-color comment #6272a4;
@define-color current #44475a;
@define-color light #f8f8f2;
@define-color warning #282A36;

#custom-plexbar,
#custom-plexbar-play-pause,
#custom-plexbar-prev,
#custom-plexbar-next,
#custom-plexbar-quit {
    color: @light;
    padding: 0px 6px 0px 6px;
    font-size: 14px;
    font-style: italic;
}

#custom-plexbar {
    margin: 0px 8px 0px 1px;
}

#custom-plexbar.playing {
    color: @comment;
}

#custom-plexbar.paused {
    color: @current;
}

#custom-plexbar.stopped {
    color: @warning;
}

#custom-plexbar-prev {
    margin: 0px 0px 0px 1px;
}

#custom-plexbar-play-pause {
    margin: 0px 0px 0px 1px;
}

#custom-plexbar-next {
    margin: 0px 0px 0px 1px;
}

#custom-plexbar-quit {
    margin: 0px 0px 0px 1px;
}
```

