# 🟫 VOXELIFY — Image-to-Voxel Live Converter

Voxelify is a self-contained, browser-native 3D voxel art generator. It reads any image pixel-by-pixel, samples the dominant colors, and procedurally builds a spinning, interactive 3D voxel scene using Three.js—all computed client-side, with zero server uploads.

The user interface features a deep retro Minecraft-themed aesthetic (stone gradients, pixel fonts, custom mechanical keycaps, blocky inputs, and grass-block buttons).

---

## 🎯 Features

*   **Zero Server Uploads**: Processing runs 100% locally in the browser using HTML5 Canvas pixel sampling.
*   **Signature Aesthetic Detail**: An SVG outline dashed-border crawl animation that wraps the drop zone upon hover.
*   **Voxel Height Scaling**: Procedural generation scales the height columns based on pixel brightness.
*   **Palette Remapping Filters**:
    *   **Full Color**: Retains original image colors.
    *   **Minecraft (16)**: Standard 16-color block palette resolved using Euclidean nearest-match calculations.
    *   **Pastel**: Soft, desaturated colors.
    *   **Grayscale**: Pure black-and-white tonal output.
    *   **Warm Tones**: Warm/earthy accent overrides.
    *   **Neon**: Maximum saturation scaling.
*   **Performance Optimization**: Employs a material cache (`matCache`) to share materials among identical colors, preventing compile overhead.
*   **Export Tools**: Download your creation as a high-resolution PNG screenshot or share it via the Web Share API.

---

## 🎮 Live Interactive Camera & Controls

*   **Orbit**: Left-Click + Drag
*   **Zoom**: Mouse Scroll Wheel
*   **Reset Camera**: <kbd>R</kbd>
*   **Toggle Auto-rotation**: <kbd>SPACE</kbd>
*   **Toggle Ground Grid**: <kbd>G</kbd>
*   **Toggle Scene Fog**: <kbd>F</kbd>
*   **Cycle Lighting Presets**: <kbd>L</kbd> *(Night 🌙, Day ☀️, Dusk 🌆)*
*   **Scale Voxel Art Size**: <kbd>+</kbd> / <kbd>-</kbd>

---

## ⚙️ CDN Libraries Used

No installation required. CDN dependencies are loaded automatically:
*   Three.js (r128)
*   OrbitControls
*   Google Fonts (*Press Start 2P*, *VT323*)

---

## 🚀 Deployed Sharing Context

The application includes full support for the **Web Share API**. When deployed over a secure connection (HTTPS) on GitHub Pages or a custom domain, mobile and modern desktop users will be able to share their generated voxel scenes as image files directly to messaging apps and social media, falling back to a shareable link copier.

---

## 📄 License

Released under the **MIT License**. Refer to the [LICENSE](LICENSE) file for terms and conditions.
