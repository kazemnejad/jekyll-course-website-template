---
layout: page
title: Lectures
permalink: /lectures/
---

You can download the lectures here (in PDF format). I will try to upload lectures prior to their corresponding classes.


<ul id="archive">
{% for lecture in site.lectures %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if lecture.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ lecture.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ lecture.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="{{ lecture.slides | prepend: site.baseurl }}">{{ lecture.title }}</a></span><br>

        <strong>tl;dr:</strong> {{ lecture.tldr }}
        <br/>
        <strong style="font-size:100%; font-family: 'Titillium Web', sans-serif;">
            [<a title="Download slides (pdf)" href="{{ lecture.slides | prepend: site.baseurl }}">slides</a>]
            {% if lecture.notes %}
            [<a title="Download notes (zip)" href="{{ lecture.notes | prepend: site.baseurl }}">notes</a>]
            {% endif %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>