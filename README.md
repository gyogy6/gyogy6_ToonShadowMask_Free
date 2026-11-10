# gyogy6 Anime Shadow Mask (Free)

**English** / [日本語](README.ja.md) / [简体中文](README.zh-CN.md) / [한국어](README.ko.md)

A generator for Substance 3D Painter.
Set the light direction, and it creates a crisp anime-style (cel-shaded) shadow area as a black-and-white mask.
Just drop it into a layer mask.

- Version: 1.0.0
- Price: Free (commercial use allowed, credit optional)
- Terms of use: [LICENSE.md](LICENSE.md) (**by downloading or using this product, you agree to these terms**)

---

## 1. Included files

| File | Description |
|---|---|
| `gyogy6_anime_shadow_mask.sbsar` | The generator |
| `README.md` and others | This manual (English, Japanese, Chinese, Korean) |
| `LICENSE.md` | Terms of use |

## 2. Requirements

- Adobe Substance 3D Painter
- The model must have **UVs unwrapped**

## 3. Installation

1. In Painter, open **File → Import resources**.
2. Click **Add resources** and select `gyogy6_anime_shadow_mask.sbsar`.
3. Set the type of the added file to **generator**.
4. Choose where to import it:
   - For the current project only: **Current session** or **Project**
   - For all projects: your own library
5. Click **Import**.
6. Installation is complete when **gyogy6 Anime Shadow Mask** appears under **Generators** in the asset shelf.

## 4. Preparation: bake mesh maps (once per project)

This generator uses the mesh maps baked by Painter.

1. In the **Texture Set Settings** panel, click **Bake Mesh Maps**.
2. Make sure these two are checked:
   - **World space normal** (used for the light direction; **required**)
   - **Ambient occlusion** (used to shade cavities)
3. Click **Bake selected textures** and wait until baking finishes.

## 5. Usage

### 5-1. Create a shadow layer

1. In the Layers panel, click **Add fill layer**.
2. On the new layer, **turn off every channel except Base Color**.
3. Set **Base Color** to the shadow color.
   A slightly tinted color (reddish for skin, bluish purple for clothes, etc.) gives cleaner anime shadows than plain gray.
4. Set the blend mode to **Multiply**.

### 5-2. Add the generator to the mask

1. Right-click the layer and choose **Add black mask**.
2. Right-click the mask and choose **Add generator**.
3. In the generator selector, choose **gyogy6 Anime Shadow Mask**.
4. If the color appears only on the shadow areas, it works.

### 5-3. Parameters

| Parameter | Meaning | Typical |
|---|---|---|
| **Light Horizontal (deg)** | Direction the light comes from (0–360°). 0 = from the front of the model. | 30–60 |
| **Light Vertical (deg)** | Light height (-89–89°). Higher = from above. | 20–50 |
| **Shadow Amount** | Shadow size. Higher = wider shadow. | 0.4–0.6 |
| **Feather** | Softness of the shadow edge. Smaller = crisper. | 0.01–0.05 |
| **AO Influence** | How strongly cavities (armpits, under the neck, cloth overlaps) are always shaded. | 0.3–0.8 |
| **Invert (lit side)** | 1 = the lit side becomes white instead of the shadow. For highlights. | 0 |

### 5-4. Tips

- **Add a darker second shade:** create another layer the same way with a small **Shadow Amount (0.1–0.3)**.
- **Fix by hand:** in the mask, add a **Paint** effect above the generator and paint white (add shadow) or black (remove shadow).
- **Highlights:** create a layer with **Invert** set to 1 and use the **Screen** blend mode.

## 6. Troubleshooting

| Problem | What to check |
|---|---|
| gyogy6 Anime Shadow Mask is not in the list | Make sure you set the type to **generator** when importing. If you imported it as another type, delete it and import it again. |
| Everything is black, or nothing appears | Make sure the mesh maps are baked (section 4). **World space normal** is required. |
| The light comes from an unexpected direction | Adjust Light Horizontal / Light Vertical. |

## 7. Terms of use: key points

Please read [LICENSE.md](LICENSE.md) for the full terms. This is only a summary.

**You may**
- Use it as an individual or a company, for commercial or non-commercial purposes
- Sell or distribute works made with textures created by this tool (VRChat avatars, games, illustrations, etc.). Credit is optional.

**You may not**
- Redistribute or sell the `.sbsar` file (even for free, even unmodified)
- Modify, analyze or extract the contents of the `.sbsar`
- Distribute Painter projects (.spp), smart materials, smart masks or templates **that still contain this generator**
  → Before distributing, **export the textures as images**.
- Use it as AI training data, or issue it as an NFT

If you want to introduce this product to others, please share the URL of the download page, not the file.

## 8. Contact

Bug reports are welcome via GitHub Issues (a response is not guaranteed).

---

Adobe and Substance 3D Painter are trademarks or registered trademarks of Adobe. This product is not affiliated with or endorsed by Adobe.
© 2026 gyogy6
