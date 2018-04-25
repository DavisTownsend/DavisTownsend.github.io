---
layout: page
title: "Hi, I'm Davis"
subtitle: Python Data Analysis / Business Analyst / Data Simplifyer
css: "/css/index.css"
meta-title: "Davis Townsend - Business Analyst"
meta-description: "Business Analyst at EA. MS Business Analytics and BA Economics from UT Austin"
bigimg:
  - "/img/big-imgs/altitude-blue-sky-clouds-530158.jpg" : "test"
  - "/img/big-imgs/bridge-california-cliff-7653.jpg" : ""
  - "/img/big-imgs/cc0-desktop-backgrounds-fog-7919.jpg" : ""
  - "/img/big-imgs/cliffs-climbing-clouds-746421.jpg" : ""
---

<div class="list-filters">
  <a href="/" class="list-filter">All posts</a>
  <a href="/popular" class="list-filter">Most Popular</a>
  <span class="list-filter filter-selected">Tutorials</span>
  <a href="/tags" class="list-filter">Index</a>
</div>

<div class="posts-list">
  {% for post in site.tags.tutorial %}
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
