---
title: "Znamenskiy Lab - Publications"
layout: gridlay
excerpt: "Znamenskiy Lab - Publications."
sitemap: false
permalink: /publications
---


# Publications
{% assign number_printed = 0 %}
{% for publi in site.data.publications reversed %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <h3>{{ publi.title }}</h3>
  {% if publi.image %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubs/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  {% endif %}
  <p><em>{{ publi.authors }}</em></p>
  <p>{{ publi.description }}</p>
  <p><strong><a href="{{ publi.url }}">{{ publi.ref }}</a></strong></p>  
 </div>
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

<p> &nbsp; </p>
