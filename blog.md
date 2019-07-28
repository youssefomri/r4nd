---
layout: default
title: R4ND BLOG
---
<ul class = "set1">
  {% for post in site.posts %}
    <li class = "set2">
      <h2><a href="{{ post.url | relative_url }}">
	  {{ post.date | date: '%Y/%m/%d-%A' }} : {{ post.title }}
      </a></h2>
      <!--<p>{{ post.excerpt }}</p>-->
    </li>
  {% endfor %}
</ul>
