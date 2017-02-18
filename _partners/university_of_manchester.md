---
title: University of Manchester - UK
layout: partners
country: United Kingdom
website: http://www.mbs.ac.uk
description: The Alliance Manchester Business School (AMBS) was established in 1965
  as one of the UK's first two business schools. Now, AMBS is the UK's largest campus-based
  business and management school and rated second in the REF 2014 for research power.
  'Original Thinking Applied' is at the heart of AMBS and underpins our ethos of conducting
  practically-relevant, theoretically-rigorous scholarly activity.
image: "/images/UoM.jpg"
map:
  latitude: 53.4686488
  longitude: -2.2353484
  address: " Alliance Manchester Business School"
  zoom: 10
---

<div class="map" id="map"></div>

<section class="testimonial">
		<div class="container flex">
			<div class="testimonial-block">
				<blockquote>
					<p class="editable">Uscore2 offers a unique and exciting opportunity to work with leading cities in civil protection to create a useable tool that will enhance the peer review process for disaster risk reduction. Manchester University is supporting the design and evaluation of this tool to ensure widespread impact through even stronger city learning and adoption of resilience practices.</p>
					<p class="editable">Professor Duncan Shaw, Alliance Manchester Business School and the Humanitarian & Conflict Research Institute (HCRI)</p>
				</blockquote>
			</div>
		</div>
	</section>

## PROFILE 

The Alliance Manchester Business School (AMBS) was established in 1965 as one of the UK's first two business schools. Now, AMBS is the UK's largest campus-based business and management school and rated second in the REF 2014 for research power. 'Original Thinking Applied' is at the heart of AMBS and underpins our ethos of conducting practically-relevant, theoretically-rigorous scholarly activity. We have a global reach with centres in São Paolo, Dubai, Hong Kong, Shanghai and Singapore. [AMBS](www.mbs.ac.uk)
 
Also involved from the University of Manchester is the Humanitarian and Conflict Research Institute (HCRI). HCRI is a leading centre for the study of humanitarianism and conflict response, and international disaster management. HCRI is driven by a desire to inform and support policy and decision makers, to optimise collaborations between partner organisations, and to foster increased understanding and debate within the field. HCRI aims to facilitate improvements in crisis response on a global scale, while providing a centre of excellence for practitioners in emergencies and conflicts. [HCRI](www.hcri.ac.uk)

![University of Manchester - UK](/images/UoM.jpg "University of Manchester - UK")

## The staff involved include:
  [Professor Duncan Shaw](https://www.research.manchester.ac.uk/portal/duncan.shaw-2.html)  
  [Dr Manuel López-Ibáñez](http://www.mbs.ac.uk/research/people/profiles/mlopez-ibanez)  
  [Dr Chris Smith](http://www.mbs.ac.uk/research/people/profiles/csmith)  

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
