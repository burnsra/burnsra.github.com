---
layout: default
title: "Blog"
---

<p class="intro">Blog entries focused on both personal events and technology / development subjects.</p>

<div class="listing">
{% for post in site.categories['blog'] %}
  {% if post.type == 'link' %}
    <div class="post other link">
      <a class="icon" href="{{ post.url }}" title="This is a link elsewhere">★</a>
      <h2><a href="{{ post.link }}">{{ post.title }}</a></h2>
      <p>{{ post.content }}</p>
    </div>
  {% else %}
    <div class="post">
      <p class="date">{{ post.date | date: "%B %e, %Y" }}</p>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-summary">{{ post.summary }}</p>
    </div>
  {% endif %}
{% endfor %}
</div>
