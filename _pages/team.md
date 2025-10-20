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

<div class="col-md-4">
  {% if member.photo %}
    {% if member.link_to_page %}
      <a href="{{ member.url }}">
        <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
      </a>
    {% else %}
      <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
    {% endif %}
  {% endif %}
  
  <div class="mt-2"> {% if member.link_to_page %}
      <a href="{{ member.url }}"><h3>{{ member.title }}</h3></a>
    {% else %}
      <h3>{{ member.title }}</h3>
    {% endif %}
    <p>{{ member.info }}</p>
  </div>
</div>

{% assign count = index | modulo: 3 %}
{% if count == 0 %}
<div class="w-100"></div>
{% endif %}
{% assign index = index | plus: 1 %}

{% endif %}
{% endfor %}
</div>

---

# Alumni

{% assign index = 1 %}

<div class="row">
{% for member in site.categories.team reversed %}
{% if member.alumni == true %}
<div class="col-md-4">
  {% if member.photo %}
    <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}

  <div class="mt-2">
    <h3>{{ member.title }}</h3>
    <p>{{ member.info }}</p>
  </div>
</div>

{% assign count = index | modulo: 3 %}
{% if count == 0 %}
<div class="w-100"></div>
{% endif %}
{% assign index = index | plus: 1 %}

{% endif %}
{% endfor %}
</div>
