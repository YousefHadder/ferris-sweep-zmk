# Ferris Sweep ZMK Configuration

This repository contains a custom ZMK configuration for the Ferris Sweep 34-key split keyboard. The keymap features four layers with home row modifiers, optimized for programming and daily use.

## Features

- 🏠 Home row modifiers on base layer
- 🔢 Dedicated number layer
- 🎵 Media and navigation controls
- 🔣 Symbol layer with Bluetooth controls
- 🔗 Extensive combo mappings for common symbols
- ⚡ Optimized for speed and ergonomics

## Keyboard Layout

The Ferris Sweep uses a 34-key layout arranged as follows:
- 3×5 column-staggered keys per hand
- 2 thumb keys per hand
- Total: 34 keys

## Keymap Layers

### Layer 0: Base (QWERTY with Home Row Mods)

```
┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
│  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │
│ Alt │ Sft │ Ctl │ Gui │     │   │     │ Gui │ Ctl │ Sft │ Alt │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│  A  │  S  │  D  │  F  │  G  │   │  H  │  J  │  K  │  L  │  ;  │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │
│ L1  │     │     │     │     │   │     │     │     │     │     │
└─────┴─────┴─────┼─────┼─────┤   ├─────┼─────┼─────┴─────┴─────┘
                  │ Bsp │ Esc │   │ Ret │ Spc │
                  │ L2  │ All │   │     │ L3  │
                  └─────┴─────┘   └─────┴─────┘
```

### Layer 1: Media & Navigation

```
┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
│ Br- │ Br+ │Prev │Play │Next │   │Vol- │Mute │Vol+ │     │     │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│     │     │     │ Spt │     │   │  ←  │  ↓  │  ↑  │  →  │     │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│     │     │Copy │     │     │   │ D←  │ D↓  │ D↑  │ D→  │     │
└─────┴─────┴─────┼─────┼─────┤   ├─────┼─────┼─────┴─────┴─────┘
                  │ Gui │ Spc │   │DRet │DSpc │
                  └─────┴─────┘   └─────┴─────┘
```

### Layer 2: Numbers & Symbols

```
┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
│  1  │  2  │  3  │  4  │  5  │   │  6  │  7  │  8  │  9  │  0  │
│     │ Sft │ Ctl │ Gui │     │   │     │ Gui │ Ctl │ Sft │     │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│  =  │  -  │  '  │C-b  │     │   │     │     │     │     │     │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│ L1  │     │     │     │     │   │     │     │  ,  │  .  │     │
└─────┴─────┴─────┼─────┼─────┤   ├─────┼─────┼─────┴─────┴─────┘
                  │     │ Spc │   │ Ret │RAlt │
                  └─────┴─────┘   └─────┴─────┘
```

### Layer 3: Symbols & Bluetooth

```
┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
│  !  │  @  │  #  │  $  │  %  │   │  ^  │  &  │  *  │  (  │  -  │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│     │     │  {  │  [  │  (  │   │  )  │  ]  │  }  │     │  =  │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│ BT0 │ BT1 │ BT2 │ BT3 │ BT4 │   │     │     │     │     │BTCLR│
└─────┴─────┴─────┼─────┼─────┤   ├─────┼─────┼─────┴─────┴─────┘
                  │     │     │   │     │     │
                  └─────┴─────┘   └─────┴─────┘
```

## Combo Mappings

The keymap includes numerous combos for efficient symbol input:

| Combo Keys | Output | Description |
|------------|--------|-------------|
| Q + W | Tab | Quick tab access |
| O + P | \\ | Backslash |
| Z + X | \` | Grave/backtick |  
| M + , | ' | Single quote |
| Bsp + Spc | Caps Lock | Caps lock toggle |
| A + S | Tmux prefix (Ctrl+B) | Terminal multiplexer |
| R + T | ( | Left parenthesis |
| Y + U | ) | Right parenthesis |
| F + G | [ | Left bracket |
| H + J | ] | Right bracket |
| V + B | { | Left brace |
| N + M | } | Right brace |

## Legend

- **Sft**: Shift
- **Ctl**: Control  
- **Gui**: Super/Windows/Cmd
- **Alt**: Alt/Option
- **All**: Hyper key (Alt+Shift+Gui+Ctrl)
- **L1/L2/L3**: Layer access keys
- **Br-/Br+**: Brightness down/up
- **Vol-/Vol+**: Volume down/up
- **Spt**: Spotlight search (Ctrl+Alt+F)
- **D←/D→**: Desktop left/right (Alt+Ctrl+Left/Right)
- **D↓/D↑**: Desktop down/up (Alt+Ctrl+Down/Up)
- **DRet**: Desktop return (Alt+Ctrl+Enter)
- **DSpc**: Desktop space (Alt+Ctrl+Gui+Left)
- **Copy**: Copy (Alt+Ctrl+C)
- **BTCLR**: Bluetooth clear
- **BT0-4**: Bluetooth profile select

## Build Instructions

This configuration uses the standard ZMK build process:

1. Fork this repository
2. Enable GitHub Actions in your fork
3. Commit changes to trigger the build
4. Download the firmware files from the Actions artifacts
5. Flash the `.uf2` files to your nice!nano controllers

## Hardware

- **MCU**: nice!nano v2 (both halves)
- **Board**: Ferris Sweep PCB
- **Layout**: 34-key split

## Credits

Based on the excellent Ferris Sweep keyboard design and optimized for personal workflow efficiency.