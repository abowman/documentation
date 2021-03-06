**super**: **[UIView](UIView.md)** (on iOS)

A Camera object represents a physical capture device and the properties associated with that device. You use a capture device to configure the properties of the underlying hardware. A capture device also provides input data, such as audio or video.

### Events

* **Load**()
This event is called when the object becames available in the current runtime system.

* **WillShow**()
The view is about to be added to the App's views hierarchy.

* **WillHide**()
The view is about to be removed from the App's views hierarchy.

* **Ready**()
This event is triggered when the physical capture device has been configured, the device properites (lensAperture, minExposureDuration, maxExposureDuration, etc) are available and the camera is ready to capture. This event is also called when a new physical capture device is configured, for example after switching between the front and the back camera.

* **DeniedAuthorization**(**cameraAuthorizationType**: **[Int](../gravity/types.md)**)
This event is called when user denied your app permission to user camera and/or microphone.

* **NewImage**(**image**: **[Image](Image.md)**, **metadata**: **[Map](../gravity/map.md)**)
This event is triggered when a new still picture is available.

* **NewVideo**(**videoPath**: **[String](../gravity/types.md)**)
This event is triggered when a new recordered movie is available.

* **RecognizedObjects**(**objects**: **[List](../gravity/list.md)**)
This event is triggered any time the array of recognized metadata objects changes or the position of a recognized object changes. The 'objects' parameter is a List of RecognizedObject.

* **DidShow**()
The view has been added to the App's views hierarchy.

* **DidHide**()
The view has been removed from the App's views hierarchy.

* **Unload**()
This event is called when the object has been removed from the current runtime system (but not yet deallocated).



### Properties

* **var** **cameraQuality**: **CameraQuality**
Current position of a capture device.

* **var** **position**: **CameraPosition**
Current position of a capture device.

* **var** **whiteBalance**: **WhiteBalanceMode**
White balance mode.

* **var** **mirror**: **CameraMirrorMode**
Camera mirror mode.

* **var** **flash**: **CameraFlashMode**
Current flash mode of a capture device. \(read-only\)

* **var** **recording**: **[Bool](../gravity/types.md)**
Boolean value to indicate if the camera is recording a video at the current moment. \(read-only\)

* **var** **isRunning**: **[Bool](../gravity/types.md)**
Boolean value to indicate if the camera session is running. The camera is automatically started if not hidden and added to a visible view hierarchy, otherwise it is stopped. Use the start/stop method to programmatically change the running status. \(read-only\)

* **var** **videoEnabled**: **[Bool](../gravity/types.md)**
Check if video mode is enabled in the capture device.

* **var** **cropImageAsSeen**: **[Bool](../gravity/types.md)**
If set to true then captured Image is cropped usign the exact View size.

* **var** **zoomingEnabled**: **[Bool](../gravity/types.md)**
Boolean value to indicate if zooming is enabled.

* **var** **useDeviceOrientation**: **[Bool](../gravity/types.md)**
Boolean value to indicate whether the orientation of the captured images should be taken from the device orientation (if set to true) or the interface orientation (if set to false).

* **var** **isFlashAvailable**: **[Bool](../gravity/types.md)**
Checks if flash is available.

* **var** **isTorchAvailable**: **[Bool](../gravity/types.md)**
Checks if torch is available.

* **var** **isFrontCameraAvailable**: **[Bool](../gravity/types.md)**
Checks if the front camera is available.

* **var** **isRearCameraAvailable**: **[Bool](../gravity/types.md)**
Checks if the rear camera is available.

* **var** **autoFocusOnTap**: **[Bool](../gravity/types.md)**
Boolean value to indicate if zooming is enabled.

* **var** **autoExposureOnTap**: **[Bool](../gravity/types.md)**
Boolean value to indicate if zooming is enabled.

* **var** **maxScale**: **[Float](../gravity/types.md)**
Maximum scaling factor.

* **var** **lensAperture**: **[Float](../gravity/types.md)**
The value of this property is a float indicating the size (the f number) of the lens diaphragm. This method returns 0.0 if the device is not yet ready (see the Ready event). The Creo simulator for Mac returns 1.8 like the latest iPhone models, not the real lens aperture of the camera on the Mac. \(read-only\)

