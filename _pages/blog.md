---
title: "Znamenskiy Lab - Blog"
layout: textlay
excerpt: "Blog and updates from the Znamenskiy lab"
sitemap: false
permalink: /blog
---

# Blog

<div class="post-list">
{% for post in site.posts %}
  {% if post.layout != 'member' %}
    <div class="post-item d-flex align-items-start mb-4">
      {% if post.thumbnail %}
        <div class="flex-shrink-0 mr-3">
          <a href="{{ post.url | relative_url }}" {% if post.thumbnail_caption %}title="{{ post.thumbnail_caption | escape }}"{% endif %}>
            <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }}" style="width: 150px; height: 150px; object-fit: cover;" class="rounded">
          </a>
        </div>
      {% endif %}
      <div class="flex-grow-1">
        <h2><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
        <div class="post-meta">
          {{ post.date | date: "%b %-d, %Y" }}
          {% if post.authors and post.authors.size > 0 %}
            &nbsp;&bull;&nbsp;by
            {% for author in post.authors %}
              {% if author.url %}
                <a href="{{ author.url }}" target="_blank" rel="noopener noreferrer">{{ author.name }}</a>
              {% else %}
                {{ author.name }}
              {% endif %}
              {% unless forloop.last %}, {% endunless %}
            {% endfor %}
          {% endif %}
        </div>
        {% if post.tags and post.tags.size > 0 %}
        <p class="post-tags">
          {% for tag in post.tags %}
            <a href="{{ tag | slugify | prepend: '/blog/tag/' | relative_url }}">
              <i class="fa-solid fa-hashtag fa-sm"></i> {{ tag }}
            </a>
            {% unless forloop.last %}&nbsp;{% endunless %}
          {% endfor %}
        </p>
        {% endif %}
        <div class="post-excerpt">
          {% if post.description %}
            {{ post.description }}
          {% else %}
            {{ post.excerpt }}
          {% endif %}
          <a href="{{ post.url | relative_url }}">Read more...</a>
        </div>
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>
