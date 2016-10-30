---
layout: default
---
### Laman dengan kategori catatan
{% for post in site.categories.catatan %}
 <li><span>{{ post.date | date: "%Y/%m/%d" }}</span> - <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
<br>
