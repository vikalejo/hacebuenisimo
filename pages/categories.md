---
layout: page
title:
meta_description:
  Archivo de posts
permalink: /categories
section: archivo
intro_paragraph:
---


<h3>
  <a href={{ site.baseurl }}"/archivo" >Archivo por fecha</a>
</h3>

{% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
<ul>
    <h4> {{ category_name }} </h4>
</ul>
    {% for post in site.categories[category_name] %}

<ul>
      <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>

    {% endfor %}
{% endfor %}
</ul>

