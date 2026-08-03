---
layout: posts
title: Articles
permalink: /articles/
entries_layout: grid
header:
  overlay_image: /Assets/4SWallpaper.jpg
  overlay_filter: 0.4
---

<h1>Articles</h1>

<p>
Thoughts on counseling, meaning, relationships,
and personal growth.
</p>


<div class="article-grid">


{% for article in site.posts %}


<article class="article-card">


<img src="{{ article.image }}"
     alt="{{ article.title }}">


<div class="card-content">


<div class="article-category">

{{ article.category }}

</div>


<h2>

<a href="{{ article.url }}">

{{ article.title }}

</a>

</h2>


<div class="article-meta">

{{ article.date | date: "%B %d, %Y" }}
•
{{ article.reading_time }}

</div>


<p>

{{ article.excerpt }}

</p>


<a href="{{ article.url }}">

Read Article →

</a>


</div>


</article>


{% endfor %}


</div>

Notice what happened:
