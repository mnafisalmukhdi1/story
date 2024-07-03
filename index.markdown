---
layout: main
title: "Indeks"
---
<h1 class="text-2xl space-y-auto dark:text-white">Indeks</h1>
{% assign categories = site.data.books | map: 'category' | uniq %}
{% for category in categories %}
<section>
<h2 class="text-xl dark:text-white">{{ category }}</h2>
<div class="relative flex flex-wrap p-3 gap-8">
      {% for book in site.data.books %}
        {% if book.category == category %}
        <div class="max-w-lg shrink-0 snap-center">
            <a href="{{book.url}}">
                <img class="aspect-[9/14] w-40 shrink-0 rounded-lg bg-white object-cover shadow-xl" src="{{book.cover}}" alt="{{book.title}}">
                <h3 class="block truncate w-40 dark:text-white">{{book.title}}</h3>
            </a>
        </div>
        {% endif %}
      {% endfor %}
</div>
</section>
{% endfor %}
