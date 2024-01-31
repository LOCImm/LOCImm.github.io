---
title: "Meetings"
layout: gridlay
excerpt: "ANR-LOCImm -- Meetings"
sitemap: false
permalink: /Meetings
---

# Webinars

## <u>Multimodal journal club and 3D pre-clinical discussions</u>
- We discuss a **multimodal analysis article**.


### Some tips on Multimodal sessions and reading groups: 
- **For the "Guru" to lead a Multimodal session**: [link](http://muratbuffalo.blogspot.fr/2015/05/how-to-run-effective-paper-reading.html)
- **For all**: [link](http://muratbuffalo.blogspot.fr/2013/07/how-i-read-research-paper.html)

### List of coming Multimodal journal club session

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

## <u>3D pre-clinical brain tumor meeting</u>
- In the 3D pre-clinical meetings we discuss methods and new approaches to analyze 3D brain tumor data.

### List of 3D pre-clinical brain tumors meetings

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
  <p><strong><a href="{{ Meetings.recordlink.url }}">{{ Meetings.recordlink.display }}</a></strong></p>
  <p><strong><a href="{{ Meetings.slideslink.url1 }}">{{ Meetings.slideslink.display1 }}</a></strong></p>
  <p><strong><a href="{{ Meetings.slideslink.url2 }}">{{ Meetings.slideslink.display2 }}</a></strong></p>
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
