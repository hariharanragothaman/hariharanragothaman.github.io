---
layout: cv
title: CV
permalink: cv/
jsarr:
- js/scripts.js
---

<h1 id="cv-title"><a href="{{ site.url }}"> {{ site.title }} </a></h1>

<p id="cv-subtitle"><i> {{ site.tagline }} </i></p>


<div>
	I am a Lead Software Engineer with 10 years of industry experience and 2 years of management experience.
	My research interests lie at the intersection of Applied AI, Embedded Systems and Cloud Computing. 
</div>

***

<div class="cv-image-links-wrapper">
	<div class="cv-image-links">
		{% for link in site.data.social-links %}
			{% if link.cv-group == 1 %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	<div class="cv-image-links">
		{% for link in site.data.social-links %}
			{% if link.cv-group == 2 %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
</div>

***

## Education
{::nomarkdown}
{% for degree in site.data.education %}
{% include cv/degree.html degree=degree %}
{% endfor %}
{:/}

## Work Experience
{::nomarkdown}
{% for experience in site.data.experiences %}
{% if experience.type == "industry"%}
{% include cv/experience.html experience=experience %}
{% endif %}
{% endfor %}
{:/}

## Selected Honors and Awards

{% for award in site.data.awards %}
{% include cv/award.html award=award %}
{% endfor %}




## Publications

{% assign selectedBoolForBibtex = true %}
{::nomarkdown}
{% assign selected = site.data.publications | where: 'type', "conference" %}
{% for pub in selected %}
{% include cv/publication.html pub=pub %}
{% endfor %}
{:/}


## Patents

{% assign patent = site.data.publications | where: 'type', "patent" %}
{% for pub in patent %}
{% include cv/publication.html pub=pub selectedBoolForBibtex=selectedBoolForBibtex %}
{% endfor %}

## Peer-Reviewing & Judging

{% for venue in site.data.reviewer %}
{% include cv/venue.html venue=venue %}
{% endfor %}

{% assign talktitles = site.data.talks | group_by:"title" %}
{% for title in talktitles %}
{% include cv/talk.html talk=title %}
{% endfor %}


{% assign talktitles = site.data.university_lectures | group_by:"title" %}
{% for title in talktitles %}
{% include cv/university_lectures.html talk=title %}
{% endfor %}

## Mentees and Interns

{::nomarkdown}
{% for mentee in site.data.mentoring %}
{% include cv/mentee.html mentee=mentee %}
{% endfor %}
{:/}

## Articles and Blogs

{% for blogs in site.data.blogs %}
{% include cv/blogs.html blogs=blogs %}
{% endfor %}

## Speaking and Press

{% for press in site.data.press %}
{% include cv/press.html press=press %}
{% endfor %}