* **var** **exposureDuration**: **[Float](../gravity/types.md)**
The length of time in seconds over which exposure takes place.

* **var** **minExposureDuration**: **[Float](../gravity/types.md)**
The minimum supported exposure duration. \(read-only\)

* **var** **maxExposureDuration**: **[Float](../gravity/types.md)**
The maximum supported exposure duration. \(read-only\)

* **var** **ISO**: **[Float](../gravity/types.md)**
The current exposure ISO value.

* **var** **minISO**: **[Float](../gravity/types.md)**
The minimum supported exposure ISO value. \(read-only\)

* **var** **maxISO**: **[Float](../gravity/types.md)**
The maximum supported exposure ISO value. \(read-only\)

* **var** **exposureMode**: **CameraExposureMode**
The camera exposure mode.

* **var** **exposurePointOfInterestSupported**: **[Bool](../gravity/types.md)**
Indicates whether the device supports a point of interest for exposure. \(read-only\)

* **var** **exposurePointOfInterest**: **[Point](Point.md)**
The point of interest for exposure. Setting a value for this property does not initiate an exposure rebalancing operation. To set exposure using a point of interest, first set this property's value, then set the exposureMode property to CameraExposureMode.AutoExpose or CameraExposureMode.ContinuousAutoExposure. This property's Point value uses a coordinate system where {0,0} is the top left of the picture area and {1,1} is the bottom right. This coordinate system is always relative to a landscape device orientation with the home button on the right, regardless of the actual device orientation.

* **var** **adjustingExposure**: **[Bool](../gravity/types.md)**
Indicates whether the device is currently adjusting its exposure setting. \(read-only\)

* **var** **exposureTargetOffset**: **[Float](../gravity/types.md)**
The metered exposure level's offset from the target exposure value, in EV units. The Creo simulator for Mac return 0.0. \(read-only\)

* **var** **exposureTargetBias**: **[Float](../gravity/types.md)**
Bias applied to the target exposure value, in EV units. When exposureMode is CameraExposureMode.AutoExpose or CameraExposureMode.Locked, the bias will affect both metering (exposureTargetOffset), and the actual exposure level (exposureDuration and ISO). When the exposure mode is AVCaptureExposureModeCustom, it will only affect metering. The Creo simulator for Mac return 0.0.

* **var** **minExposureTargetBias**: **[Float](../gravity/types.md)**
The minimum supported exposure bias, in EV units. The Creo simulator for Mac return 0.0. \(read-only\)

* **var** **maxExposureTargetBias**: **[Float](../gravity/types.md)**
The maximum supported exposure bias, in EV units. \(read-only\)

* **var** **focusMode**: **CameraFocusMode**
The camera focus mode.

* **var** **focusPointOfInterestSupported**: **[Bool](../gravity/types.md)**
Indicates whether the device supports a point of interest for focus. \(read-only\)

* **var** **focusPointOfInterest**: **[Point](Point.md)**
The point of interest for focusing. Setting a value for this property does not initiate a focusing operation. To focus the camera on a point of interest, first set this property's value, then set the focusMode property to CameraFocusMode.AutoFocus or CameraFocusMode.ContinuousAutoFocus. This property's Point value uses a coordinate system where {0,0} is the top left of the picture area and {1,1} is the bottom right. This coordinate system is always relative to a landscape device orientation with the home button on the right, regardless of the actual device orientation. You can convert between this coordinate system and view coordinates using AVCaptureVideoPreviewLayer methods.

* **var** **adjustingFocus**: **[Bool](../gravity/types.md)**
Indicates whether the device is currently adjusting its focus setting. \(read-only\)

* **var** **autoFocusRangeRestrictionSupported**: **[Bool](../gravity/types.md)**
A Boolean value that indicates whether the device supports focus range restrictions. \(read-only\)

* **var** **autoFocusRangeRestriction**: **CameraAutoFocusRangeRestriction**
A value controlling the allowable range for automatic focusing.

* **var** **smoothAutoFocusSupported**: **[Bool](../gravity/types.md)**
A Boolean value that indicates whether the device supports smooth autofocus. \(read-only\)

* **var** **smoothAutoFocusEnabled**: **[Bool](../gravity/types.md)**
A Boolean value that determines whether smooth autofocus is enabled. On capable devices, you can enable a “smooth” focusing mode in which lens movements are made more slowly. This mode make focus transitions less visually intrusive, a behavior that you may want for video capture.

