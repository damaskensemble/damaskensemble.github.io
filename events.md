---
layout: page
title: Events
eyebrow: Where to hear us
permalink: /events/
---

{% assign today = site.time %}
{% assign upcoming = site.notices | where_exp: "item", "item.date >= today" | sort: "date" %}
{% assign past = site.notices | where_exp: "item", "item.date < today" | sort: "date" | reverse %}

<h2>Upcoming</h2>
{% if upcoming.size > 0 %}
<ul class="notice-list">
  {% for n in upcoming %}
  <li>
    <span class="notice-date">{{ n.date | date: "%-d %B %Y" }}</span>
    <p class="notice-title"><a href="{{ n.url | relative_url }}">{{ n.title }}</a></p>
    {% if n.venue %}<p class="notice-venue">{{ n.venue }}</p>{% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No upcoming events are scheduled at the moment — check back soon.</p>
{% endif %}

<h2>Past</h2>
{% if past.size > 0 %}
<ul class="notice-list">
  {% for n in past %}
  <li>
    <span class="notice-date">{{ n.date | date: "%-d %B %Y" }}</span>
    <p class="notice-title"><a href="{{ n.url | relative_url }}">{{ n.title }}</a></p>
    {% if n.venue %}<p class="notice-venue">{{ n.venue }}</p>{% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No past events yet.</p>
{% endif %}

<p>Presenting a series, festival, or house concert? We'd love to hear from
you — see the <a href="{{ '/contact/' | relative_url }}">contact page</a>.</p>
