---
title: "Matute Lab - Media"
layout: piclay
excerpt: "Matute Lab -- Media"
permalink: /media/
---



## Lectures and Interviews ##

#### On the evolution of postzygotic isolation during divergence [(EcoEvoSeminars Youtube Channel)](https://www.youtube.com/@EvoEco)
<iframe width="560" height="315" src="https://www.youtube.com/embed/6Czy7x-ooqA?si=Im52pegNCwRKaRhn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


#### The genetics basis of inviability between *Drosophila melanogaster* and *D. santomea* | Drosophila Conference Plenary Session I (1:15:00)[(Genetics Society of America Youtube Channel)](https://www.youtube.com/@GeneticsSocietyofAmerica)


<iframe width="560" height="315" src="https://www.youtube.com/embed/iWY1ewdYD2o?si=4hLMsyDRNAKY-Zss&amp;start=4479" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


#### The promise of speciation research as a bridge for micro & macroevolution (30:33)[(Network for the Integration of Speciation Research Youtube Channel)](https://www.youtube.com/@Speciation_net)

<iframe width="560" height="315" src="https://www.youtube.com/embed/Uv_NtODQiss?si=NsZ4BoeQ2NwTzJQ8&amp;start=1832" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Gallery ## 

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
