---
title: 
layout: 
description: 
image: " "
map:
  latitude: 
  longitude: 
  address: " "
  zoom: 
published: false
---
<div class="map" id="map"></div>

<section class="testimonial">
		<div class="container flex">
			<div class="testimonial-block">
				<blockquote>
					<p class="editable">Quote text to go here.</p>
					<p class="profile_author">Name of the person quoted</p>
					<p>Mayor</p>
				</blockquote>
			</div>
		</div>
	</section>

## First heading

Body content 

![alt text](/images/imageName.png "Image Name")

## Second heading 

Body content 

<script type="text/javascript">
	window.mapData = {{ page.map | jsonify }};

	function initMap() {
		var myOptions = {
			scrollwheel: false,
			draggable: false,
			panControl: false,
			disableDefaultUI: true,
			zoom: window.mapData.zoom,
			maxZoom: window.mapData.zoom,
			minZoom: window.mapData.zoom,
			center: new google.maps.LatLng(window.mapData.latitude, window.mapData.longitude),
			mapTypeId: google.maps.MapTypeId.ROADMAP
		};
		map = new google.maps.Map(document.getElementById("map"), myOptions);
		marker = new google.maps.Marker({
			map: map,
			position: new google.maps.LatLng(window.mapData.latitude, window.mapData.longitude)
		});

		google.maps.event.addDomListener(window, "resize", function () {
			map.setCenter(myOptions.center);
		});
	}
</script>

<script async defer src="https://maps.googleapis.com/maps/api/js?key={{ site.google_maps_javascript_api_key }}&amp;callback=initMap"></script>