* **var** **lowLightBoostSupported**: **[Bool](../gravity/types.md)**
A Boolean value that indicates whether the capture device supports boosting images in low light conditions. \(read-only\)

* **var** **lowLightBoostEnabled**: **[Bool](../gravity/types.md)**
A Boolean value that indicates whether the capture device’s low light boost feature is enabled. \(read-only\)

* **var** **automaticallyEnablesLowLightBoostWhenAvailable**: **[Bool](../gravity/types.md)**
A Boolean value that indicates whether the capture device should automatically switch to low light boost mode when necessary.

* **var** **machineReadableObjectTypes**: **MachineReadableObjectType**
A bitmask used to filter the metadata objects reported by the RecognizedObjects event.

* **var** **filters**: **[List](../gravity/list.md)**
A list a ImageFilters to apply to the live Camera preview.

* **var** **objectName**: **[String](../gravity/types.md)**
The name of the object.



### Class Methods

* **func** **exposureString**(**seconds**: **[Float](../gravity/types.md)**): <strong>[String](../gravity/types.md)</strong> 
Return a readable string representation of the exposure value.



### Methods

* **func** **capture**(**onSuccess**: **[Closure](../gravity/closure.md) = null**, **onError**: **[Closure](../gravity/closure.md) = null**)
Initiates a still image capture action.

* **func** **togglePosition**()
Toggle the position of a capture device.

* **func** **toggleFlashMode**(): <strong><a href="#_enum_CameraFlashMode">CameraFlashMode</a></strong> 
Toggle the flash mode of the capture device. Returns the new flash mode.

* **func** **setFlashMode**(**flashMode**: **[Int](../gravity/types.md)**): <strong><a href="#_enum_CameraFlashMode">CameraFlashMode</a></strong> 
Set the flash mode of the capture device. Returns true if the camera supports the new flash mode, false otherwise.

* **func** **startRecording**(**onSuccess**: **[Closure](../gravity/closure.md) = null**, **onError**: **[Closure](../gravity/closure.md) = null**)
Start recording a video.

* **func** **stopRecording**()
Stop recording a video.

* **func** **start**()
Starts running the camera session.

* **func** **stop**()
Stops running the camera session.

* **func** **animate**(**duration**: **[Float](../gravity/types.md)**, **delay**: **[Float](../gravity/types.md)**, **options**: **<a href="#_enum_AnimationOption">AnimationOption</a>**, **closure**: **[Closure](../gravity/closure.md)**, **completion**: **[Closure](../gravity/closure.md)**)
Animate changes to one or more views using the specified duration, delay, options and completion handler.

* **func** **setFocus**()
Force focus to be set to the selected control. For TextField and TextView that means force Keyboard to appear.

* **func** **clearFocus**()
Clear focus from selected control





### Enumeration

#### CameraQuality
 * .High
 * .Low
 * .Medium
 * .Photo
 * .cif352x288
 * .hd1280x720
 * .hd1920x1080
 * .hd4K3840x2160
 * .iFrame1280x720
 * .iFrame960x540
 * .vga640x480

#### CameraPosition
 * .Front
 * .Rear

#### WhiteBalanceMode
 * .Auto
 * .Continuous
 * .Locked

#### CameraMirrorMode
 * .Auto
 * .Off
 * .On

#### CameraFlashMode
 * .Auto
 * .Off
 * .On

#### CameraExposureMode
 * .AutoFocus
 * .ContinuousAutoExposure
 * .Custom
 * .Locked

#### CameraFocusMode
 * .AutoFocus
 * .ContinuousAutoFocus
 * .Locked

#### CameraAutoFocusRangeRestriction
 * .Far
 * .Near
 * .None

#### MachineReadableObjectType
 * .AztecCode
 * .Code128Code
 * .Code39Code
 * .Code39Mod43Code
 * .Code93Code
 * .DataMatrixCode
 * .EAN13Code
 * .EAN8Code
 * .ITF14Code
 * .Interleaved2of5Code
 * .PDF417Code
 * .QRCode
 * .UPCECode

#### AnimationOption
 * .AllowAnimatedContent
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



