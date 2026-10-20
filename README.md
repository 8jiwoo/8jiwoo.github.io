<div align="center">

# Jiwoo's Room

**A little 360° room you can look around in. My portfolio.**

[**Open it → 8jiwoo.github.io**](https://8jiwoo.github.io)

<a href="https://8jiwoo.github.io"><img src="docs/preview.jpg" alt="A cartoon-style living room at blue hour, seen through a fisheye lens" width="100%"></a>

</div>

## Look around

You're standing in the middle of a small flat just before sunrise. Drag to look around, scroll or pinch to zoom, and click things in the room:

| Click | Opens |
| --- | --- |
| 📺 The TV | **Projects** |
| 🗄️ The pink cabinet | **About** |
| 📚 The bookshelf | **Skills** |
| ☎️ The red phone | **Contact** |
| 💡 Any light | Lights on / off |

The menu along the top does the same thing. Turn the sound on (bottom right) for a quiet, rainy-morning soundtrack.

## How it's made

- **360° panorama**: the room is two 8192×4096 equirectangular images, lights off and lights on (4096 on phones), shown through a fisheye lens and crossfaded when you flip the lights. That's the same idea as Balming Tiger's krpano tour.
- **Live layers pinned on top**: the fire, the typing terminal on the TV, the clock hands, the curtains, lamp glows and the hover outlines are real 3D objects at their true positions. They line up with the photo as you look around, and hide correctly behind furniture.
- **Built with [three.js](https://threejs.org)** in a single `index.html`. No framework and no build step.
- **The panorama comes from the room itself**: the low-poly room with photographic textures is rendered once into the two images. `index.html#live` shows that room rendered in real time, which is also the automatic fallback if the images fail to load. `index.html#bake` exposes the tool that produces new images.

### Using a real 360° photo

To swap in a photographed room, shoot it from the middle of the room at about 1.2–1.7 m: a 2:1 equirectangular JPEG, ideally 8192×4096, with no visible seam, once with the lamps off and once with them on. Save them as `assets/room_off_8k.jpg` and `room_on_8k.jpg`, plus 4096×2048 `_4k` versions. Then move the hotspot shapes to match the photo, or use the `LAYERS` list in `index.html` to pin photos, posters or notes at a yaw and pitch.

### Run it locally

```bash
python3 -m http.server
# then visit http://localhost:8000
```

## Credits

3D models from the [Khronos glTF Sample Assets](https://github.com/KhronosGroup/glTF-Sample-Assets):

- **Glam Velvet Sofa**: Eric Chadwick, © 2021 Wayfair, LLC ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
- **Diffuse Transmission Plant**: Eric Chadwick, © 2024 Darmstadt Graphics Group GmbH ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)), based on an original by Rico Cilliers ([CC0](https://creativecommons.org/publicdomain/zero/1.0/))
- **Glass Vase with Flowers**: Eric Chadwick and Rico Cilliers ([CC0](https://creativecommons.org/publicdomain/zero/1.0/))

Photo textures: wood grain and woven fabric from the **Sheen Chair** sample by Eric Chadwick / Wayfair ([CC0](https://creativecommons.org/publicdomain/zero/1.0/)); floorboard and checker-tile photos from the [three.js examples](https://github.com/mrdoob/three.js/tree/dev/examples/textures).

Night environment light also from the three.js examples. Menu layout inspired by [Balming Tiger](https://balmingtiger.com).

---

<div align="center">

[LinkedIn](https://www.linkedin.com/in/jiwoohahaha) · [GitHub](https://github.com/8jiwoo)

</div>
