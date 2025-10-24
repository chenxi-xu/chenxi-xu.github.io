---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}

{% for category_hash in site.teaching_category %}
{% assign category_name = category_hash[0] %}
{% assign category_info = category_hash[1] %}

{% assign category_posts = site.teaching | where: "category", category_name %}

{% if category_posts.size > 0 %}
<h2 class="archive__subtitle">{{ category_info.title }}</h2>
{% for post in category_posts %}
{% include archive-single.html %}
{% endfor %}
{% endif %}
{% endfor %}
