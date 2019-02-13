---
layout: page
title: Blog
permalink: /blog/
---

I blog semi-regularly about stuff. Most of my blog entries involve professional development stuff for student or some parlor tricks in LaTeX, R, or Markdown that I have taught myself. A full listing of my blog posts follows.

<ul id="archive">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h2 class="blogyear">{{ y}}</h2>
  {% endif %}
<li class="archiveposturl"><span><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></span><br/>
<span class = "postlower"><strong>Author:</strong> {{post.author}} 
<strong>Category:</strong>  {% if post.categories %}
 
  {% for cat in post.categories %}
  <a href="/categories/#{{ cat }}" title="{{ cat }}">{{ cat }}</a>&nbsp;
  {% endfor %}

{% endif %} <!-- {{ post.categories | first }} -->
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif; float:right">{{ post.date | date: '%d %b %Y' }}</strong> 
</span> 

</li>
{% endfor %}
</ul>

<!-- {{ post.date | date: '%m %d, %Y' }} -->
