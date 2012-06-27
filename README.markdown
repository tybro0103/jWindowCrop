Description
===========
Easy to use jQuery plugin for zoom & pan image cropping.

Demo
====
Visit: http://www.tmatthew.net/jwindowcrop

Usage
=====
	// minimum
	$('img.crop_me').jWindowCrop();

	// typical
	$('img.crop_me').jWindowCrop({
		targetWidth:300,
		targetHeight:300,
		onChange: function(result) {
			console.log($(this).attr('id'));
			console.log('x: '+result.cropX);
		}
	});

Options
=======
<table>
	<tr>
		<th>Option</th>
		<th>Type</th>
		<th>Default</th>
		<th>Required</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>targetWidth</td><td>integer</td><td>320</td><td>no</td>
		<td>Width in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>targetHeight</td><td>integer</td><td>180</td><td>no</td>
		<td>Height in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>cropX / cropY</td><td>integer</td><td>null</td><td>no</td>
		<td>Specifies the initial start position. If you've previously stored the results of JWC you can set these values (along with  cropH and cropW) to what they were in order to continue where you left off. You must specify both cropX and cropY to use this feature (and it won't make much sense without cropW and cropH).</td>
	</tr>
	<tr>
		<td>cropW / cropH</td><td>integer</td><td>null</td><td>no</td>
		<td>Specifies the initial zoom level. If you've previously stored the results of JWC you can set these values (along with  cropX and cropY) to what they were in order to continue where you left off. You must specify both cropW and cropH to use this feature (and it won't make much sense without cropX and cropY)</td>
	</tr>
	<tr>
		<td>onChange</td><td>function</td><td>function(){}</td><td>no</td>
		<td>Callback function that gets called whenever the values change. cropX, cropY, cropW, cropH, mustStretch (boolean) values are passed to this function in a hash. Use the this keyword in the function for a reference to the element that was updated.</td>
	</tr>
	<tr>
		<td>zoomSteps</td><td>integer</td><td>10</td><td>no</td>
		<td>Number of incremental zoom steps. With the default of 10, you have to click the zoom-in button 9 times to reach 100%.</td>
	</tr>
	<tr>
		<td>loadingText</td><td>string</td><td>"Loading..."</td><td>no</td>
		<td>Text (can be HTML) to display within frame until image is loaded.</td>
	</tr>
	<tr>
		<td>smartControls</td><td>boolean</td><td>true</td><td>no</td>
		<td>If true, controls will hide on mouseleave and appear on mouseenter.</td>
	</tr>
	<tr>
		<td>showControlsOnStart</td><td>boolean</td><td>true</td><td>no</td>
		<td>If true, controls will be hidden on start. Note: Do not set both this and smartControls to false.</td>
	</tr>
</table>

Methods
======
<table>
	<tr>
		<th>Method</th>
		<th>Return</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>reset()</td><td>void</td>
		<td>Re-initializes the cropping area, including re-zooming and re-centering the image, and adjusting the canvas size to the new values in options.targetWidth and options.targetHeight (if changed).</td>
	</tr>
</table>

Advanced
========
The structure for this plugin comes from http://starter.pixelgraphics.us/. An object is created for each dom element jWindowCrop is initialized on. A reverse reference to that object can be accessed like so:

	var jwc = $('img#beach').getjWindowCrop();

You then have access to all the properties and methods used for that specific element.

Questions
=========
Email tyler at tmatthew dot net
