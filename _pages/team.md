---
title: "Znamenskiy Lab - Team Members"
layout: gridlay
excerpt: "Members of the Znamenskiy lab at the Francis Crick Institute"
sitemap: false
permalink: /team
---

# Current Lab Members

{% assign index = 1 %}

<div class="row">
{% for member in site.categories.team reversed %}
{% if member.alumni != true %}
<div class="col-sm-3">
  {% if member.photo %}
  {% if member.link_to_page %}
  <a href="{{ member.url }}">
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  </a>
  {% else %}
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}
  {% endif %}
</div>
<div class="col-sm-3 align-self-center">
    {% if member.link_to_page %}
    <a href="{{ member.url }}"><h3>{{ member.title }}</h3></a>
    {% else %}
    <h3>{{ member.title }}</h3>
    {% endif %}
    <p>{{ member.info }} <br />
    </p>
</div>
{% assign even_odd = index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% assign index = index | plus: 1 %}
{% endif %}
{% endfor %}

<div id="gridid" class="col-12">
<h1 id="former-lab-members">Former Lab Members</h1>
{% assign index = 1 %}
<div class="row">
{% for member in site.categories.team reversed %}
{% if member.alumni == true %}
<div class="col-sm-3">
  {% if member.photo %}
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}
</div>
<div class="col-sm-3 align-self-center">
    <h3>{{ member.title }}</h3>
    <p>{{ member.info }} <br />
    </p>
</div>
{% assign index = index | plus: 1 %}
{% assign even_odd = index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% endif %}
{% endfor %}
</div>
</div>
