# VOXELIFY

Client-side image-to-voxel pipeline converter using WebGL/Three.js.

## System Overview

```
[ Image Input ] -> [ HTML5 Offscreen Canvas ] -> [ Pixel Array (RGBA) ]
                                                        |
                                            [ Brightness/Color Maps ]
                                                        |
[ 3D Render Viewport ] <- [ THREE.Mesh BoxGeometry Stack (Material Cached) ]
```

## Stack

- Core: Vanilla JS / HTML5 Canvas API
- 3D Renderer: Three.js (r128) + OrbitControls
- Typography: Press Start 2P, VT323

## Input Processing Parameters

- Resolution: 8x8 to 48x48 grid matrix
- Vertical Scaling: 1x to 8x height multiplier
- Color Mapping Mode: Full RGB, Nearest-Neighbor Euclidean Minecraft 16, Grayscale, Pastel, Warm, Neon

## Control Mappings

| Command | Action |
| --- | --- |
| Drag (Left Click) | Orbit camera |
| Scroll | Zoom viewport |
| `R` | Reset camera viewport / focus |
| `SPACE` | Toggle auto-rotation |
| `G` | Toggle base grid visibility |
| `F` | Toggle scene linear fog |
| `L` | Cycle lighting presets (Night, Day, Dusk) |
| `+` / `-` | Scale voxel model bounds |

## Optimization Specs

- O(C) Material Overhead: Reuses THREE.MeshLambertMaterial instances via color-key hashing.
- O(1) Bobbing Overhead: Stateless per-frame Y-axis transform based on global scene delta, replacing dynamic bounding box calculations.
- Web Share API integration with dynamic path resolution for production contexts.

## License

MIT License. See LICENSE for details.
