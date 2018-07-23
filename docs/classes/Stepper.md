# Stepper

**super**: [UIStepper](UIStepper.md) on iOS

A stepper control provides a user interface for incrementing or decrementing a value. A stepper displays two buttons, one with a minus (“–”) symbol and one with a plus (“+”) symbol. If you set stepper behavior to “autorepeat” (which is the default), pressing and holding one of its buttons increments or decrements the stepper’s value repeatedly. The rate of change depends on how long the user continues pressing the control. The maximum value must be greater than or equal to the minimum value. If you set a maximum or minimum value that would make break this invariant, both values are set to the new value. For example, if the minimum value is 200 and you set a maximum value of 100, then both the minimum and maximum become 200.

### Events

* **Load**()
This event is called when the object becames available in the current runtime system.

* **Changed**(**value**: <strong>[Float](../gravity/types.md)</strong>)
Use this event to be notified when value changes.

* **Unload**()
This event is called when the object has been removed from the current runtime system (but not yet deallocated).

</ul>

### Properties

* **var** **value**: **[Float](../gravity/types.md)**
The numeric value of the stepper.

* **var** **minimumValue**: **[Float](../gravity/types.md)**
The lowest possible numeric value for the stepper.

* **var** **maximumValue**: **[Float](../gravity/types.md)**
The highest possible numeric value for the stepper.

* **var** **stepValue**: **[Float](../gravity/types.md)**
The step, or increment, value for the stepper.

* **var** **continuous**: **[Bool](../gravity/types.md)**
The continuous vs. noncontinuous state of the stepper. If true, value change events are sent immediately when the value changes during user interaction. If false, a value change event is sent when user interaction ends. The default value for this property is true.

* **var** **autorepeat**: **[Bool](../gravity/types.md)**
The automatic vs. nonautomatic repeat state of the stepper. If true, the user pressing and holding on the stepper repeatedly alters value. The default value for this property is true.

* **var** **wraps**: **[Bool](../gravity/types.md)**
The wrap vs. no-wrap state of the stepper. If true, incrementing beyond maximumValue sets value to minimumValue; likewise, decrementing below minimumValue sets value to maximumValue. If false, the stepper does not increment beyond maximumValue nor does it decrement below minimumValue but rather holds at those values.

</ul>

### Methods

* **func** **backgroundImageForState**(**state**: <strong>[Int](../gravity/types.md)</strong>): <strong>[Image](image.md)</strong> 
Returns the background image associated with the specified control state.

* **func** **setBackgroundImageForState**(**image**: <strong>[Image](image.md)</strong>, **state**: <strong>[Int](../gravity/types.md)</strong>)
Sets the background image for the control when it is in the specified state.

* **func** **dividerImageForStates**(**leftSegmentState**: <strong><a href="#_enum_ControlState">ControlState</a></strong>, **rightSegmentState**: <strong><a href="#_enum_ControlState">ControlState</a></strong>): <strong>[Image](image.md)</strong> 
Returns the divider image for the given combination of left and right states.

* **func** **setDividerImageForStates**(**image**: <strong>[Image](image.md)</strong>, **leftSegmentState**: <strong><a href="#_enum_ControlState">ControlState</a></strong>, **rightSegmentState**: <strong><a href="#_enum_ControlState">ControlState</a></strong>)
Sets the image to use for the given combination of left and right states.

* **func** **incrementImageForState**(**state**: <strong>[Int](../gravity/types.md)</strong>): <strong>[Image](image.md)</strong> 
Returns the image used for the increment glyph of the control.

* **func** **setIncrementImageForState**(**image**: <strong>[Image](image.md)</strong>, **state**: <strong>[Int](../gravity/types.md)</strong>)
Sets the image to use for the increment glyph of the control.

* **func** **decrementImageForState**(**state**: <strong>[Int](../gravity/types.md)</strong>): <strong>[Image](image.md)</strong> 
Returns the image used for the decrement glyph of the control.

* **func** **setDecrementImageForState**(**image**: <strong>[Image](image.md)</strong>, **state**: <strong>[Int](../gravity/types.md)</strong>)
Sets the image to use for the decrement glyph of the control.

* **func** **animate**(**duration**: <strong>[Float](../gravity/types.md)</strong>, **delay**: <strong>[Float](../gravity/types.md)</strong>, **options**: <strong><a href="#_enum_AnimationOption">AnimationOption</a></strong>, **closure**: <strong>[Closure](../gravity/closures.md)</strong>, **completion**: <strong>[Closure](../gravity/closures.md)</strong>)
Animate changes to one or more views using the specified duration, delay, options and completion handler.

* **func** **setFocus**()
Force focus to be set to the selected control. For TextField and TextView that means force Keyboard to appear.

* **func** **clearFocus**()
Clear focus from selected control

</ul>

</ul>

### Enumeration

### ControlState* .Application
* .Disabled
* .Focused
* .Highlighted
* .Normal
* .Selected
<br><br>### AnimationOption* .AllowAnimatedContent
* .AllowUserInteraction
* .Autoreverse
* .BeginFromCurrentState
* .CurveEaseIn
* .CurveEaseInOut
* .CurveEaseOut
* .CurveLinear
* .LayoutSubviews
* .OverrideInheritedCurve
* .OverrideInheritedDuration
* .OverrideInheritedOptions
* .Repeat
* .ShowHideTransitionViews
* .TransitionCrossDissolve
* .TransitionCurlDown
* .TransitionCurlUp
* .TransitionFlipFromBottom
* .TransitionFlipFromLeft
* .TransitionFlipFromRight
* .TransitionFlipFromTop
* .TransitionNone
<br><br></ul>
