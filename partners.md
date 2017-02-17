---
title: Partners
layout: partners
description: Listing of U-Score2 partners
---

![Uscore2 project partners](/images/uscore2_partners.jpg "Uscore2 Partners")
<h2>Partner profiles</h2>
{% for partners in site.partners %}

<h3><a href="{{ partners.url | prepend: site.baseurl }}">{{ partners.title }}
</a></h3>
<div class="text-container flex">
<p class="post-excerpt profile-thumb-image">
	{% if partners.image %}<img src="{{ partners.image}}"/>{% endif %}
{{ partners.description}}<a href="{{ partners.url | prepend: site.baseurl }}">  Read More</a></p>
</div>
{% endfor %} 
