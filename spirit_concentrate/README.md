# Spirit concentrate: item textures

16x16 RGBA PNG item icons with a transparent background and hard pixels (alpha is 0 or 255 only).

Each icon is a single brilliant-cut spirit gem:
- a flat table on top;
- a bright girdle;
- a pavilion whose facets meet in a point at the bottom;
- a glowing diagonal crack across the shaded side.

The icon is lit from the upper left. Each icon uses its own 8-tone ramp. The ramps are built from Malum spirit textures, then hue-shifted and resaturated, so they are not copies of the spirit palettes.

`preview/` holds review sheets only. Do not copy it into `assets/`.

## Files and suggested spirit mapping

| File | Built from | Suggested spirit |
|---|---|---|
| `spirit_concentrate_cyan.png` | aerial | aerial |
| `spirit_concentrate_blue.png` | aqueous | aqueous |
| `spirit_concentrate_lime.png` | earthen | earthen |
| `spirit_concentrate_yellow.png` | infernal | infernal |
| `spirit_concentrate_pink.png` | sacred | sacred |
| `spirit_concentrate_purple.png` | wicked | wicked |
| `spirit_concentrate_black.png` | umbral | umbral |
| `spirit_concentrate_raspberry.png` | sacred, shifted toward red | arcane (or a custom variant) |
| `spirit_concentrate_indigo.png` | wicked, shifted toward blue | eldritch (or a custom variant) |
| `spirit_concentrate_mixed.png` | wicked, with cyan, pink and yellow crack inclusions | a generic or mixed concentrate |

## Using them in a mod (Minecraft 1.21.1)

`<modid>` and the item ids are placeholders.

1. Copy a PNG to `assets/<modid>/textures/item/<item_id>.png`.
2. Create `assets/<modid>/models/item/<item_id>.json`:

```json
{
  "parent": "minecraft:item/generated",
  "textures": {
    "layer0": "<modid>:item/<item_id>"
  }
}
```

3. Add a name to `assets/<modid>/lang/en_us.json`:

```json
{
  "item.<modid>.<item_id>": "Aerial Spirit Concentrate"
}
```

1.21.1 does not use the `assets/<modid>/items/` item definitions. Those were added in 1.21.4.
