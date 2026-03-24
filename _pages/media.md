---
title: "Matute Lab - Media"
layout: piclay
excerpt: "Matute Lab -- Media"
permalink: /media/
---

# Pictures



## Lectures and Interviews ##

#### On the evolution of postzygotic isolation during divergence [(EcoEvoSeminars Youtube Channel)](https://www.youtube.com/@EvoEco)
<iframe width="560" height="315" src="https://www.youtube.com/embed/6Czy7x-ooqA?si=Im52pegNCwRKaRhn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

#### Gallery

{% assign number_printed = 0 %}
{% for pic in site.data.pictures %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix img-container">
  <img src="{{ site.url }}{{ site.baseurl }}/images/Gallery/{{ pic.image }}" 
       class="img-responsive" width="95%" />

</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>


<!-- 
First advertisement.
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/WebpageLeiden_red.jpg" width="60%" >
</figure>
-->
