# r-image-viewer

A simple, fast, minimalist image viewer built with C and the raylib library.

## Features

-   View individual images or all images in a directory.
-   Pan, zoom, rotate, and flip images.
-   Toggle between anti-aliasing (bilinear) and nearest-neighbor (point) scaling.
-   Display basic image information.

## Usage

Provide a path to an image file or a directory as a command-line argument.

```bash
./iv path/to/your/image.png
```

or

```bash
./iv path/to/your/directory/
```

## Controls

| Key                  | Action                       |
| -------------------- | ---------------------------- |
| `Right Arrow`        | Next image in directory      |
| `Left Arrow`         | Previous image in directory  |
| `Mouse Wheel`        | Zoom in/out at cursor        |
| `Ctrl` + `+` / `Ctrl` + `-` | Zoom in/out at center        |
| `Mouse Left` (drag)  | Pan image                    |
| `W`, `A`, `S`, `D`   | Pan image                    |
| `Q`, `E`             | Rotate image                 |
| `R`                  | Reset rotation               |
| `H`                  | Flip horizontally            |
| `V`                  | Flip vertically              |
| `F`                  | Reset all view changes     |
| `I`                  | Toggle info display          |
| `Ctrl` + `A`         | Toggle anti-aliasing         |
| `Esc`                | Quit                         |

## Building

You need a C compiler (like `gcc`) and `raylib` installed.

On a Debian-based distro, you can install `raylib` with:
```bash
sudo apt-get install libraylib-dev
```

On an Arch-based distro, you can install `raylib` with:
```bash
sudo pacman -S raylib
```
```
```

Then, compile the program using the following command:
```bash
gcc main.c -o iv -lraylib -lGL -lm -lpthread -ldl -lrt -lX11
# --- If you are on wayland and not X11 you can simply run the build command with out the x11 linker
```
