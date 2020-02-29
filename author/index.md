---
layout: blog
title: "Archive Author"
background-image: s-1.jpg
---

<div class="clearfix"></div>

<ul>
    {% for author in site.data.authors %}
    <li>
        <h2><a href="{{ author.url }}">{{ author.display_name }}</a></h2>
        <p>{{ author.content | markdownify }}</p>
    </li>
    {% endfor %}
</ul>
