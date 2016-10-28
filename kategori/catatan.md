---
layout: default
---
### Laman dengan kategori catatan
{% for post in site.categories.catatan %}
 <li><span>{{ post.date | date: "%m/%d/%Y" }}</span> - <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
<br>
