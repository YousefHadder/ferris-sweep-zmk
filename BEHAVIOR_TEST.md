# Tap-Hold-Repeat Behavior Test

## What was implemented

Custom behaviors `mt_repeat` and `lt_repeat` that enable tap-hold-repeat functionality:

1. **Normal tap**: Functions exactly like standard `&mt` and `&lt` behaviors
2. **Normal hold**: Functions exactly like standard `&mt` and `&lt` behaviors  
3. **Tap + Hold**: NEW - Tap action is sent first, then holding repeats the tap action

## How it works

The implementation uses a nested hold-tap structure:
- Primary behavior (`mt_repeat`/`lt_repeat`) handles mod/layer on hold, tap action on tap
- Helper behavior (`kp_repeat`) handles the key repeat when held after a tap
- Built-in `&key_repeat` provides the actual repeat functionality

## Keys that now have tap-hold-repeat

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
1. **Normal tap**: Tap Q → should type 'q'
2. **Hold for mod**: Hold Q → should activate Left Alt 
3. **Tap-then-hold**: Tap Q quickly then hold → should type 'q' then repeat 'qqqqq...'
4. **Layer switching**: Tap Z → types 'z', Hold Z → activates layer 1, Tap-hold Z → types 'zzzz...'

The timing is controlled by:
- `tapping-term-ms = <200>`: Time to distinguish tap vs hold
- `quick-tap-ms = <175>`: Time for quick consecutive taps
- `kp_repeat` with `tapping-term-ms = <40>`: Very quick transition to repeat mode