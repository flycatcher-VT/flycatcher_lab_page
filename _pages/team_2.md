---
title: "Matute Lab - Team"
layout: gridlay
excerpt: "Matute Lab: Team members"
sitemap: false
permalink: /team_2/
---

# Group Members

<!--  
 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

# page links to team member sections, insert/edit if there are changes
[administrative support](#administrative-support),
[master and bachelor students](#master-and-bachelor-students),
[lab visitors](#lab-visitors)
-->
Jump to [Staff](#staff), [Undergraduate Researchers ](#undergraduate-researchers),  [Post Doctoral Alumni](#post-doctoral-alumni).

## Staff
{% for member in site.data.team_members %}
<div style="overflow: hidden; margin-bottom: 1.2em; padding-bottom: 0.5em; border-bottom: 1px solid #ddd;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="float: left; width: 145px; max-width: 25%; margin-right: 1rem; margin-bottom: 0.5rem;" alt="{{ member.name }}" />
  <h4 style="margin-top: 0;">{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <ul style="margin-top: 0.5rem; padding-left: 1.2rem; overflow: hidden;">
    {% if member.number_educ == 1 %}
    <li>{{ member.education1 | markdownify }}</li>
    {% endif %}
    {% if member.number_educ == 2 %}
    <li>{{ member.education1 | markdownify }}</li>
    <li>{{ member.education2 | markdownify }}</li>
    {% endif %}
    {% if member.number_educ == 3 %}
    <li>{{ member.education1 | markdownify }}</li>
    <li>{{ member.education2 | markdownify }}</li>
    <li>{{ member.education3 | markdownify }}</li>
    {% endif %}
    {% if member.number_educ == 4 %}
    <li>{{ member.education1 | markdownify }}</li>
    <li>{{ member.education2 | markdownify }}</li>
    <li>{{ member.education3 | markdownify }}</li>
    <li>{{ member.education4 | markdownify }}</li>
    {% endif %}
    {% if member.number_educ == 5 %}
    <li>{{ member.education1 | markdownify }}</li>
    <li>{{ member.education2 | markdownify }}</li>
    <li>{{ member.education3 | markdownify }}</li>
    <li>{{ member.education4 | markdownify }}</li>
    <li>{{ member.education5 | markdownify }}</li>
    {% endif %}
  </ul>
</div>
{% endfor %}



<!--  Remove comment blocks to put lab member sections back in

<br>email: <{{ member.email }}></i> 

## Master and Bachelor Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} 
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

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
-->

## Undergraduate Researchers

{% assign number_printed = 0 %}
{% for member in site.data.undergraduates %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
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


## Post Doctoral Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.duration }} <br> {{ member.info }}</i>
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


<!--
## Former visitors, BSc/ MSc students
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>
-->


