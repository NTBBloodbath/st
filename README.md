# st (suckless terminal)

Just my personal st build.

> **NOTE**: I'm using st HEAD

## Default settings

- `Font size`: 12px
- `Font family`: `JetBrainsMono Nerd Font` and `Iosevka Slab`
- `Colorscheme`: `doom-one`

## Patches

- Alpha (transparency)
- anysize
- anygeometry
- appsync (Improve draw time, animation smoothness and reduce flickering/tearing)
- blinking cursor
- dynamic cursor color
- hide cursor
- boxdraw
- newterm
- clipboard
- delkey
- desktopentry
- scrollback (+ mouse)
- CSI 22 23
- OSC 10 11 12 (2)
- font2
- vertcenter
- ligatures
- fix-glyphs
- [patch_column](https://github.com/nimaipatel/st/blob/master/patches/7672445bab01cb4e861651dc540566ac22e25812.diff) (doesn't cut text while resizing)
- title parsing fix
- w3m
- xclearwin

> **NOTE**: ligatures needs `libharfbuzz-dev` to work!

## Keybinds

### Keyboard

| Action             | Key combo                                                  |
| ------------------ | ---------------------------------------------------------- |
| Copy               | `Control` + `Shift` + `C`                                  |
| Paste              | `Control` + `Shift` + `V`                                  |
| Zoom in            | `Alt` + `Arrow Up` / `Contrl` + `Shift` + (`k` / `Arrow Up`)   |
| Zoom out           | `Alt` + `Arrow Down` / `Control` + `Shift` + (`j` / `Arrow Down`) |
| Zoom reset         | (`Alt` / `Control` + `Shift`) + `Backspace`                            |
| Scroll up          | `Alt` + (`k` / `Arrow Up` / `Page Up`)                     |
| Scroll down        | `Alt` + (`j` / `Arrow Down` / `Page Down`)                 |
| Inc. transparency  | `Alt` + `a`                                                |
| Dec. transparency  | `Alt` + `s`                                                |
| Reset transparency | `Alt` + `d`                                                |
| Open new terminal  | `Control` + `Shift` + `Return`                               |

### Mouse

| Action      | Modifier          |
| ----------- | ----------------- |
| Slow scroll | `Alt` + `wheel`   |
| Fast scroll | `Shift` + `wheel` |
| Select      | `Right click`     |
| Paste       | `Middle button`   |

> **NOTE**: You can also scroll by just using the `wheel` without using
> the `Alt` key.

## Dynamic colorscheme

Because of the `OSC 10 11 12 (2)` patch, it's possible to use a tool like
[theme.sh](https://github.com/lemnos/theme.sh) for changing the colorscheme on the fly.

### Known issues

Nothing here but chickens ...

## Installation

```sh
sudo make clean install
```

### Required packages

- `GNU Make`
- `fontconfig`
- `harfbuzz`
- `libX11`
- `libXft-bgra` (for displaying emojis)
