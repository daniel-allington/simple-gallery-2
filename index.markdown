---
title: Gallery index
layout: index
---

{% for exhibit in site.exhibits %}
{% assign creator = site.data.creators | find: "name", exhibit.creator %}
<a href = "{{ exhibit.url | relative_url }}"><img src="{{ exhibit.image-url }}" width = 256></a>
<p><a href = "{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a> by <a href = "{{ creator.homepage }}">{{ exhibit.creator }}</a></p>
<p><a href="{{ exhibit.licence-url }}">{{ exhibit.licence }}</a></p>
{% endfor %}
