- add tween node as child
- add script on parent:
	- use tween.interpolate_property()
	- tween.start() to start



```gdscript
$Tween.interpolate_property(self, "rect_scale", start_scale, end_scale, tween_time, Tween.TRANS_CUBIC, Tween.EASE_OUT)
$Tween.start()
```
