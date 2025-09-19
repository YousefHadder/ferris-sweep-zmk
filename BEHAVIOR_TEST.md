# Tap-Hold-Repeat Behavior Implementation

## What was implemented

Custom behaviors `mt_repeat` and `lt_repeat` that enable tap-hold-repeat functionality using ZMK's native hold-tap behavior with optimized timing settings.

## How it works

The implementation uses ZMK's `tap-preferred` flavor with specific timing parameters:
- `flavor = "tap-preferred"`: Prioritizes tap actions over hold actions
- `quick-tap-ms = <200>`: Allows quick successive taps, enabling repeat when held after tap
- `tapping-term-ms = <200>`: Time window to distinguish between tap and hold
- `require-prior-idle-ms = <100>`: Prevents accidental activation during fast typing

## Behavior Modes

Each key now supports:
1. **Normal tap**: Types the key character
2. **Normal hold**: Activates modifier or layer 
3. **Tap + Hold**: Types the key once, then repeats it when held (native ZMK behavior)

## Keys with tap-hold-repeat

### Homerow Mods (Layer 0)
- Q, W, E, R: Left side with ALT, SHIFT, CTRL, GUI
- U, I, O, P: Right side with GUI, CTRL, SHIFT, ALT

### Layer switches  
- Z: Layer 1 tap/hold, 'Z' repeat on tap-hold
- Backspace: Layer 2 tap/hold, Backspace repeat on tap-hold
- Space: Layer 3 tap/hold, Space repeat on tap-hold

### Number keys with mods (Layer 2)
- 2, 3, 4: With LEFT_SHIFT, LEFT_CTRL, LEFT_GUI  
- 7, 8, 9: With RIGHT_GUI, RIGHT_CTRL, RIGHT_SHIFT

## Testing behavior

To test on actual hardware:
1. **Normal tap**: Tap Q → types 'q'
2. **Hold for mod**: Hold Q → activates Left Alt
3. **Tap-then-hold**: Tap Q quickly then hold → types 'q' then repeats 'qqqqq...'

The tap-hold-repeat functionality uses ZMK's built-in key repeat mechanism, making it reliable and efficient.