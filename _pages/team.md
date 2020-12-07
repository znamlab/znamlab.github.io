---
title: "Znamenskiy Lab - Team Members"
layout: gridlay
excerpt: "Znamenskiy Lab: Team members"
sitemap: false
permalink: /team/
---
# Lab Members

<div class="row">
{% for member in site.data.team_members %}

<div class="col-sm-3">
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
</div>
<div class="col-sm-3 align-self-center">
    <h3>{{ member.name }}</h3>
    <p>{{ member.info }} <br />
    <a href="maito:{{ member.email }}">{{ member.email }}</a></p>
</div>

{% assign even_odd = forloop.index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% endfor %}
</div>
