---
layout: page
title: "Hi, I'm Davis"
subtitle: Python Data Analysis / Business Analyst / Data Simplifyer
css: "/css/index.css"
meta-title: "Davis Townsend - Business Analyst"
meta-description: "Business Analyst at EA. MS Business Analytics and BA Economics from UT Austin"
bigimg:
  - "/img/big-imgs/abstract-art-blur-373543.jpg" : ""
  - "/img/big-imgs/airport-bank-board-534216.jpg" : ""
  - "/img/big-imgs/altitude-architecture-business-cabinet-325229.jpg" : ""
  - "/img/big-imgs/black-coffee-cellphone-coffee-860379.jpg" : ""
  - "/img/big-imgs/bridge-california-cliff-7653.jpg" : ""
  - "/img/big-imgs/altitude-blue-sky-clouds-530158.jpg" : ""
  - "/img/big-imgs/city-hd-wallpaper-lights-5443.jpg" : ""
  - "/img/big-imgs/cc0-desktop-backgrounds-fog-7919.jpg" : ""
  - "/img/big-imgs/clouds-dawn-dusk-46253.jpg" : ""
  - "/img/big-imgs/clouds-daylight-forest-592077.jpg" : ""
  - "/img/big-imgs/imgix-391813-unsplash.jpg" : ""
  - "/img/big-imgs/jesse-orrico-60373-unsplash.jpg" : ""
  - "/img/big-imgs/markus-spiske-507983-unsplash.jpg" : ""
  - "/img/big-imgs/nasa-43563-unsplash.jpg" : ""
  - "/img/big-imgs/nathan-anderson-143022-unsplash.jpg" : ""
  - "/img/big-imgs/cliffs-climbing-clouds-746421.jpg" : ""
  - "/img/big-imgs/spacex-549326-unsplash.jpg" : ""
---

<div class="list-filters">
  <a href="/" class="list-filter">All posts</a>
  <span class="list-filter filter-selected">Most Popular</span>
  <a href="/tutorials" class="list-filter">Tutorials</a>
  <a href="/tags" class="list-filter">Index</a>
</div>

<div class="posts-list">
  {% for post in site.tags.popular %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>
