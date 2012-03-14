Description
===========
Easy to use jQuery plugin for zoom & pan image cropping.

Demo
====
Visit: http://www.tmatthew.net/jwindowcrop

Usage
=====
	// mininum
	$('img.crop_me').jWindowCrop();

	// soemthing more realistic
	$('img.crop_me').jWindowCrop({
		targetWidth:300,
		targetHeight:300,
		onChange: function(result) {
			console.log(result);
		}
	});

Options
=======
<table>
	<tr>
		<th>Option</th>
		<th>Default</th>
		<th>Required</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>targetWidth</td>
		<td>320</td>
		<td>no</td>
		<td>Width in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>targetHeight</td>
		<td>180</td>
		<td>no</td>
		<td>Height in pixels of the cropping window</td>
	</tr>
	<tr>
		<td>zoomSteps</td>
		<td>10</td>
		<td>no</td>
		<td>Number of incremental zoop stops. With the default of 10, you have to click the zoom in button 9 times to reach 100%</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>

<table>

Advanced
========

Questions
=========
Email tyler at tmatthew dot net