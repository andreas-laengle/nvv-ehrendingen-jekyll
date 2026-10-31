---
title: Anlässe
nav: Anlässe
nav_order: 5
layout: page
permalink: /anlaesse/
---

<div class="event-list">
{% assign events = site.posts | sort: 'date' | reverse %}
{% for post in events %}
{% assign post_image = post.image | default: '/assets/images/mrlebies-red-backs-1201550_1920.jpg' %}
<article class="event-teaser card h-100">
  <img class="event-teaser__image" src="{{ post_image | relative_url }}" alt="{{ post.title }}" />
  <div class="card-body p-3 p-md-4">
    <span class="event-teaser__date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d. %B %Y" }}</time></span>
    <h2 class="h4 mt-3 mb-2"><a href="{{ post.url | relative_url }}" class="text-decoration-none text-dark">{{ post.title }}</a></h2>
    <p class="text-muted mb-3">{{ post.excerpt | strip_html | truncate: 180 }}</p>
    <a href="{{ post.url | relative_url }}" class="btn event-teaser__link">Mehr lesen</a>
  </div>
</article>
{% endfor %}
</div>
