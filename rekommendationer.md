---
layout: testimonial
title: Nöjda kunder
date: 2016-08-29 15:54:10 +0200
class: testimonial-page
headline: Många som anlitar oss har blivit rekommenderade av våra kunder. De visar att de uppskattar vårt arbete och det kommer du garanterat också att göra.
description: Många som anlitar oss har blivit rekommenderade av våra kunder. De visar att de uppskattar vårt arbete och det kommer du garanterat också att göra.
permalink: /rekommendationer/
---
<div class="flex one two-800">
    {% assign rekommendationer = (site.rekommendationer | sort: 'date') | reverse %}
    {% for rekommendation in rekommendationer %}
      <div class="block">
        <div class="flex one testimonial">
          <h4><a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">{{ rekommendation.title | escape }}</a></h4>
          <blockquote>{{ rekommendation.excerpt | strip_html | truncatewords: 50 }}</blockquote>
          <div class="testimonial-client">— {{ rekommendation.kund }}</div>
          <a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">Läs mer</a>
        </div>
      </div>
    {% endfor %}
  </div>