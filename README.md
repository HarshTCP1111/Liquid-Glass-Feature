# 💧 Liquid Glass Effect (Vanilla JS)

A draggable, animated **"liquid glass" shader effect** built entirely in **Vanilla JavaScript**, using SVG filters and HTML5 canvas — no external dependencies required.

> Created by [Harsh S](https://github.com/HarshTCP1111) — 2025

---

## 🚀 Demo

Paste the code snippet directly into your browser’s **Developer Console** (DevTools) and see the **interactive liquid glass** appear on your screen.

Drag it around. Resize the window. Watch it respond to your mouse.

---

## 🧠 Features

- ✅ No dependencies (pure JavaScript)
- 💠 Uses SVG `feDisplacementMap` for the blur effect
- 🖱️ Draggable UI with constrained viewport movement
- 📏 Dynamically responsive to mouse position
- ⚙️ Clean destruction and reinitialization logic
- 🎨 Shader-like distortion map using canvas

---

## 🧾 How to Use

### 🖥 Paste into Console

1. Open any webpage.
2. Press `F12` (or right-click → Inspect → Console).
3. Paste the full script.
4. Press `Enter`.

A glowing, draggable "liquid glass" will appear in the center of your screen!

---

## 📦 Code Structure

- **Shader Class:**  
  Handles UI creation, displacement map generation, dragging logic, and animation.

- **RoundedRectSDF + SmoothStep:**  
  Core math functions for creating a dynamic and smooth displacement.

- **SVG Filters + Canvas:**  
  Combines `<feDisplacementMap>` and `<feImage>` with a dynamic canvas-generated texture.

---

## 🔧 Customization

You can tweak the following inside the `createLiquidGlass()` function:

```js
width: 300,
height: 200,
```

Or change how distortion behaves via:

```js
fragment: (uv, mouse) => {
  // ... customize shader logic here
}
```

---

## 🧹 Cleanup

If a glass instance already exists, it will be **destroyed automatically** when a new one is created:

```js
if (window.liquidGlass) {
  window.liquidGlass.destroy();
}
```

To manually remove it:

```js
window.liquidGlass.destroy();
```

---

## 🧑‍💻 Author

Built by **Harsh Shuddhalwar**  
GitHub: [@HarshTCP1111](https://github.com/HarshTCP1111)

---

## 📄 License

MIT License – Free to use, share, and modify.

---

## ❤️ Support & Contributions

If you enjoy this project or want more JS shader-style effects, feel free to ⭐️ star and fork the repo. PRs and ideas welcome!
