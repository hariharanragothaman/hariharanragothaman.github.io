---
layout: cv
title: CV
permalink: cv/
jsarr:
- js/scripts.js
---

<h1 id="cv-title"><a href="{{ site.url }}"> {{ site.title }} </a></h1>

<p id="cv-subtitle"><i> {{ site.tagline }} </i></p>


<div style="text-align: justify;">
    I am a Lead Software Engineer with 10+ years of industry experience—including 2 years in management—and a strong passion for complex systems design, DevSecOps, Embedded Systems, Distributed Systems.
    My research interests lie at the intersection of Applied AI, Embedded Systems, and Cloud Computing.

<p>
    Proficient in Python (3.x), C++17, and Data Structures & Algorithms, I thrive on solving challenging technical problems at scale. 
    I excel at rapidly understanding large codebases and am deeply passionate about problem-solving, product building, and technical leadership.
</p>

<p>
    Highlights: 23 Publications | 21 Invited Talks | 90+  Manuscripts Reviewed | 11 Hackathons Judged   
</p>

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

## Research Experience

{::nomarkdown}
{% for experience in site.data.experiences %}
{% if experience.type == "research"%}
{% include cv/experience.html experience=experience %}
{% endif %}
{% endfor %}
{:/}

## Selected Honors & Awards

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

## Invited Technical Talks, Keynotes & Press

{% for press in site.data.press %}
{% include cv/press.html press=press %}
{% endfor %}

## Reviewer Activities

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

## Synergistic Activities

{% for venue in site.data.synergy %}
{% include cv/pc.html venue=venue %}
{% endfor %}


## Scientific & Technical Leadership

{% for venue in site.data.pc %}
{% include cv/pc.html venue=venue %}
{% endfor %}

## Memberships

{% for item in site.data.membership %}
{% include cv/membership.html membership=item %}
{% endfor %}

## Technical Blogs & Thought Leadership

{% for blogs in site.data.blogs %}
{% include cv/blogs.html blogs=blogs %}
{% endfor %}

## Mentees & Interns

{::nomarkdown}
{% for mentee in site.data.mentoring %}
{% include cv/mentee.html mentee=mentee %}
{% endfor %}
{:/}
