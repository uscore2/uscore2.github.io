---
title: Salford city – United Kingdom
layout: partners
country: United Kingdom
website: www.gmemergencyplanning.org.uk
Size: 97.19 km2
Population:
- year: 2011
- total: 233933
Part Of: Greater Manchester
Hazards: Epidemic & Pandemic, Flood, Heat Wave, Technical Disaster
description: Greater Manchester lies in the north west of England and is one of the
  largest metropolitan areas in the UK. Designated a city region in 2011 it comprises
  the cities of Manchester and Salford, together with the metropolitan boroughs of
  Bolton, Bury, Oldham, Rochdale, Stockport, Tameside, Trafford and Wigan. There is
  a mix of high density urban areas, suburbs and semi-rural locations.
image: "/images/salford.png"
map:
  latitude: 53.4845812
  longitude: -2.2841627
  address: " Amadora, Portugal"
  zoom: 7
---

<div class="map" id="map"></div>

<section class="testimonial">
		<div class="container flex">
			<div class="testimonial-block">
				<blockquote>
					<p class="editable">Working in partnership helps residents and businesses to recognise opportunities to realise our ambitions whilst meeting the challenges of a changing risk landscape. Greater Manchester is stronger together.</p>
					<p class="profile_author">Mr. Tony Lloyd</p>
					<p>Mayor</p>
				</blockquote>
			</div>
		</div>
	</section>


## HAZARD AND VULNERABILITY PROFILE 
Greater Manchester lies in the north west of England and is one of the largest metropolitan areas in the UK. Designated a city region in 2011 it comprises the cities of Manchester and Salford, together with the metropolitan boroughs of Bolton, Bury, Oldham, Rochdale, Stockport, Tameside, Trafford and Wigan. There is a mix of high density urban areas, suburbs and semi-rural locations. Due to its geographical position Greater Manchester is exposed to a number of climate related and severe weather risks. Flooding is acknowledged as a major risk with heatwaves, storms, snow and high winds presenting further risks within the conurbation. On account of the population size and Greater Manchester’s importance as an economic region there are also transport, infrastructure, industrial and environmental risks. Manchester hosts one of the largest airports in the UK and the conurbation acts as a central hub for road and rail travel in the north west. 

![alt text](/images/salford.png "Salford - Manchester")

## DISASTER AND RISK REDUCTION ACTIVITIES 
The UK has a robust disaster risk reduction framework underpinned by legislation. Across Greater Manchester the 10 local authorities work in partnership with public sector, private sector, academic and voluntary organisations to research the impacts of major risks, to develop collaborative responses to potential hazards and to strengthen the resilience of the city region. The self-assessment contains details of many of the disaster risk reduction programmes in place across Greater Manchester.

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
