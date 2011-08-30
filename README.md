WKShake
=======================================

A custom 'shake' event plugin for mobile web browsers using device accelerometer.

Note: this plugin relies on having access to device accelerometer via DeviceMotion API:

http://dev.w3.org/geo/api/spec-source-orientation

Usage
---------------------------------------

First, include the main JavaScript file in the &lt;head&gt; of your HTML document:

	<script type="text/javascript" src="WKShake.js" ></script>

Next, include the following script just before the end &lt;/body&gt; tag in your HTML to create a new instance of the plugin. Put your own code within the shakeEventDidOccur() method for what you want to happen when a shake event occurs.

	<script type="text/javascript"> 
	window.onload = function() {

		//create a new instance of WKShake.
		var myShakeEvent = new WKShake();

		//start listening for shake event. 
		//you can also use stop() to stop listening.
		myShakeEvent.start();
	
		//define a custom method to fire when shake occurs.
		myShakeEvent.shakeEventDidOccur = function() {
	
			//put your own code here etc.
			if (confirm("Undo?")) {

			}
		}
	};
	</script>
	
License
---------------------------------------

Copyright (c) 2009-2011 Alex Gibson

http://miniapps.co.uk/

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction except as noted below, including without limitation the rights to use, copy, modify, merge, publish, distribute, and/or sublicense, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE