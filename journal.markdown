---
title: Journal
layout: index
bodyclass: journal
---


<ul class="archive">
{% for post in site.posts %}
  <li>
      <a href="{{ post.url }}">{{ post.title }}</a>      
  </li>
{% endfor %}
</ul>
