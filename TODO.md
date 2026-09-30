# TODO

## Fit the layout to my hands

Tune `ergogen/magic34.yaml` (column stagger, splay, thumb cluster) from real
hand measurements instead of the current defaults (8 mm stagger, ±4° splay).

1. Measure hands, either:
   - Cosmos hand scan (`ryanis.cool/cosmos`) on the iPad camera, scanned a
     few times to check consistency, or
   - a single-page iPad touch tool: rest fingers on the screen, then curl and
     extend each one; it records fingertip positions in mm.
2. Update stagger and splay only, regenerate, print the outline 1:1 with
   keycaps drawn, and test by typing on paper.
3. Then adjust the thumb cluster and MCU/battery placement.
4. Re-route the PCB in KiCad before ordering.

## Maybe: USB dongle

Add a `magic34_dongle` shield (no keys, central for 2 peripherals) plus a
left-as-peripheral build in `build.yaml`, keeping the current builds as a
fallback. Hardware: nice!nano v2 or a cheap SuperMini nRF52840 clone, which
is fine here because the dongle runs on USB power.
