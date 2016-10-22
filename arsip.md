---
layout: page
title: Arsip
---
<section id="archive">
  <h3>Arsip tahun ini.</h3>
  {%for post in site.posts %}
    {% unless post.next %}
      <ul class="this">
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        </ul>
        <h3>{{ post.date | date: '%Y' }}</h3>
        <ul class="past">
      {% endif %}
    {% endunless %}
      <li><time>
<!-- Localization to Indonesia language -->
{% assign m = post.date | date: "%-m" %}
{{ post.date | date: "%-d" }}
{% case m %}
  {% when '1' %}Jan
  {% when '2' %}Feb
  {% when '3' %}Mar
  {% when '4' %}Apr
  {% when '5' %}Mei
  {% when '6' %}Jun
  {% when '7' %}Jul
  {% when '8' %}Agu
  {% when '9' %}Sep
  {% when '10' %}Okt
  {% when '11' %}Nov
  {% when '12' %}Des
{% endcase %}
</time> - <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
</section>
