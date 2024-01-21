---
title: "3D pre-clinical"
layout: gridlay
excerpt: "ANR-LOCimm - 3D pre-clinical"
sitemap: false
permalink: /3D_pre-clinical
---

## 3D pre-clinical

3D pre-clinical is a journal club around the analysis and brainstorming of 3D data in animal models with brain tumors.

## List of coming Multimodal journal club session

*Work in progress*

{% assign number_printed = 0 %}
{% for 3D in site.data.3D %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if 3D.highlight == 1 %}
{% if 3D.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ 3D.title }}</pubtit>
  <p>{{ 3D.date }} <br> </p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ 3D.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ 3D.description }}</p>
  <p><em>{{ 3D.authors }}</em></p>
  <p><strong><a href="{{ 3D.link.url }}">{{ 3D.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ 3D.news1 }}</strong></p>
  <p> {{ 3D.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


