# Drawing the room yourself

The viewer shows your room as **six square drawings folded into a cube around you**: four walls, the ceiling and the floor. Each square is what you'd see standing in the middle of the room, looking straight at that side, with a 90° view.

## The format

One image laid out as a **cross**, 4 squares wide and 3 squares tall. Start from `template.png`.

```
          [CEILING]
[LEFT ]   [FRONT  ]   [RIGHT ]   [BACK ]
          [FLOOR  ]
```

- **Size:** 4:3. 6144 × 4608 (1536 px squares) is a good size, and 8192 × 6144 is the most worth using. The size must divide into equal squares.
- **Front** is the first view visitors see.
- **Seams:** edges that touch in the cross must line up (front↔left, front↔right, right↔back, ceiling↔front, floor↔front). The back wall's right edge wraps round to the left wall's left edge. The ceiling's top edge and the floor's bottom edge meet the back wall, and their sides meet the side walls (turned 90°).
- **Perspective:** every square's vanishing point is its centre (red dot). The horizon (red line) is eye level, and it's the same height on all four walls. Lines going "into" a wall run towards its centre. The blue lines show where the floor and ceiling meet the walls in the example room. Your room can differ, as long as all four walls agree.
- Leave the grey corners of the cross empty.

## The files

Put these in `2d/room/` next to `index.html`:

| File | What | Needed? |
| --- | --- | --- |
| `off.png` | the room with the lights off (e.g. blue hour) | yes |
| `on.png` | the same drawing with the lamps on | optional; without it the viewer tints `off.png` |
| `hotspots.png` | same layout, black background, clickable things painted in flat colours | optional |

Hotspot colours (fill the whole object, no anti-aliasing):

| Colour | Opens |
| --- | --- |
| red `#FF0000` | Projects |
| green `#00FF00` | About |
| blue `#0000FF` | Skills |
| yellow `#FFFF00` | Contact |
| magenta `#FF00FF` | Lights on/off |
| cyan `#00FFFF` | a screen that plays the typing terminal (opens Projects) |

When `off.png` is there, the site uses your drawing instead of the built-in one. The glow, zoom-on-click, menu and lights all work the same. `example_off.jpg` and `example_hotspots.png` are the built-in room in this format, if you want to trace or paint over it.

## Tips

- Draw `on.png` by duplicating your `off.png` layer and repainting the light, so the two line up exactly.
- Check the seams by opening the site. Any break shows up as a crease.
- The ceiling and floor squares look straight up and straight down, so a ceiling lamp sits in the middle of the ceiling square.
