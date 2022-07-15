---
layout: page
title:
meta_description:
  Archivo de posts
permalink: /archivo
section: archivo
intro_paragraph:
---
<section>
<h4>
  <a href={{ site.baseurl }}"/categories" >Archivo por categorias </a>
</h4>

{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in postsByYear %}
  {% comment %}
  {{ year.name }}
  {% endcomment %}
  {% assign postsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}

{% for month in postsByMonth %}
<strong>{{ month.name }}</strong>
<ul>
  {% for post in month.items %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

{% endfor %}
{% endfor %}
<p>
