# Minimal Map and Movement System

## Overview

`minimal-map-movement.html` is a self-contained, standalone system that isolates and demonstrates the world map structure and player movement mechanics from the main game.

## Purpose

This system allows experimentation with just the world and movement system in isolation, without any gameplay features. It's useful for:
- Testing map generation and tile rendering
- Debugging movement mechanics
- Understanding the coordinate system
- Performance testing of large worlds
- Prototyping new features related to map and movement

## Features Included

1. **World Map Structure**
   - Fixed-size grid: `WORLD_SIZE = 8000` units
   - Tile division: `TILE_SIZE = 16`, `blockSize = 800`
   - Grid-based terrain with streets and grass tiles
   - Street layout in a regular grid pattern

2. **Player Movement**
   - WASD key controls
   - Smooth movement with configurable speed (200 units/second)
   - World boundary collision detection
   - Normalized diagonal movement

3. **Rendering**
   - Efficient tile-based rendering with viewport culling
   - Camera that smoothly follows the player
   - Visual distinction between grass tiles, streets, and paths
   - Player character rendered as a bright green circle
   - Direction indicator showing player orientation

4. **UI**
   - Real-time position display
   - World parameters display (size, tile size, block size)
   - Simple control instructions

## Features NOT Included (by Design)

- Buildings, zombies, loot
- Combat and weapons
- Fog of war, minimap
- Inventory system
- Day/night cycle
- Audio
- Any gameplay mechanics

## Usage

Simply open the file in a web browser:

```bash
# Option 1: Direct file open
open minimal-map-movement.html

# Option 2: Via local server (recommended for development)
python3 -m http.server 8080
# Then navigate to: http://localhost:8080/minimal-map-movement.html
```

### Controls

- **W** - Move up (north)
- **A** - Move left (west)
- **S** - Move down (south)
- **D** - Move right (east)

## Technical Details

### World Structure

- The world is divided into blocks of 800x800 units
- Streets are 120 units wide and positioned between blocks
- The player starts at the center of the world (4000, 4000)
- Terrain tiles are rendered as 100x100 units for performance

### Camera System

- The camera smoothly follows the player with interpolation (factor: 0.1)
- This creates a smooth scrolling effect
- The player is always rendered at the center of the viewport

### Performance

- Viewport culling ensures only visible tiles are rendered
- The system can handle the full 8000x8000 world smoothly
- Approximately 6,400 terrain tiles generated for the entire world

## Integration

To integrate features from this system back into the main game:
1. The terrain generation logic can be found in the `generateTerrain()` function
2. The movement logic is in the `update()` function
3. The rendering logic is in the `draw()` function
4. All constants are clearly defined at the top of the script section

## File Size

~10KB - completely self-contained with no external dependencies
