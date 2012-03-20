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
		<td>targetWidth</td><td>integer</td><td>320</td><td>no</td><td>Width in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>targetHeight</td><td>integer</td><td>180</td><td>no</td><td>Height in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>zoomSteps</td><td>integer</td><td>10</td><td>no</td><td>Number of incremental zoop stops. With the default of 10, you have to click the zoom in button 9 times to reach 100%</td>
	</tr>
	<tr>
		<td>onChange</td><td>function</td><td>function(){}</td><td>no</td><td>Callback function that gets called whenever the values change. cropX, cropY, cropW, and cropH values are passed to this function in a hash. Use the this keyword in the function for a reference the element that was updated.</td>
	</tr>
<table>

Advanced
========
The structure for this plugin comes from http://starter.pixelgraphics.us/. An object is created for each dom element this is initialized on. A reverse refernce to that object can be accessed like so:

	var jwc = $('img#beach').getjWindowCrop();

You then have access to all the properties and methods used for that specific element.

Questions
=========
Email tyler at tmatthew dot net