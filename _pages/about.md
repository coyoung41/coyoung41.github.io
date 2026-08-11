---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm Co Yong, a PhD student in the Data Science Degree Program at National Taiwan University and Academia Sinica under the supervision of Prof. Shao-Hua Sun. My research focuses on offline RL, offline imitation learning and model-based planning. I'm recently exploring zero-shot RL.

## News

{% assign sorted_news = site.data.news | sort: "date" | reverse %}
<ul class="news-list">
{% for item in sorted_news %}
  <li><span class="news-date">{{ item.date | date: "%b %Y" }}</span> — {{ item.text | markdownify | remove: "<p>" | remove: "</p>" }}</li>
{% endfor %}
</ul>

## Publications

{% include base_path %}

{% assign sorted_pubs = site.publications | sort: "date" | reverse %}
{% for post in sorted_pubs %}
  {% include archive-single.html %}
{% endfor %}