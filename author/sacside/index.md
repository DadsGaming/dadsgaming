---
author: sacside
layout: blog
title: Archive Author
background-image: s-1.jpg
---

<div class="clearfix"></div>

<ul>
	<li>
		{{ site.data.authors[sacside].display_name }}
	</li>
</ul>

<ul>
    {% for author in site.data.authors %}
    <li>
        {{ author.display_name }}
    </li>
    {% endfor %}
</ul>

<!--author box-->
<div class="author-box"> <img alt="" src="{{ site.baseurl }}/img/team/{{ author.avatar }}"  class="avatar " height="100" width="100">
	<div class="author-box-title"> Authored By <a href="{{ site.baseurl }}/author/{{ page.author }}/" rel="author">{{ page.author }}</a> </div>
	<div class="author-description"> {{ author.description }} </div>
	<div class="author_social"> </div>
</div>
<!--/author box-->



<div class="clearfix"></div>

{% assign sorted-posts = site.posts | where: "author","sacside" %}
{% for post in sorted-posts %}

<!--article-->
<article class="col-md-12 wow fadeInUp">
  <header class="entry-header"> <span class="date-article"><i class="fas fa-calendar-alt"></i> {{ post.date | date_to_string }}</span> <a href="{{post.url}}"><img src="/img/post/{{ post.image }}" class="img-responsive"></a> <span class="byline"><span class="author vcard"><a href="{{ site.baseurl }}/category/{{ post.category }}/"><i class="fas fa-folder-open"></i> {{ post.category }}</a><a href="#"><i class="fas fa-user"></i> {{ post.author }}</a> </span></span> <a href="{{post.url}}">
    <h2>{{ post.title }}</h2>
    </a></header>
  <p>{{ post.excerpt | strip_html | truncatewords:25 }}</p>
  <a class="btn  readmore-btn" href="{{post.url}}">READ MORE</a>
</article>
<!--/article-->

{% endfor %}
