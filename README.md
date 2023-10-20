# pikocore


pikocore is a hackable, open-source, lo-fi music mangler based on the Raspberry Pi Pico.

![img](https://user-images.githubusercontent.com/6550035/276962341-4c0065e4-f0cf-4315-9de2-e26aa2ebe1e7.jpg)

read more here: https://pikocore.com


## usage

### prerequisites

First install Go and then install pre-reqs:

```
make prereqs
```

This will install `clang-format`, `cmake`, the pico toolchain, `gcc`, `python`, and other useful packages.

### create audio

You can use the default audio by just running

```
make audio
```

The audio is taken from the `audio2h/demo` folder. You can edit the `Makefile` to choose a different folder.

### build

To build just run

```
make
```

If you are using a 2mb pico, then you should do `make build2` (the default is 16mb).

Then upload the `build/pikocore.uf2` to your pico.

If you want to turn off the LED, change `#define WS2812_ENABLED 1` to `#define WS2812_ENABLED 0` in the `main.cpp` file.

## dev

You can open a minicom terminal by running `make debug` after switching on `DEBUG_X` flags in `main.cpp`.

Easing functions generated with: https://editor.p5js.org/schollz/sketches/l5F_ZWjZM

