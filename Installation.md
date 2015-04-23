There are two ways to use the tryplex toolkit. With Synapse you're able to get it running within a few minutes. If you like to use OSCeleton, the installation procedure takes about two hours to complete.
<br><br>
<h3>Synapse</h3>
<ul><li>Single skeleton tracking<br>
</li><li>Depth image<br>
</li><li>Works without installing drivers etc.</li></ul>


<h3>OSCeleton</h3>
<ul><li>Track up to 6 users<br>
</li><li>Lower cpu usage<br>
</li><li>Is a bit more responsive<br>
<br><br><br><br>
<hr />
<h1>Running tryplex with Synapse</h1></li></ul>

<ul><li>Place the plugins from 'QC Plug-ins/Quartz Composer Plug-Ins' in your '/Library/Graphics/Quartz Composer Plug-Ins' folder<br>
</li><li>Place the plugins from 'QC Plug-ins/Quartz Composer Patches' in your '/Library/Graphics/Quartz Composer Patches' folder<br>
</li><li>If these folders don't exist, make them<br>
</li><li>To install the macro's in your library place them in the /library/graphics/Quartz Composer Patches/ folder.<br>
</li><li>Connect your Kinect, and run Synapse from the 'Synapse' folder.<br>
</li><li>Open and run '01_01s single skeleton.qtz' from the 'QC/ macros sample compositions Synapse' folder.<br>
</li><li>Stand and hold in the cactus position to calibrate.<br><br>
<img src='http://www.oneseconds.com/dev/images/calibrationpose.png' /><br><br>
<hr />
<br><br><br><br>
<b><i>NOTE: this installation guide is probably outdated.<br>
Check <a href='http://www.codingcolor.com/featured-articles/set-up-kinect-on-osx-10-8-mountain-lion/'>http://www.codingcolor.com/featured-articles/set-up-kinect-on-osx-10-8-mountain-lion/</a> for a more up to date guide!</i></b>
<br><br><br><br></li></ul>

<h1>Insalling for use with OSCeleton</h1>
<h1>Installing Xcode, Libtool, Macports, LibUSB, OpenNI, primesense NITE, avin2/sensorkinect, qcOSC</h1>


This is the fast route to install OSCeleton to use with Quartz Composer.<br><br>
We did our best to document it, at the bottom of this page you'll find common error's people encountered. Note that this is quite a tedious operation, it takes some time and patience. Previous installs of kinect/openNI related software could influence the success rate of a installation, so preferably use a clean system with only Xcode and Snow Leopard. Start only if you have some basic knowledge of using the terminal and Quartz Composer.<br><br>
Things definitely will get easier in the future, but for now it's all new and still in development by a lot of parties.<br><br>

