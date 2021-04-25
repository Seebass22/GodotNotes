## drawing, selecting tiles
- left click to draw
- right click to erase
- press ctrl to select block
- press shift to draw line

## scale tilemap
- modify "scale" under Node2D on TileMap

# procedural map
```gdscript
# place tile
tilemap.set_cell(xPos, yPos, tileIndex)
# update autotile bitmask to display correct tile
# vectors are start and stop position in tilemap
tilemap.update_bitmask_region(Vector2(0.0, 0.0), Vector2(16, 16))
```

example: place 2x16 tiles, starting at 0,0
```gdscript
	for y in range(16):
		for x in range(2):
			$Walls.set_cell(x, y, 0)
	$Walls.update_bitmask_region(Vector2(0.0, 0.0), Vector2(16, 16))
```
