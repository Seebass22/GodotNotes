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

## enums
```gdscript
# define enum
enum chordType {MAJ, MIN, DIM, AUG}

# create variable of enum type and export
export (chordType) var currentChordType = chordType.MIN
```

## switch statement
```gdscript
match statement:
	chordType.MAJ:
		pass
	chordType.MIN:
		pass
```

## signals
declare signal
```gdscript
signal coin_collected
```

send signal
```gdscript
emit_signal("coin_collected")
```

connect signal
```gdscript
# connect the signal "health_changed" of character node with function _on_Character_health_changed on lifebar node
func _ready():
	var character_node = get_node('Character')
	var lifebar_node = get_node('UserInterface/Lifebar')

	character_node.connect("health_changed", lifebar_node, "_on_Character_health_changed")
```

## coroutines
wait seconds
```gdscript
yield(get_tree().create_timer(5.0), "timeout")
```

## random numbers
`randomize()` randomize seed

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

## cache on ready
```gdscript
onready var label = get_node("Label")

# same as
var label
func _ready():
	label = get_node("Label")
```

## reference another node (choose in editor)
```gdscript
export (NodePath) var _dialogTextPath
onready var _dialogText: Label = get_node(_dialogTextPath)
# or
export (NodePath) onready var _dialogText = get_node(_dialogText) as Label
```

## format strings
```gdscript
var score_text = "score: %d / %d points" % [score, max_score]
```

## switch scene
```gdscript
get_tree().change_scene("scene_path")
```

## check OS (build)
```gdscript
if OS.get_name() == "HTML5":
```

## quit
```gdscript
get_tree().quit()
```

# General tips
- you can run event functions manually

```gdscript
_ready()
```

## instantiate scene
```
const Bullet = preload("res://Bullet.tscn")

var bullet = Bullet.instance()
# add to parent
get_parent().add_child(bullet)
# or add as child of current node
add_child(bullet)
```
