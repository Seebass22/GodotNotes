## fall collider
- create Area2D with child:
	- create CollisionShape2D

## get extents of CollisionShape2D
```gdscript
$CollisionShape2D.shape.get_extents().x
```

## layers
- configure names: Project > Project Settings
- On each object with collision, under "Collision" set:
	- "Layer" to layer that object should belong to
	- "Mask" to layers that should collide with object

## raycasts
RayCast2D node
- set collision mask
- remember to check "enable"

check for collision
```gdscript
$RayCast2D.is_colliding()
```

enable/disable
```gdscript
$RayCast2D.enabled = false
```
