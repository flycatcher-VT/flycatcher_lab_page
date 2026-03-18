---
title: "Matute Lab - Publications"
layout: gridlay
excerpt: "Matute Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**All papers are also available on [BioXiv](https://www.biorxiv.org/search/Daniel%252BMatute) and [Google Scholar](https://scholar.google.com/citations?user=zZFIS2oAAAAJ&hl=en).**

{% include accordion.html %}

{% assign the_years = "2026,2025,2024,2023,2022,2021,2020,2019,2018,2017,2016,2015,2014" | split: "," %}
<ul class="jekyllcodex_accordion">
{% for year in the_years %}
  {% assign pubs = site.data.publist | where: "year", year %}
  <li>
    <input id="accordion{{ year }}" type="checkbox" />
    <label for="accordion{{ year }}">{{ year }}</label>
    <div>
      {% if pubs.size > 0 %}
        <ul style="margin: 0; padding-left: 1rem;">
          {% for publi in pubs %}
            <li style="margin-bottom: 0.5rem;">{% if publi.citation %}{{ publi.citation }}{% else %}<strong>{{ publi.title }}</strong> <em>{{ publi.authors }}</em>{% endif %}</li>
          {% endfor %}
        </ul>
      {% else %}
        <p>No citations for {{ year }}.</p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>


