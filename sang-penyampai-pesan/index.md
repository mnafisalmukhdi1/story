---
layout: story
img: https://mnafisalmukhdi1.github.io/cdn/works/spp.jpeg
title: Sang Penyampai Pesan
desc: Sang Penyampai Pesan adalah trilogi cerpen fiksi penggemar–tidak termasuk prolog–untuk seseorang yang seharusnya muncul di dunia maya.
---
<ul>
{% assign folder = 'sang-penyampai-pesan' %}
{% for file in site.static_files %}
{% if file.path contains folder and file.name != "index.md" %} 
<li><a href="{{ file.url }}">{{ file.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
