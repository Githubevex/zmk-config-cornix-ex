# ZMK Config for Cornix TB (Trackball)

This is a ZMK firmware configuration for the Cornix split keyboard with integrated trackball support.

## Hardware

- **Left Half**: Cornix Left (Central) - Main controller
- **Right Half**: Cornix Right (Peripheral) - Right keyboard half
- **Trackball**: Separate trackball peripheral with PAW3222 sensor

## Features

- Auto-mouse layer - Activates when trackball moves
- 5 layers: Default, Function, Num, Scroll, Mouse
- Bluetooth split keyboard (supports 3 devices)
- Japanese keyboard layout support
- Prospector status advertisement for real-time visualization
- RGB LED indicators

## Building Firmware

Firmware is automatically built via GitHub Actions when you push changes.

Download the latest firmware from the [Actions tab](../../actions).

## Keymap Editor

Edit your keymap visually using [keymap-editor](https://nickcoutsos.github.io/keymap-editor/)

## Flashing

1. Download the `.uf2` files from GitHub Actions artifacts
2. Double-tap the reset button on each device to enter bootloader mode
3. Copy the corresponding `.uf2` file to the device

### Files

- `cornix_left_central.uf2` - Left half (central)
- `cornix_right.uf2` - Right half (peripheral)
- `trackball_peripheral.uf2` - Trackball module
- `reset.uf2` - Settings reset (troubleshooting)

## Configuration

Main configuration files:

- `config/cornix_left.keymap` - Keymap definition
- `config/cornix_left.conf` - Feature configuration
- `config/west.yml` - Dependencies
- `config/build.yaml` - Build targets

## Layers

0. **DEFAULT** - Base QWERTY layer
1. **FUNCTION** - Function keys and symbols
2. **NUM** - Number pad
3. **SCROLL** - Bluetooth controls and scrolling
4. **MOUSE** - Auto-activated on trackball movement

## Trackball

- 180-degree rotation (X and Y inverted)
- Auto-mouse layer timeout: 600ms
- Position 46 (RH2) disabled for trackball placement

## License

MIT
