# World Builder Guide: Heresy Gaming Minecraft Server (Gothrasea Map)

## Overview
**World Name:** Gothrasea  
**Server Type:** Towny RPG with MMO mechanics  
**Map Size:** 2048 x 2048 blocks  
**Minecraft Version:** 1.21.4 (Java Edition)  
**Tools Required:** WorldPainter, WorldEdit, optional: WorldMachine, Chunky, VSCode

This guide is for Fiverr contractors tasked with building the custom terrain, infrastructure, and layout for the Gothrasea Minecraft world. The final product will serve as the world foundation for Heresy Gaming's Towny server.

---

## Contents
1. Heightmap & Terrain Generation  
2. Biomes & Environmental Zones  
3. Kingdoms & Lore Descriptions  
4. Settlements & Towny Integration  
5. Rivers & Water Systems  
6. Trade Routes & Road Systems  
7. Points of Interest (Markers & Lore Sites)  
8. Dungeons & Special Zones  
9. Technical Details (WorldPainter, Exporting)  
10. Deliverables & Checklist

---

## 1. Heightmap & Terrain Generation

### Heightmap:
- Use `Gothrasea Heightmap.png` or `.svg` to import into WorldPainter
- Y-level range: 50 (low/ocean) to 160 (mountain peaks)

### Elevation Configuration:
| Color | Feature | Y-level Range | Notes |
|-------|---------|----------------|-------|
| Deep Blue | Ocean | 50–61 | Lakes/rivers |
| Light Blue | Shoreline | 62–65 | Beach/Stony Shore |
| Green | Plains/Forest | 66–80 | Standard land |
| Yellow | Hills | 81–100 | Gentle slopes |
| Orange | Lower Mountains | 101–130 | Mid-height terrain |
| Red | Mountains | 131–160 | Jagged/cliff edges |

---

## 2. Biomes & Environmental Zones

### Distribution:
Reference `Gothrasea Biomes.csv` and the Biome Map PNG.

| Terrain | Biomes |
|---------|--------|
| Plains | Plains, Meadow |
| Forests | Forest, Birch Forest, Dark Oak |
| Hills | Windswept Hills, Savanna Plateau |
| Mountains | Jagged Peaks, Stony Peaks |
| Water | Ocean, River |
| Jungle/Tropical | Jungle, Mangrove Swamp |

Apply biome brushes after terrain formation. Smooth transitions are critical.

---

## 3. Kingdoms & Lore Descriptions

Use `Gothrasea States.csv` and the political map to define borders. Each major state has a unique lore profile:

### 1. Thearchy of Silean
A mystic, lunar-worshipping society led by spiritual dreamseers. Architecture is temple-based with gothic towers. Ancient relics lie buried beneath cities.
- **Style:** Gothic, Monastic
- **Towny Tag:** Silean

### 2. Kingdom of Hlioriat
A noble, tradition-bound kingdom with banners on every hill. Known for elite knights and stone keeps. Biomes are temperate forests and plains.
- **Style:** Feudal European
- **Towny Tag:** Hlioriat

### 3. Republic of Cielb
Technocratic and advanced, with coastal merchant cities and canal systems. Central hubs for trade.
- **Style:** Venetian, Harbor City
- **Towny Tag:** Cielb

### 4. Kingdom of Harlythaneth
Isolationist and mountainous, this kingdom thrives in alpine terrain. Home to rugged stonemasons.
- **Style:** Nordic/Mountain Dwarven
- **Towny Tag:** Harlyth

### 5. Dironglian Empire
Imperial and expansive, this faction builds monumental architecture and aqueducts across the land.
- **Style:** Roman/Byzantine
- **Towny Tag:** Dirongl

### 6. Republic of Kutyurt
Desert merchants and oasis builders. Their cities are hub-stops for caravans crossing wastelands.
- **Style:** Adobe, Middle Eastern
- **Towny Tag:** Kutyurt

