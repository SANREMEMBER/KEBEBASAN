---
layout: page
title: Tanda
---
### Kumpulan Laman yang Disortir Berdasarkan Tanda

<section id="tanda">
{% for tag in site.tags %}
 <h3 id="{{ tag | first }}"><font style="text-transform: capitalize;">{{ tag | first }}</font></h3>
    <ul>
    {% for posts in tag %}
      {% for post in posts %}
        {% if post.url %}
          <li>{{ post.date | date: "%Y/%m/%d" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endif %}
      {% endfor %}
    {% endfor %}
    </ul>
{% endfor %}
</section>
