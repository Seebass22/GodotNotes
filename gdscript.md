## signals
declare signal
```gdscript
signal coin_collected
```

send signal
```gdscript
emit_signal("coin_collected")
```

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
extends KinematicBody2D
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

# General tips
- you can run event functions manually

```gdscript
_ready()
```

