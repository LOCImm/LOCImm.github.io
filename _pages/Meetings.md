---
title: "Meetings"
layout: gridlay
excerpt: "ANR-LOCImm -- Meetings"
sitemap: false
permalink: /Meetings
---

# Webinars

In the context of AI Chair Oceanix and AI4OAC project, we organize a webinar every third Wednesday of the month, starting in October 2020. When possible, additional links with a video record of the webinar will be provided.

**Zoom link for Herve Claustre's webinar, June 15, 2pm**: [link](https://imt-atlantique.zoom.us/j/5513937378?pwd=L3pRYlFiODZOeG9paWMvZXE5Z2pZQT09)

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ Meetings.image }}" class="img-responsive" width="33%" style="float: left" />
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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ Meetings.image }}" class="img-responsive" width="33%" style="float: left" />
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

