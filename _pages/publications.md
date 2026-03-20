---
title: "Matute Lab - Publications"
layout: gridlay
excerpt: "Matute Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**A full list of publications can be found on [Google Scholar](https://scholar.google.com/citations?user=zZFIS2oAAAAJ&hl=en). Preprints are also available on [BioRxiv](https://www.biorxiv.org/search/Daniel%252BMatute).**


<!-- accordion menu markdown architecture -->
{% include accordion.html %}

{% assign the_years = "2026,2025,2024,2023,2022,2021,2020,2019,2018,2017" | split: "," %}
<ul class="jekyllcodex_accordion">
{% for year in the_years %}
  {% assign pubs = site.data.publist | where: "year", year %}
  <li>
    <input id="accordion{{ year }}" type="checkbox" {% if forloop.first %}checked{% endif %} />
    <label for="accordion{{ year }}">{{ year }}</label>
    <div>
      {% if pubs.size > 0 %}
        <ul style="margin: 0; padding-left: 1rem;"> 
          {% for publi in pubs %}
            <li style="margin-bottom: 0.5rem;">
              <strong>{{ publi.title }}.</strong><br>
              <em>{{ publi.authors }}</em>. {{ publi.journal }}{% if publi.pages %} {{ publi.pages }}{% endif %}.{% if publi.link.url %} <a href="{{ publi.link.url }}" target="_blank">{{ publi.link.display }}</a>{% endif %}
            </li>
          {% endfor %}
        </ul>
      {% else %}
        <p>No citations for {{ year }}.</p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>
