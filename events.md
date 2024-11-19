---
layout: page
title: Events
permalink: /events/
---
<h1 class="heading">Events</h1>
{% for event in site.events %}
<section class='event'>
  <h2><a href="{{ event.url | prepend: site.baseurl }}">{{ event.title }}</a></h2>
  <p>
    <a href='{{ event.url | prepend: site.baseurl }}'><img src='{{ site.baseurl }}{% include directory url=event.url %}{{ event.image }}' alt='{{ event.title }}'></a>
  </p>
  <p>
  {% if event.begin != "" and event.begin != nil %}Beginn: {{ event.begin | date: "%m.%d.%Y %H:%M" }}{% endif %} 
  </p>
  <p>
  {% if event.end != "" and event.end != nil %}Ende: {{ event.end | date: "%m.%d.%Y %H:%M" }}{% endif %} 
  </p>
</section>{% endfor %}
