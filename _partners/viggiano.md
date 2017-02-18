---
title: Viggiano city – Italy
layout: partners
country: Italy
website: www.comuneviggiano.it/
Size: 89.70 sq km
Population:
- year: 2011
- total: 3122
Hazards: Cold Wave, Drought, Earthquake, Heat Wave, Land Slide, NBC - Nuclear, Biological,
  Chemical, Technical Disaster
description: The Municipal Civil Protection Plan is in preparation. Localized structural
  and non-structural interventions for Disaster Risk Reduction. Insights are provided
  by the LGSAT.
image: "/images/viggiano.png"
map:
  latitude: 40.353866
  longitude: 15.8961315
  address: " Viggiano – Italy"
  zoom: 7
---

<div class="map" id="map"></div>

<section class="testimonial">
		<div class="container flex">
			<div class="testimonial-block">
				<blockquote>
					<p class="editable">I wish to be fully engaged in developing environmental sustainability and territorial safety in the urban and land-use government actions. To this aim, our community will actively participate with the Province of Potenza in the action proposed for strengthening territorial resilience by adopting local policies and specific actions.</p>
					<p class="profile_author">Amedeo Cicala</p>
					<p>Mayor</p>
				</blockquote>
			</div>
		</div>
</section>

## HAZARD AND VULNERABILITY PROFILE 
Prevailing hazards and vulnerable conditions of the provincial territory: Several areas prone to hydrogeological hazards; Presence of some industrial activities prone to “major accident” hazard; Presence of plants and industrial activities with particular territorial impact; Municipality classified in seismic zone 1 in relation to the 2012 Italian seismic classification for Municipalities; Seismic Vulnerability of the buildings, especially in the historical centres of the municipalities; Widespread presence of soil-sailing phenomena; Phenomena of abandonment of land resulting in settlements very exposed to seismic and hydrogeological risks.

![alt text](/images/viggiano.png "Viggiano – Italy")

## DISASTER AND RISK REDUCTION ACTIVITIES 
The Municipal Civil Protection Plan is in preparation. Localized structural and non-structural interventions for Disaster Risk Reduction. Insights are provided by the LGSAT.

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
