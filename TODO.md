# TODO

## Fit the layout to my hands

Tune `ergogen/magic34.yaml` (column stagger, splay, thumb cluster) from real
hand measurements instead of the current defaults (8 mm stagger, ±4° splay).

1. Measure hands, trying these in order:
   - Ergopad (`pashutk.com/ergopad`) on the iPad: tap each finger through
     the three rows. It's unfinished and has no export, so give it five
     minutes and move on if it can't give stagger and splay in mm.
   - Cosmos hand scan (`ryanis.cool/cosmos`) on the iPad camera, scanned a
     few times to check consistency.
   - Last resort: build a single-page iPad touch tool that records
     fingertip positions in mm.
2. Update stagger and splay only, regenerate, print the outline 1:1 with
   keycaps drawn, and test by typing on paper.
3. Then adjust the thumb cluster and MCU/battery placement.
4. Re-route the PCB in KiCad before ordering.

## Go to 36 keys

Each half direct-wires 17 of the 18 Pro Micro pins, so a third thumb key fits
on the free pin `P16` (confirm it on the nice!nano pinout first). Add a column
to the `thumbfan` zone, add one thumb binding per side in the keymap, and
consider giving Shift its own thumb key. Do this in the same PCB revision as
the hand-fit changes, and add mounting holes to that revision.

## 3D-printed case

Do this last: the hand-fit and 36-key changes both move the outline. Add a
`cases:` section to the ergogen file that extrudes `cutout` into a tray with a
2-3 mm wall, then export JSCAD and convert it to STL. Plan on 1-3 test prints
for the MCU, battery, and USB clearance. For printing, look for a used printer
on Marketplace.
