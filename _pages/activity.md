---
layout: archive
title: "Activity"
permalink: /activity/
author_profile: true
---

{% include base_path %}

<h2 id="professional-service">Professional Service</h2>
<hr />

{% if site.data.service.reviewer.size > 0 %}
<h3>Reviewer</h3>
<ul>
{% for item in site.data.service.reviewer %}
  <li>
    {% if item.url %}<a href="{{ item.url }}">{{ item.venue }}</a>{% else %}{{ item.venue }}{% endif %}
    {% if item.years %}({{ item.years | join: ", " }}){% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

{% if site.data.service.organizer.size > 0 %}
<h3>Organizer</h3>
<ul>
{% for item in site.data.service.organizer %}
  <li>
    {% if item.url %}<a href="{{ item.url }}">{{ item.name }}</a>{% else %}{{ item.name }}{% endif %}
    {% if item.role %} &mdash; {{ item.role }}{% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

<h2 id="talks">Talks</h2>
<hr />

{% if site.talks.size > 0 %}
  {% for post in site.talks reversed %}
    {% include archive-single-talk.html %}
  {% endfor %}
{% else %}
  <p>No talks to display yet.</p>
{% endif %}
