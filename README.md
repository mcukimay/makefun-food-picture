# The Pepperoni Slice — make.fun food-picture-01

One slice of Neapolitan-style pepperoni pizza, shot from directly above on a
dark walnut table in warm evening light. Golden, leopard-spotted crust; molten
mozzarella in deep amber and pale cream; six glossy pepperoni cups with
glistening oil; fresh basil, chili flakes and a snowfall of parmesan. A halved
cherry tomato, a basil leaf and flaky salt sit beside the slice. One dish, one
bold diagonal silhouette — it still reads as pizza at 300 pixels across.

The image is an original work drawn procedurally for this entry (Python + PIL,
layered gradients, soft light and grain — not the kit's starter image, not a
copy of any existing artwork or photo). The program is a plain base64 decode —
the rules explicitly allow a repository holding the image and a program that
writes it to `/output/entry.png` — so both grader runs write identical bytes.

## Files

- `entry.png.b64` — the picture, base64-encoded on a single line (the repo
  stays plain UTF-8 text). JPEG bytes under the name `entry.png` once decoded
  (the rules allow PNG or JPEG, told apart by their first bytes). 1024x1024,
  233,116 bytes, sha256
  `a630b2c3967c0a486817592783f6b9262f6d0cc3ae9f3bc8a36b4fcc5d184398`.
- `main.ts` — Node 22, standard library only. Decodes `entry.png.b64` and
  writes `$MAKEFUN_OUTPUT_DIR/entry.png` (or `/output/entry.png` in the
  grader).

## Run it locally

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# out/entry.png is byte-identical to the shipped picture
```
