---
layout: default
title: Blog
---
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">
	  {{ post.date | date: '%Y/%m/%d-%A' }} : {{ post.title }}
      </a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>