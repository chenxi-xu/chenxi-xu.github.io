---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

{% for category_hash in site.publication_category %}
{% assign category_name = category_hash[0] %}
{% assign category_info = category_hash[1] %}

{% assign category_posts = site.research | where: "category", category_name | reverse %}

{% if category_posts.size > 0 %}
## {{ category_info.title }} {:.archive__subtitle}
{% for post in category_posts %}
{% include archive-single.html %}
{% endfor %}
{% endif %}
{% endfor %}
