# Graphics Refresh (Option A: Tactical Vector Style)

This document summarizes the updated visual direction for the current `index.html` build. The goal is a Door Kickers–inspired, top-down tactical look using clean silhouettes, restrained palettes, and clearer depth cues.

## Summary of Visual Changes
- **Terrain** now uses layered fills with subtle streaks/seams and edge highlights to improve readability and separation between grass, streets, and paths.
- **Buildings** have soft drop shadows, roof insets, and stronger outlines for depth and tactical readability.
- **Loot boxes** gained a more defined lock strip and medallion for cleaner silhouette recognition.
- **Characters** (player and zombies) are drawn as flat tactical silhouettes with stronger edge strokes and body/helmet separation instead of pure circles.
- **Weapons** use sharper vector-like silhouettes and metallic highlights to read better at a distance.

## Style Notes
- Everything remains canvas-drawn to keep performance predictable and assets minimal.
- The palette favors muted mid-tones with bright accent edges to mirror Door Kickers’ clarity.
- Shadows are soft and consistent to emphasize height without needing full sprite art.

## Next Iteration Candidates
- Introduce a limited decal system (cracks, stains, road markings) using precomputed stamps.
- Add unit “unit markers” (tiny icon overlays) for quick target recognition.
- Optional vignette and subtle AO to further boost contrast between objects and ground.
