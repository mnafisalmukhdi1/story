---
layout: main
title: "Indeks"
---
<h1 class="text-2xl space-y-auto dark:text-white">Indeks</h1>
{% assign categories = site.data.books | map: 'category' | uniq %}
{% for category in categories %}
<section>
<h2 class="text-xl dark:text-white">{{ category }}</h2>
<div class="relative flex flex-wrap items-start p-3 gap-3 sm:gap-6 md:gap-8">
      {% for book in site.data.books %}
        {% if book.category == category %}
        <div class="w-[calc(50%-0.75rem)] max-w-[10rem] shrink-0 snap-center sm:w-auto sm:max-w-lg">
            <a class="block" href="{{book.url}}">
                <img class="aspect-[9/14] w-full max-w-[10rem] shrink-0 rounded-lg bg-white object-cover shadow-xl sm:w-40" src="{{book.cover}}" alt="{{book.title}}">
                <h3 class="block truncate w-full max-w-[10rem] dark:text-white sm:w-40">{{book.title}}</h3>
            </a>
        </div>
        {% endif %}
      {% endfor %}
</div>
</section>
{% endfor %}