The installation should take 1 or 2 hours to complete.<br>
For this to work I've used the processing sample to reroute the osc messages into a format that quartz could read.<br>
In this setup I'm still using the 11/1/2010 build of OSCeleton, it seems to be the most reliable version for osx at the moment. There's a <a href='https://github.com/Sensebloom/OSCeleton'>newer version</a> (with QC OSC support!) but I still get segmentation errors sometimes and jerky knee/feet data with that version. When there's a more stable build of OSCeleton I'll update this page and the source.<br>
<br><br>
<h2>Step 1 - Xcode</h2>
<b>Download and install this:</b><br>
Xcode (get a membership first, it's free)<br>
<a href='http://developer.apple.com/devcenter/mac/index.action'><a href='http://developer.apple.com/devcenter/mac/index.action'>http://developer.apple.com/devcenter/mac/index.action</a></a><br>
<a href='https://developer.apple.com/ios/download.action?path=/ios/ios_sdk_4.2__final/xcode_3.2.5_and_ios_sdk_4.2_final.dmg'><a href='https://developer.apple.com/ios/download.action?path=/ios/ios_sdk_4.2__final/xcode_3.2.5_and_ios_sdk_4.2_final.dmg'>https://developer.apple.com/ios/download.action?path=/ios/ios_sdk_4.2__final/xcode_3.2.5_and_ios_sdk_4.2_final.dmg</a></a><br><br>
<b>NOTE: Xcode 4 is only free when you are enlisted in the developer program, else available for $4.99 in the app store. The Xcode 3.2.5 download link provided still works if you register at the developer page without a paid subscription.</b>

<br><br>
<h2>Step 2 - Macports</h2>
<b>Macports</b><br>
<a href='http://distfiles.macports.org/MacPorts/MacPorts-1.9.2-10.6-SnowLeopard.dmg'><a href='http://distfiles.macports.org/MacPorts/MacPorts-1.9.2-10.6-SnowLeopard.dmg'>http://distfiles.macports.org/MacPorts/MacPorts-1.9.2-10.6-SnowLeopard.dmg</a></a>

<br><br>
<h2>Step 3 - Libtool</h2>
<b>Libtool</b><br>
open the terminal and type:<br>
sudo port install libtool<br>
and press enter<br>
<img src='http://www.oneseconds.com/dev/images/libtool.png' /> <br><br>

if it doesn't work, restart your terminal program and try again<br>
<br>
If during the install it gives this error:<br>
Error: db46 requires the Java for Mac OS X development headers.<br>
Error: Download the Java Developer Package from:<br>
Error: Target org.macports.configure returned: missing Java headers<br>
Error: Failed to install db46<br><br>
<b>Then Install this package first:</b><br>
<a href='https://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wa/getSoftware?bundleID=20719'><a href='https://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wa/getSoftware?bundleID=20719'>https://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wa/getSoftware?bundleID=20719</a></a><br>
The latest OSX doesn't include the Java for Mac OS X development headers annymore standard.<br>
<br><br>

<h2>Step 4 - LibUSB</h2>
<b>LibUSB</b><br>
In the terminal type:<br>
sudo port install libusb-devel +universal<br>
and press enter<br>
<img src='http://www.oneseconds.com/dev/images/libusb.png' /><br>
<br><br>

<b>Important note: Put the following installation files (openNI, NITE and avin2/sensorkinect) inside a folder that doesn't contain spaces or weird characters, else it'll generate errors during installation! Leave the folder names of openNI, NITE and avin2/sensorkinect intact.</b><br><br>

<h2>Step 5 - OpenNI</h2>
<b>Download the 'OpenNI Unstable Build for MacOSX 10.6 Universal x86/x64 (32/64-bit)' from:</b> <a href='http://www.openni.org/downloadfiles/opennimodules/openni-binaries/20-latest-unstable'><a href='http://www.openni.org/downloadfiles/opennimodules/openni-binaries/20-latest-unstable'>http://www.openni.org/downloadfiles/opennimodules/openni-binaries/20-latest-unstable</a></a> and expand the files.<br>
<img src='http://www.oneseconds.com/dev/images/openni.png' />
<br>
<br>
In the terminal go to the OpenNI directory (the easy way: type 'cd ' and drag and drop the directory from the finder and press enter) and type: sudo sh install.sh<br>
and press enter<br><br>

<h2>Step 6 - PrimeSense NITE</h2>
<b>Download the 'PrimeSense NITE Unstable Build for for MacOSX 10.6 Universal x86/x64 (32/64-bit)' from:</b> <a href='http://www.openni.org/downloadfiles/opennimodules/openni-compliant-middleware-binaries/33-latest-unstable'><a href='http://www.openni.org/downloadfiles/opennimodules/openni-compliant-middleware-binaries/33-latest-unstable'>http://www.openni.org/downloadfiles/opennimodules/openni-compliant-middleware-binaries/33-latest-unstable</a></a> and expand the files.<br>
<img src='http://www.oneseconds.com/dev/images/primesense.png' />

<br><br>
Now in the terminal go to the NITE directory (the easy way: type 'cd ' and drag and drop the directory from the finder and press enter) and type:<br>
sudo sh install.sh<br>
and press enter<br>
use <b><code>0KOIk2JeIBYClPWVnMoRKn5cdY4=</code></b> as licence key (and yes, include the '=' sign!)<br><br>

<h2>Step 7 - avin2/sensorkinect</h2>
<b>Download the avin2/sensorkinect drivers at:</b><br>
<a href='https://github.com/avin2/SensorKinect'><a href='https://github.com/avin2/SensorKinect'>https://github.com/avin2/SensorKinect</a></a> and expand the files.<br>
Navigate to the avin2/bin folder and expand the 'SensorKinect-Bin-MacOSX-v5.0.3.4.tar.bz2' file.<br>
In the terminal, go to the avin2/bin/SensorKinect-Bin-MacOSX-v5.0.3.4 folder and type:<br>
sudo sh install.sh<br>
<blockquote><br><br></blockquote>

<h2>Step 8 - qcOSC/kineme structure maker</h2>

Place the plugins from 'QC Plug-ins/Quartz Composer Plug-Ins' in your '/Library/Graphics/Quartz Composer Plug-Ins' folder<br><br>
Place the plugins from 'QC Plug-ins/Quartz Composer Patches' in your '/Library/Graphics/Quartz Composer Patches' folder<br><br>
If these folders don't exist, make them<br><br>

If you've completed installation procedure, and it's working it's time to play!<br><br>

<hr />
<h1>Running</h1>

First of all, <b>Quartz Composer should be in 32-bit mode</b>. To do this, locate the Quartz Composer app in the Developer/Applications folder and press CMD+I when selected. Now select 32-bit mode.<br>
<br>
<img src='http://www.oneseconds.com/dev/images/32bit.png' />

<b>To run</b><br>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=i5QhYgUh6ck' target='_blank'><img src='http://img.youtube.com/vi/i5QhYgUh6ck/0.jpg' width='425' height=344 /></a><br>
<br>
Connect the kinect<br>
Open a terminal window and drag and drop osceleton from the 'OSCeleton and sendOSC' folder in the tryplex toolkit to the terminal window <b>(opening from the finder doesn't work!!)</b> and press enter<br>
<br>
<br><br>
Start the  application sendosc from the 'OSCeleton and sendOSC' folder in the tryplex toolkit by double clicking<br><br>
open '01 01s_single_skeleton' from the 'QC' folder in quartz composer<br><br>
<img src='http://www.oneseconds.com/dev/images/calibrationpose.png' /><br><br>
To calibrate the kinect should have a clear view and you have to stand in front of it with both arms stretched and the upper-arms at 90 degrees. After a second or so it should work and you can move freely!<br>
If it fails, reposition yourself a bit more to the front/back/left and try again<br><br>

It's best to open en play around with the examples in the numbered order, so you'll get an idea of how all patches work.<br><br>

To install the macro's in your library place them in the /library/graphics/Quartz Composer Patches/ folder. Quit and restart QC to activate them.<br><br>


QCosc can't open the same port twice so when you open a second composition it gives an error: 'Error opening socket on specified port. Please choose a different port.'.<br>
Quit and restart QC and open the composition again, and it'll work. Once a new version of OSCeleton will be around this error will be gone.<br>
<br><br><br>

<h1>For questions, error's suggestions, please report to the <a href='http://groups.google.com/group/tryplex-toolkit'>discussion group!</a>.</h1>
<br><br><br>
<hr />
<h1>Common errors people encountered</h1>

<img src='http://www.oneseconds.com/dev/images/portproblem.jpg' /><br><br>
<b>Error on opening socket at specified port</b><br>
qcOSC can't open two the same OSC ports at one time. This happens when you open a second composition with the OSC receiver in it. To fix quit and restart QC, and open one composition at the same time.<br><br>


<b>Segmentation fault</b><br>
either you're using the latest osceleton build (this error pops up now and then, but in between it works). Or the camera is used by another application, close any open programs and the terminal, disconnect and reconect the kinect. If it still fails, try reinstalling from the begin.<br>
<br><br>

<b>Image not found/bus error</b><br>
Maybe the camera is used by another application, close any open programs and the termincal, disconnect and reconnect the kinect. Or libusb is not installed (correctly) uninstall and reinstall by opening a new terminal window and type: sudo port uninstall libusb-devel and then:<br>
sudo port install libusb-devel +universal<br>
Restart your terminal program and try again. If it still fails, try reinstalling from the begin.<br><br>

<b>Quartz composer closes/crashes when opening an example</b><br>
Maybe Quartz isn't in 32-bit mode yet. Locate the Quartz Composer app in the Developer/Applications folder and press CMD+I when selected. Now select 32-bit mode.<br><br>

<b>During installation: Command not found, No such file directory</b><br>
and when trying to run:<br>
Library not loaded: ../../Bin/Release/libOpenNI.dylib<br>
Referenced from: /Users/blumBlum/Desktop/OPENNI_FOR_QUARTZ/OSCeleton<br>
QC toolkit v0.1/OSCeleton and sendOSC/osceleton.app<br>
Reason: image not found<br>
Trace/BPT trap<br>
Check if the OpenNI/Nite/avin2 installation files you downloaded are nested in a directory with spaces. If they are, put them in a folder without any spaces or unusual characters and repeat the installation procedure.<br><br>

<b>"StructureTools.plugin" is not a valid Quartz Composer plug-in etc.</b><br>
If you get something like this:<br><br>

QCPlugIn: Bundle at path "/Library/Graphics/Quartz Composer Plug-Ins/<br>
StructureTools.plugin" is not a valid Quartz Composer plug-in<br>

<QCNodeManager | namespace = "com.apple.QuartzComposer" | 410 nodes>:<br>
Patch with name "StructureMaker:KinemeNamedStructureMaker" is missing<br>

Macro Patch<br>
Cannot create node of class "StructureMaker" and identifier<br>
"KinemeNamedStructureMaker"<br><br>

The Structuremaker plugin is either not there or at the wrong place.<br>
The Structure maker plug in should be in the /Library/Graphics/Quartz Composer Patches folder<br>
If that folder doesn't exist, make it and place it there.<br>