---
layout: home
title: Home
jsarr:
- js/scripts.js
---

<div id ="intro-wrapper" class="l-page">
	<div id="intro-title-wrapper" class="intro-left">
		<h1 id="intro-title">{{ site.title }}</h1>
		<div id="intro-subtitle">
			{{ site.tagline }} 
		</div>
	</div>
	<div class="intro-left">
	<div class="intro-left">
		Hariharan Ragothaman is Member of Technical Staff  at <a href="https://www.amd.com/en.html">Advanced Micro Devices, Inc (AMD)</a>.
	</div>
	<div style="height: 1rem"></div>
	<div>
       Prior to this, he served as a Lead Software Engineer - System Design and Architecture (Manager) at <a href="https://www.athenahealth.com/">athenahealth</a>  where he designed and developed 'Unified Deployment Pipeline' to integrate multiple tech stacks, enhancing service visibility and improving release and product quality. His work in commercializing the macro-service hybrid cloud (Amazon EKS, AWS Local Zones, and AWS Outposts) was a major step towards modernizing the <a href="https://www.athenahealth.com/solutions/athenaone">athenaOne platform</a>.
	</div>
	<div style="height: 1rem"></div>
	<div class="intro-left">
        During his time at <a href="https://www.bose.com/explore/music-at-home">Bose Corporation</a> as an Embedded Software Engineer, he developed scalable firmware for the next generation of Wireless Speakers, Headphones and Home theaters. He also made key contributions to <a href="https://www.bose.com/stories/amazon-alexa?srsltid=AfmBOorb0yocFoRa84y9v3-3D9VVaeBhnJb9_x89QpLkOtTJUw0vsTkp">Alexa Voice Service (AVS)</a> and <a href="https://www.bose.com/stories/google-assistant?srsltid=AfmBOoqrzgh8KID8ZA9PqasC4i9jzrE8v_SEJRtAMgn3PVhhGwh3qUE5">Google Voice Assistant (GVA)</a> integrations with Bose ecosystem, creating unique scalable frameworks.
	</div>
	<div style="height: 1rem"></div>
	<div class="intro-left">
        He received his Masters degree at <a href="https://www.northeastern.edu/">Northeastern University</a>, Boston and Bachelors degree at <a href="https://www.annauniv.edu/">Anna University</a>, Chennai. He is also Senior Member in <a href="https://www.ieee.org/">IEEE</a>, <a href="https://www.computer.org/">IEEE Computer Society</a>, <a href="https://www.isa.org/">ISA</a>.
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

# Timeline
{% for news in site.data.news %}
{% include news.html news=news %}
{% endfor %}


<hr class="l-page">

# Publications

{% assign selectedBoolForBibtex = true %}
{% assign selected = site.data.publications %}
{% for pub in selected %}
{% include pubentry.html pub=pub %}
{% endfor %}


<!-- ### All Publications -->

{% assign selectedBoolForBibtex = false %}

<hr class="l-page">
