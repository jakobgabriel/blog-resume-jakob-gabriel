---
layout: home
title: Home
sitemap: false
---

<section class="text-center mb-12" data-aos="fade-down">
  <img src="{{ site.logo_light }}" alt="{{ site.title }}" class="mx-auto rounded-full w-32 h-32 mb-4" />
  <h1 class="text-4xl font-bold mb-2">{{ site.short_title | default: site.title }}</h1>
  <p class="text-lg text-gray-700 mb-4">{{ site.tagline | default: site.description }}</p>
  <div class="space-x-2">
    <a href="/resume-english/" class="btn btn-primary">Resume (EN)</a>
    <a href="/lebenslauf-deutsch/" class="btn btn-outline">Lebenslauf (DE)</a>
  </div>
</section>

<section class="grid grid-cols-1 sm:grid-cols-2 gap-6" data-aos="fade-up">
  {% for section in site.data.home_sections %}
  <a href="{{ section.url | relative_url }}" class="card flex flex-col items-center p-6 rounded-2xl bg-white">
    <img src="{{ section.icon }}" alt="{{ section.label }}" class="w-12 h-12 mb-3" />
    <span class="font-semibold">{{ section.label }}</span>
  </a>
  {% endfor %}
</section>

<!-- Optional fallback quick links for no-CSS or small screens -->
<ul class="list-disc list-inside md:hidden mt-8">
  {% for section in site.data.home_sections %}
  <li><a href="{{ section.url | relative_url }}">{{ section.label }}</a></li>
  {% endfor %}
</ul>

<p class="mt-6 text-sm text-gray-500">Last updated: {{ "now" | date: "%B %Y" }}</p>