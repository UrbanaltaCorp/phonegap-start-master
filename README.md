# Hello World PhoneGap Application using bluetoothle plugin

> A Hello World application built with PhoneGap

## Changes from Phonegap Hello World 

Download Hello World project: 
	https://github.com/phonegap/phonegap-start

Modify index.html:
	Delete:  <script type="text/javascript" src="cordova.js"></script>
	Add: <script src="phonegap.js"></script>
	Add: <script type="text/javascript" src="js/bluetoothle.js"></script> before index.js line.
	
Modify index.js:
	Add a call to StartBluetooth() in function onDeviceReady().

Modify config.xml:
Add to 3rd party plugins: 
	<gap:plugin name="com.randdusing.bluetoothle" version="1.0.0" />

Add file bluetoothle.js to the project.  This is nothing more than the example code
by the plugin author with the initialize method called from StartBluetooth().

	function StartBluetooth()
	{
		console.log("starting bluetooth");
		bluetoothle.initialize(initializeSuccess, initializeError);
	}


