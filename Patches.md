# The Quartz Composer Patches #


---

## Kinect Skeleton OSC to SkeletonStruct ##
![http://www.oneseconds.com/dev/images/OSCtostruct.jpg](http://www.oneseconds.com/dev/images/OSCtostruct.jpg)
<br><br>
Receives the OSC data and makes the SkeletonStruct.<br>
<hr />
<h2>Kinect Skeleton Stickman</h2>
<img src='http://www.oneseconds.com/dev/images/stickman.jpg' />
<br><br>
This renders a standart stickman figure with the SkeletonStruct as input. You can change color, bone thickness and userID<br>
<hr />
<h2>Kinect Skeleton Get Element</h2>
<img src='http://www.oneseconds.com/dev/images/getelement.jpg' />
<br><br>
Outputs a XYZ value for the given element from a skeleton with the set UserID.<br>
<hr />
<h2>Kinect Skeleton Labels</h2>
<img src='http://www.oneseconds.com/dev/images/skeletonlabels.jpg' />
<br><br>
Shows the labels for each skeleton element. It's feeded by the SkeletonStruct and you can set the UserID<br>
<hr />
<h2>Kinect Skeleton Mid, Rot and distance from elements</h2>
<img src='http://www.oneseconds.com/dev/images/midrotwidth.jpg' />
<br><br>
Outputs the Middle point, rotation and distance from two given points<br>
<hr />
<h2>Kinect Skeleton Active Players</h2>
<img src='http://www.oneseconds.com/dev/images/activeplayers.jpg' />
<br><br>
This patch receives the OSC information and generates a structure (array) that contains the player's data<br>
<hr />
<h2>Kinect Skeleton Hit Test</h2>
<img src='http://www.oneseconds.com/dev/images/hittest.jpg' />
<br><br>
Generates a hit test result from a XYZ/Width Height Depth input. Also forwards XYZ Width Height Depth for the hit object.<br>
<hr />
<h2>Kinect Skeleton Multiple Hit Test</h2>
<img src='http://www.oneseconds.com/dev/images/multiplehit.jpg' />
<br><br>
Generates a Hit test result and userID, from a given element.<br>
<hr />
<h2>Kinect Skeleton Acceleration Values</h2>
<img src='http://www.oneseconds.com/dev/images/accelerationvalues.jpg' />
<br><br>
Outputs the acceleration values for a given element.<br>
<hr />
<h2>Kinect Skeleton Gesture Hands Together</h2>
<img src='http://www.oneseconds.com/dev/images/gesturehandstogether.jpg' />
<br><br>
Checks if the hands are together. You can set a tolerance value.<br>
<hr />
<h2>Kinect Skeleton Gesture Hands Above Head</h2>
<img src='http://www.oneseconds.com/dev/images/gesturehandsabovehead.jpg' />
<br><br>
Checks if the hands are above the head.<br>
<hr />
<h2>Kinect Skeleton Gesture Stretch Arms</h2>
<img src='http://www.oneseconds.com/dev/images/gesturestretcharms.jpg' />
<br><br>
Detects if the arms are stretched towards the kinect camera.<br>
<hr />