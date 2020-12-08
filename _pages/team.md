---
title: "Znamenskiy Lab - Team Members"
layout: gridlay
excerpt: "Znamenskiy Lab: Team members"
sitemap: false
permalink: /team/
---
# Lab Members

<div class="row">
{% for member in site.categories.team reversed %}

<div class="col-sm-3">
  {% if member.link_to_page %}
  <a href="{{ member.url }}">
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  </a>
  {% else %}
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}
</div>
<div class="col-sm-3 align-self-center">
    {% if member.link_to_page %}
    <a href="{{ member.url }}"><h3>{{ member.title }}</h3></a>
    {% else %}
    <h3>{{ member.title }}</h3>
    {% endif %}
    <p>{{ member.info }} <br />
    <a href="maito:{{ member.email }}">{{ member.email }}</a></p>
</div>

{% assign even_odd = forloop.index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% endfor %}
</div>
