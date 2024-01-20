---
title: "Meetings"
layout: gridlay
excerpt: "AI Chair OceaniX - Meetings"
sitemap: false
permalink: /Meetings
---

# Multimodal journal club

Multimodal is a journal club to discuss papers of interest while eating pizzas.
<!--**Zoom conference for session on Nov. 25**: [link](https://zoom.us/j/94354512890?pwd=cHNCMlVISVRnZjFuN29TV2d2a1R3UT09)-->

## Some tips on Multimodal journal club sessions and reading groups: 
- **For the "Guru" to lead a Multimodal journal club session**: [link](http://muratbuffalo.blogspot.fr/2015/05/how-to-run-effective-paper-reading.html)
- **For all**: [link](http://muratbuffalo.blogspot.fr/2013/07/how-i-read-research-paper.html)

## List of coming Multimodal journal club session

{% assign number_printed = 0 %}
{% for Meetings in site.data.Meetingslist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if Meetings.highlight == 1 %}
{% if Meetings.codetype == 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ Meetings.title }}</pubtit>
  <p>{{ Meetings.date }} <br> </p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/domino_pic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ Meetings.description }}</p>
  <p><em>{{ Meetings.authors }}</em></p>
  <p><strong><a href="{{ Meetings.link.url }}">{{ Meetings.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ Meetings.news1 }}</strong></p>
  <p> {{ Meetings.news2 }}</p>
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


## List of previous Multimodal journal club session

{% assign number_printed = 0 %}
{% for Meetings in site.data.Meetingslist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if Meetings.highlight == 1 %}
{% if Meetings.codetype == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ Meetings.title }}</pubtit>
  <p>{{ Meetings.date }} <br></p>
  <img src="{{ site.url }}{{ site.baseurl }}/images/domino_pic/{{ domino.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ Meetings.description }}</p>
  <p><em>{{ Meetings.authors }}</em></p>
  <p><strong><a href="{{ Meetings.link.url }}">{{ Meetings.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ Meetings.news1 }}</strong></p>
  <p> {{ Meetings.news2 }}</p>
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

