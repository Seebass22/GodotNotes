## signals
declare signal
```gdscript
signal coin_collected
```

send signal
```gdscript
emit_signal("coin_collected")
```

## random numbers
`Randomize()` randomize seed

`randi()` return random uint32

`rand_range()` random float in range

## remove node (when it is safe to)
```gdscript
queue_free()
```

## string concatenation
```gdscript
print("I have this many coins: ", coins)
```

## inheritance
`extends` keyword at top of file
```gdscript
# extend built-in
extends KinematicBody2D

# extend unnamed class
extends "Res://CustomClass"

# extend named-class
extends CustomClass
```

## make variable configurable from inspector
`export` keyword
```gdscript
const FLOOR_NORMAL: = Vector2.UP
```

## get a node (only immediate children)
```gdscript
get_node(path)
```

shorthand: `$`
```gdscript
$AnimatedSprite.play()
# same as
get_node("AnimatedSprite").play()
```

## switch scene
```gdscript
get_tree().change_scene("scene_path")
```

# General tips
- you can run event functions manually

```gdscript
_ready()
```