### 7. Asyturt Horde
Nomadic plainsmen with mobile towns and vast herds. Expect yurts and seasonal encampments.
- **Style:** Mongolian Steppe
- **Towny Tag:** Asyturt

### 8. Commonwealth of Alkenrodel
Artisan nation, valuing nature and magic. Glimmering forests, elven-style builds.
- **Style:** High Fantasy/Nature
- **Towny Tag:** Alken

### 9. Principality of Yanesin
A seafaring archipelago chain with coral cities and port towns. Naval dominance.
- **Style:** Pirate/Island Nation
- **Towny Tag:** Yanesin

### 10. Tyerel Theocracy
Militant and disciplined, this theocracy trains elite inquisitors. Fortified cities and clerical strongholds.
- **Style:** Crusader Monastic
- **Towny Tag:** Tyerel

---

## 4. Settlements & Towny Integration

Reference `Gothrasea Burgs.csv` and `Markers.geojson`

| Type | Size | Notes |
|------|------|-------|
| Capital | 300–500 blocks wide | Largest, custom-built |
| City | 200–300 blocks | Mid-size hub |
| Town | 100–200 blocks | Towny-joinable |
| Village | 60–100 blocks | Background flavor |

**Towny Requirements:**
- Each major settlement must have flat land
- Include space for Towny plots: farms, homes, outposts

---

## 5. Rivers & Water Systems

Use `Rivers.geojson` or `Rivers.csv`. Carve water networks:
- Major rivers: 10–15 blocks wide
- Tributaries: 5–8 blocks wide
- Flow toward oceans/lakes

Rivers must:
- Follow terrain curves
- Connect with trade routes where applicable

---

## 6. Trade Routes & Road Systems

Use `Routes.geojson` and `Routes.csv`

- Main roads: 5 blocks wide (gravel, coarse dirt, stone brick)
- Secondary roads: 3 blocks
- Trails: 2 blocks

Include:
- Bridges over rivers
- Tunnels through hills
- Rail corridors (3–5 blocks cleared for future rail line placement)

---

## 7. Points of Interest (POIs)

Use `Markers.geojson` or `Markers.csv`

Marker Types:
- Dungeon Entrances
- Lore Shrines
- Abandoned Fortresses
- Mythical Trees / Totems
- Warp Hubs / Fast Travel Points

Minimum: 1–2 POIs per kingdom.

---

## 8. Dungeons & Special Zones

### Suggested Dungeon Sites:
- **Abbey of Nightmares** (-1800, ~70, -1600)
- **Ghost Tower** (2100, ~90, -1900)

Dungeon Terrain:
- 100x100 flat areas
- Atmospheric terrain (foggy, cliffs, ruins nearby)
- Mark these zones clearly with wool blocks underground

---

## 9. Technical Details

### WorldPainter Instructions:
- Use 2048x2048 heightmap at 1:1 scale (1 pixel = 1 block)
- Y levels: 50 (deep ocean) to 160 (mountain)
- Use `Noise`, `Smooth`, `Flatten`, `Raise/Lower` tools
- Paint biomes post-terrain

### Resource Distribution:
| Ore | Height | Location Notes |
|-----|--------|----------------|
| Coal | -64 to 128 | Common, especially near Axstone |
| Iron | -32 to 64 | Hills and mountains |
| Gold | -64 to 32 | Sparse, mountain-only |
| Diamond | -64 to -16 | Very rare |
| Copper | -16 to 112 | Windswept areas |

---

## 10. Deliverables & Checklist

### Files to Deliver:
- WorldPainter project (`.world`)
- Exported Minecraft world folder
- Top-down overview map (PNG)
- README with settings used
- Coordinate reference list
- Zip of all files

### Requirements:
- Smooth terrain transitions
- Accurate biome placement
- Flat areas at each major settlement
- Rivers and roads match data files
- No unwalkable or unbuildable terrain zones
- No pre-built structures unless specified

---

*End of Guide.*

