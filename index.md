---
layout: home
title: Home
jsarr:
- js/scripts.js
---

<div id ="intro-wrapper" class="l-page">
	<div id="intro-title-wrapper" class="intro-left">
		// <h1 id="intro-title">{{ site.title }}</h1>
		<div id="intro-subtitle">
			{{ site.tagline }} 
		</div>
	</div>
	<div class="intro-left">
	<div class="intro-left">
        Hariharan Ragothaman is a seasoned Software Engineer at Advanced Micro Devices (AMD). </div>
	<div style="height: 1rem"></div>
	<div>
        Prior to this, he served as a Lead Software Engineer at athenahealth and worked at Bose Corporation as an Embedded Software Engineer.	
	</div>
	<div class="intro-left">
        Hariharan holds a Master of Science degree from Northeastern University and a Bachelor of Engineering from Anna University. With a strong passion for complex systems design, DevOps, embedded systems, distributed systems, and robotics, he thrives on solving challenging technical problems at scale.
	</div>
	<div style="height: 1rem"></div>
</div>

<div class="intro-right">
	<img id="intro-image" class="intro-right" src="/images/profile.jpeg">
	<div style="height: 0.5rem"></div>
	<div id="intro-image-links" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.on-homepage == true %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	<div style="height: 0.5rem"></div>
	<div id="intro-cv-wrapper" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.id == "cv-web" %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	</div>
</div>




<hr class="l-page">

# News
{% for news in site.data.news %}
{% include news.html news=news %}
{% endfor %}


<hr class="l-page">

# Publications and Patents

{% assign selectedBoolForBibtex = true %}
{% assign selected = site.data.publications %}
{% for pub in selected %}
{% include pubentry.html pub=pub %}
{% endfor %}


<!-- ### All Publications -->

{% assign selectedBoolForBibtex = false %}

<hr class="l-page">
