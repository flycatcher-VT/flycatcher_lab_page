---
title: "Matute Lab - Publications"
layout: gridlay
excerpt: "Matute Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**All papers are also available on [BioXiv](https://www.biorxiv.org/search/Daniel%252BMatute) and [Google Scholar](https://scholar.google.com/citations?user=zZFIS2oAAAAJ&hl=en).**

{% comment %} Accordion years 2026-2014. Use Bootstrap-compatible panel accordions. {% endcomment %}

<div class="panel-group" id="yearAccordion" role="tablist" aria-multiselectable="true">
{% assign the_years = "2026,2025,2024,2023,2022,2021,2020,2019,2018,2017,2016,2015,2014" | split: "," %}
{% for year in the_years %}
  {% assign open_class = "" %}
  {% assign aria_expanded = "false" %}
  {% if forloop.first %}
    {% assign open_class = "in" %}
    {% assign aria_expanded = "true" %}
  {% endif %}
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="heading{{ year }}">
      <h4 class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#yearAccordion" href="#collapse{{ year }}" aria-expanded="{{ aria_expanded }}" aria-controls="collapse{{ year }}">
          {{ year }}
        </a>
      </h4>
    </div>
    <div id="collapse{{ year }}" class="panel-collapse collapse {{ open_class }}" role="tabpanel" aria-labelledby="heading{{ year }}">
      <div class="panel-body">
        {% assign pubs = site.data.publist | where: "year", year %}
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
    </div>
  </div>
{% endfor %}
</div>


