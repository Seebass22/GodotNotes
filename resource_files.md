- similar to scriptable objects in unity
- expose properties to editor

resource script
```gdscript
extends Resource

class_name Dialog

export (Texture) var avatar_texture
export (Array, String) var dialog_slides
```

using resource in script
```gdscript
export (NodePath) onready var _dialogText = get_node(_dialogText) as Label
export (NodePath) onready var _avatar = get_node(_avatar) as TextureRect
export (Resource) var _currentDialog = _currentDialog as Dialog

func _ready():
	_avatar.texture = _currentDialog.avatar_texture
	_dialogText.text = _currentDialog.dialog_slides[0]
```
