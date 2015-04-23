<br><br>
Hi! We're not actively developing the tryplex toolkit at the moment, nor is it tested for ML 10.8.<br>
If you want to use the kinect with Quartz Composer, we recommend <a href='http://www.ni-mate.com'>http://www.ni-mate.com</a>. It's easy to use, and parts of this toolkit will still work with the ni-mate quick-fix.<br><br>
Also, all the macro patches are completely open, so easily adaptable for your needs, and good learning material if you intent to work with the data ni-mate sends.<br><br>

<br><br>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=nWiKojvULcA' target='_blank'><img src='http://img.youtube.com/vi/nWiKojvULcA/0.jpg' width='425' height=344 /></a><br>
<br><br>
<b>Tryplex Kinect Toolkit NI mate quick fix for Quartz Composer</b><br>
For people who want to play around with NI mate and QC/tryplex, there's a quick fix. It supports one user only.<br>
We're currently adapting the full tryplex package to NI mate, so this for testing purposes only.<br>
Find it under the downloads.<br>
<br>
<br><br>
<b>This is the 0.222 version of the tryplex toolkit.</b><br>
The tryplex toolkit is a set of macro patches for Quartz Composer that makes Kinect skeleton tracking more accessible. All patches are open source. A lot of samples are provided, as well as a puppet-tool and a skeleton recorder.<br><br>
Please share your results!<br>
<br><br>
<h3>NEW</h3>
Synapse support (<a href='http://synapsekinect.tumblr.com'>http://synapsekinect.tumblr.com</a>)<br>
Gives the ability to track one skeleton and show the depth image.<br>
<ul><li>Added Synapse 1.1 to the package<br>
</li><li>Macro patch '01s_Kinect Skeleton Synapse to SkeletonStruct' gets and tranlates OSC data from Synapse to Tryplex.<br>
</li><li>Macro patch '01s_Kinect Skeleton Synapse settings' keeps the Synapse OSC connection alive, and lets you adjust  the depth image settings.<br>
</li><li>Macro patch '01s_Kinect Skeleton World coordinate', get's the realworld coordinates measured in millimeters from the sensor.<br>
</li><li>Added 'macros sample compositions Synapse' folder with Sample patches for Synapse.<br>
</li><li>Included all QC plug-ins needed for Tryplex.<br>
</li><li>Bugfix in the skeleton recorder<br>
</li><li>Added a universal build of the Synapse kinect plugin<br>
</li><li>Added qcOSC 0.6<br>
<br><br>
<h3>UPGRADING</h3>
If you have an existing 0.21 installation you can maintain your current setup. Only add the macro's  '01s_Kinect Skeleton Synapse to SkeletonStruct', '01s_Kinect Skeleton Synapse settings' and '01s_Kinect Skeleton World coordinate' to your /library/graphics/Quartz Composer Patches/ folder, and install the Synapse Kinect plug-in from QC Plug-ins/Quartz Composer Plug-Ins in the Quartz Composer Plug-Ins folder in Library/Graphics/ folder.<br>
Replace the skeleton recorder with this version.</li></ul>

If you already used Synapse; the Max patch is not needed to use Synapse in QC with Tryplex.<br>
<br>
<br><br>
Tutorial page on the <a href='bodybuilder.md'>bodybuilder app</a>
<hr />
<h2><b><a href='http://code.google.com/p/tryplex/downloads'>download the toolkit</a></h2>
<hr />
<h2><a href='Installation.md'>installation guide</a></h2>
<hr />
<h2>Check out the <a href='Gallery.md'>gallery</a> to see what people made with tryplex!</h2>
<hr />
<h2>Please share your improvements, results, problems, ideas and suggestions in our</b> <a href='http://groups.google.com/group/tryplex-toolkit'>discussion group!</a></h2>
<hr />

If you want to add a feature request, or have an interesting idea use the <a href='http://code.google.com/p/tryplex/issues/list'>Issues</a> tab to add one!<br /><br />

<b>Credits</b><br /><br />
<a href='http://www.oneseconds.com'><img src='http://www.oneseconds.com/assets/site_images/oneseconds_logo_small.gif' /></a><br><a href='http://www.oneseconds.com/'>oneseconds</a>, (Sebastian Kox) developer/interaction design of the Tryplex Quartz Composer toolkit.<br />
With help from Mischa Schaub & Stephan Urech from <a href='http://hyperwerk.ch/'> Hyperwerk Institute for Postindustrial Design</a>, Interaction Design<br />
<a href='http://www.kineme.net/'>kineme.net</a> for their plug-ins and everyone posting sharing and helping.<br />
Sensebloom for their OSCeleton <a href='https://github.com/Sensebloom/OSCeleton'>https://github.com/Sensebloom/OSCeleton</a><br />
Synapse (Ryan Challinor), <a href='http://synapsekinect.tumblr.com'>http://synapsekinect.tumblr.com</a><br />