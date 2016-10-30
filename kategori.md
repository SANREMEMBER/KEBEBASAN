---
layout: page
title: Kategori
---
### Kumpulan Laman yang Disortir Berdasarkan Kategori

<section id="categories">
{% for category in site.categories %}
 <h3 id="{{ category | first }}"><font style="text-transform: capitalize;">{{ category | first }}</font></h3>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
        {% if post.url %}
          <li>{{ post.date | date: "%Y/%m/%d" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endif %}
      {% endfor %}
    {% endfor %}
    </ul>
{% endfor %}
</section>
