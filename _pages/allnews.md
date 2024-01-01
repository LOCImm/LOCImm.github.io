---
title: "News"
layout: textlay
excerpt: "Dr Agusti Alentorn at Paris Brain Institute (ICM)."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br> {{ article.headline | markdownify}}</p>
{% endfor %}
