---
layout: page
title:
meta_description:
  Archivo de posts
permalink: /categories
section: archivo
intro_paragraph:
---

<section>
<h4>
  <a href={{ site.baseurl }}"/archivo" >Archivo por fecha</a>
</h4>

{% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
<ul>
    <strong> {{ category_name }} </strong>
</ul>
    {% for post in site.categories[category_name] %}

<ul>
      <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>

    {% endfor %}
{% endfor %}
</ul>

