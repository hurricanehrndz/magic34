# Magic34

Custom 34 key keyboard that feels like magic!

![magic34 PCB][magic34pcb]

## Design

More info coming soon!

## Firmware

CI builds everything in `build.yaml`. Flash `settings_reset` on every board
before switching between these setups:

- Without a dongle: `magic34_left` (central) and `magic34_right`.
- With a USB dongle: `magic34_dongle`, `magic34_left_peripheral`, and
  `magic34_right`. The dongle pairs with both halves on its own and shows up
  on the host as a USB keyboard.

The dongle build also works on cheap nice!nano clones that lack the 32 kHz
crystal and DC/DC inductors. The halves run on battery and need DC/DC, so use
genuine nice!nanos for them.

[magic34pcb]: images/magic34.png
