# PageSplit

**super**: [UISplitViewController](UISplitViewController.md) on iOS

The SplitView class is a container that presents a master-detail interface. In a master-detail interface, changes in the master window drive changes in the detail window. The two windows can be arranged so that they are side-by-side, so that only one at a time is visible, or so that one only partially hides the other. You can use the SplitView class on all devices. When building your app’s user interface, the split view  is typically the root container of your app. The split view has no significant appearance of its own. Most of its appearance is defined by the child windows you set.

### Events

* **Load**()
This event is called when the object becames available in the current runtime system.

* **WillShow**()
Use this event to be notified when navigation is about to be added to a view hierarchy.

* **DidShow**()
Use this event to be notified when navigation was added to a view hierarchy.

* **WillHide**()
Use this event to be notified when navigation is about to be removed from a view hierarchy.

* **DidHide**()
Use this event to be notified when navigation was removed from a view hierarchy.

* **Unload**()
This event is called when the object has been removed from the current runtime system (but not yet deallocated).

</ul>

### Properties

* **var** **bounds**: **[Rect](rect.md)**
The bounds rectangle, which describes the view’s location and size in its own coordinate system.

* **var** **frame**: **[Rect](rect.md)**
The frame rectangle, which describes the view’s location and size in its superview’s coordinate system.

* **var** **statusBarVisibility**: **StatusBarVisibility**
A value indicating whether the status bar should be visible.

* **var** **statusBarStyle**: **StatusBarStyle**
The style of the status bar.

* **var** **windows**: **[List](../gravity/lists.md)**
Array of windows currently managed by the navigation.

* **var** **selectedWindow**: **[Window](window.md) or [Navigation](navigation.md)**
Current Window in the details view. If the Window does not exit in the view hierarchy then it is automatically added.

* **var** **collapsed**: **[Bool](../gravity/types.md)**
A Boolean value indicating whether only one of the child view controllers is displayed. \(read-only\)

* **var** **preferredDisplayMode**: **SplitViewDisplayMode**
The preferred arrangement of the split view controller interface.

* **var** **displayMode**: **SplitViewDisplayMode**
The current arrangement of the split view controller’s contents. \(read-only\)

* **var** **preferredPrimaryColumnWidthFraction**: **[Float](../gravity/types.md)**
The relative width of the primary view controller’s content.

* **var** **minimumPrimaryColumnWidth**: **[Float](../gravity/types.md)**
The minimum width (in points) required for the primary view controller’s content.

* **var** **maximumPrimaryColumnWidth**: **[Float](../gravity/types.md)**
The maximum width (in points) allowed for the primary view controller’s content.

* **var** **primaryColumnWidth**: **[Float](../gravity/types.md)**
The width (in points) of the primary view controller’s content. \(read-only\)

</ul>

### Methods

* **func** **open**(**completion**: <strong>[Closure](../gravity/closures.md) = null</strong>)
Open window in currently displayed window or navigation using the destination object default behaviour.

* **func** **openIn**(**window**: <strong>[Window](window.md) or [Navigation](navigation.md)</strong>, **completion**: <strong>[Closure](../gravity/closures.md) = null</strong>)
<pre><code class="swift">TargetWindow.openIn(ContainerWindow);</code></pre>
Open callee object (TargetWindow) inside parameter object (ContainerWindow) using its default behaviour. Note that TargetWindow and/or ContainerWindow can be a Window or a Navigation.

* **func** **openDetailWindowAtIndex**(**index**: <strong>[Int](../gravity/types.md)</strong>)
Open the detail window of the PageSplit at the specified index. The first window inside a PageSplit is used as the <i>master</i> window, the next window(s) will be used as <i>detail</i> window(s). If the PageSplit has more than one detail window then this method opens the window at the specified index from the array of configured windows (skipping the first <i>master</i> window). If the PageSplit is configured with two subwindows - one master and one details - this method opens the detail window and set the value of the <i>index</i> parameter to the <i>rowIndex</i> property of the first custom <i>View</i> inside the detail window.

* **func** **openModal**(**TransitionStyle**: <strong><a href="#_enum_TransitionStyle">TransitionStyle</a></strong>, **completion**: <strong>[Closure](../gravity/closures.md) = null</strong>)
Open window modally usign the specified transition style.

* **func** **close**()
Close window if modally opened.

</ul>

</ul>

### Enumeration

### StatusBarVisibility* .Default
* .Hidden
* .Visible
<br><br>### StatusBarStyle* .DarkContent
* .Default
* .LightContent
<br><br>### SplitViewDisplayMode* .AllVisible
* .Automatic
* .PrimaryHidden
* .PrimaryOverlay
<br><br>### TransitionStyle* .Cards
* .CoverVertical
* .CrossDissolve
* .Crossfade
* .Cube
* .Default
* .Explode
* .Flip
* .FlipHorizontal
* .Fold
* .NatGeo
* .NotAnimated
* .PartialCurl
* .Portal
* .Turn
<br><br></ul>
