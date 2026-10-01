---
layout: home
title: "Indeks"
---
{% assign categories = site.data.books | map: 'category' | uniq %}
{% for category in categories %}
<section class="mb-14 last:mb-0">
  <h2 class="text-xs font-medium uppercase tracking-[0.2em] text-gray-500 dark:text-slate-400">{{ category }}</h2>
  <div class="mt-6 grid grid-cols-2 gap-x-6 gap-y-10 sm:grid-cols-3 lg:grid-cols-4">
    {% for book in site.data.books %}
      {% if book.category == category %}
      <a href="{{book.url}}" class="group block max-w-[10rem]">
        <img class="aspect-[9/14] w-full rounded-md border border-gray-100 bg-white object-cover transition duration-300 group-hover:-translate-y-1 group-hover:shadow-lg dark:border-slate-800" src="{{book.cover}}" alt="{{book.title}}" loading="lazy">
        <h3 class="mt-3 truncate text-sm font-medium text-gray-800 transition-colors group-hover:text-gray-950 dark:text-slate-200 dark:group-hover:text-white">{{book.title}}</h3>
      </a>
      {% endif %}
    {% endfor %}
  </div>
</section>
{% endfor %}
