---
layout: page
title: Badrumsrenovering Stockholm Bloggen
date: 2016-08-29 15:54:10 +0200
class: blog
description: Bloggen för dig som älskar badrum! Följ oss här, på Instagram (@km.living) och Facebook (www.facebook.com/KMLivingConstructionAB)
permalink: /bloggen/
redirect_from:
  - /bloggen/2016/third-post
  - /bloggen/2016/welcome-to-jekyll
  - /bloggen/2016/second-post
---
<section class="center p-b-90px" itemscope="" itemtype="http://schema.org/Blog">
  <div class="container">
  {% assign posts = (site.posts | sort: 'date') %}
  {% for post in posts %}
    <article class="post one" itemprop="blogPost" itemscope="" itemtype="http://schema.org/BlogPosting">
      <link itemprop="mainEntityOfPage" href="{{ site.url }}{{ post.url | replace:'index.html','' }}">
      <meta itemprop="description" content="{{ post.description | strip_html | truncatewords: 40 }}">
      <meta itemprop="keywords" content="{{ post.categories | join: ',' }}" />
      <meta itemprop="datePublished" content="{{ post.date | date: '%Y-%m-%d' }}">
      <meta itemprop="dateModified" content="{{ post.date | date: '%Y-%m-%d' }}">
      <span itemprop="author" itemscope itemtype="https://schema.org/Person">
        <meta itemprop="name" content="{{ site.organization_name }}">
      </span>
      <span itemscope itemprop="publisher" itemtype="http://schema.org/Organization">
        <meta itemprop="name" content="{{ site.organization_name }}">
        <span itemprop="logo" itemscope itemtype="http://schema.org/ImageObject">
          <meta itemprop="url" content="{{ site.logo_jpg }}">
        </span>
      </span>
      <span itemprop="image" itemscope itemtype="https://schema.org/ImageObject">
        <meta itemprop="url" content="{% if page.main_image %}{{ page.main_image }}{% else %}{{ site.og_image }}{% endif %}">
        <meta itemprop="width" content="800">
        <meta itemprop="height" content="800">
      </span>
      <h2>
        <a href="{{ post.url }}" itemprop="url">
          <span itemprop="headline name">{{ post.title }}</span>
        </a>
      </h2>
      <div class="entry" itemprop="description">
        {{ post.content | strip_html | truncatewords: 40 }}
      </div>
      <a href="{{ post.url }}" itemprop="url" class="read-more">Läs mer</a>
    </article>
  {% endfor %}
</div>
</section>