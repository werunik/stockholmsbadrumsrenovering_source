---
layout: testimonial
title: Badrumsrenovering Stockholm rekommendation
date: 2016-08-29 15:54:10 +0200
class: testimonial-page
description: Många som anlitar oss har blivit rekommenderade av våra kunder. De visar att de uppskattar vårt arbete och det kommer du garanterat också att göra.
permalink: /rekommendationer/
redirect_from:
  - /rekommendationer/www.kmliving.se/badrumsrenovering/
---
<section class="grid-container">
  {% assign rekommendationer = (site.rekommendationer | sort: 'date') | reverse %}
  {% for rekommendation in rekommendationer %}
  <div class="col-2">
    <div class="testimonial block">
      <figure class="{% if rekommendation.main_image %}main_image{% else %}icon_towel{% endif %}">
        <a href="{{ rekommendation.url | prepend: site.baseurl }}" title="{{ rekommendation.title | escape }}">
          <amp-img class="img-responsive img-grid" placeholder
            src="{% if rekommendation.main_image %}{{ rekommendation.main_image }}{% else %}{{ site.icon_towel }}{% endif %}"
            layout="responsive" width="360" height="216"
            alt="{{ rekommendation.title }}">
          </amp-img>
        </a>
      </figure>
      <div class="testimonial-content">
        <h3><a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}" title="{{ rekommendation.title | escape }}">{{ rekommendation.title | escape }}</a></h3>
        <p class="testimonial-client">{{ rekommendation.kund }}</p>
        <a class="testimonial-more" href="{{ rekommendation.url | prepend: site.baseurl }}" title="{{ rekommendation.title | escape }}">Se mer</a>
      </div>
    </div>
  </div>
  {% endfor %}
</section>