---
layout: page
show_meta: false
title: "Let's talk about work a little."
subheadline:
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/development/"
---
<ul>
    {% for post in site.categories.development %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
