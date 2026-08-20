---
title: "Flycatcher Lab - Team"
layout: gridlay
excerpt: "Flycatcher Lab: Team members"
sitemap: false
permalink: /team_2/
---

# Group Members

  
<!--  **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

# page links to team member sections, insert/edit if there are changes
[administrative support](#administrative-support),
[master and bachelor students](#master-and-bachelor-students),
[lab visitors](#lab-visitors) -->


Jump to [Senior Members](#senior-members), [Students] (#students), [Undergraduate Researchers ](#undergraduate-researchers).

## Senior Members
{% for member in site.data.team_members_2 %}
<div style="overflow: hidden; margin-bottom: 1.2em; padding-bottom: 0.5em; border-bottom: 1px solid #ddd;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img" style="float: left; width: 145px; max-width: 25%; margin-right: 1rem; margin-bottom: 0.5rem;" alt="{{ member.name }}" />
  <h4 style="margin-top: 0;">{{ member.name }}</h4>
  <i>{{ member.info }}</i><br/>
  {% if member.email %}<a href="mailto:{{ member.email }}">{{ member.email }}</a><br/>{% endif %}
  <ul style="margin-top: 0.5rem; padding-left: 1.2rem; overflow: hidden;">
  <i>{{ member.bio }}</i><br/>
  </ul>
</div>
{% endfor %}

## Students
{% for member in site.data.students %}
<div style="overflow: hidden; margin-bottom: 1.2em; padding-bottom: 0.5em; border-bottom: 1px solid #ddd;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img" style="float: left; width: 145px; max-width: 25%; margin-right: 1rem; margin-bottom: 0.5rem;" alt="{{ member.name }}" />
  <h4 style="margin-top: 0;">{{ member.name }}</h4>
  <i>{{ member.info }}</i><br/>
  {% if member.email %}<a href="mailto:{{ member.email }}">{{ member.email }}</a><br/>{% endif %}
  <ul style="margin-top: 0.5rem; padding-left: 1.2rem; overflow: hidden;">
  <i>{{ member.bio }}</i><br/>
  </ul>
</div>
{% endfor %}

## Undergraduate Researchers

{% assign number_printed = 0 %}
{% for member in site.data.undergraduates %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

