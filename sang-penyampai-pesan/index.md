---
layout: story
img: https://mnafisalmukhdi1.github.io/cdn/works/spp.jpeg
title: Sang Penyampai Pesan
desc: Sang Penyampai Pesan adalah trilogi cerpen fiksi penggemar–tidak termasuk prolog–untuk seseorang yang seharusnya muncul di dunia maya.
---
---
layout: story
img: https://mnafisalmukhdi1.github.io/cdn/works/spp.jpeg
title: Sang Penyampai Pesan
desc: Sang Penyampai Pesan adalah trilogi cerpen fiksi penggemar–tidak termasuk prolog–untuk seseorang yang seharusnya muncul di dunia maya.
---
<ul>
{% for file in site.pages %}
{% if file.dir == 'sang-penyampai-pesan' and file.title != "index.md" %}
<li><a href="{{ file.url }}">{{ file.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
