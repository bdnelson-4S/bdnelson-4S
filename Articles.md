---
layout: single
title: Articles
permalink: /articles/
author_profile: false
sidebar: false
header:
  overlay_image: /Assets/4SWallpaper.jpg
  overlay_filter: 0.4
---

<div class="custom-page">
  <div class="wrap">
    <div class="content">

      <p class="eyebrow">Writing</p>
      <h1>Articles</h1>
      <p class="lede">Reflections on parenting, meaning, and creativity — thoughts I hope are useful to you as much as they've been to me.</p>

      <div class="article-search-bar">
        <input type="text" id="article-search" placeholder="Search Articles..." aria-label="Search Articles">
      </div>

      <div class="category-filters" id="category-filters">
        <button class="category-filter-btn active" data-category="all">All</button>
        <button class="category-filter-btn" data-category="parenting">Parenting</button>
        <button class="category-filter-btn" data-category="meaning">Meaning</button>
        <button class="category-filter-btn" data-category="creativity">Creativity</button>
      </div>

      <hr class="divider">

      {% assign featured = site.posts | first %}
      {% if featured %}
      <section class="featured-article">
        <h2>Featured</h2>
        <a href="{{ featured.url }}" class="featured-card">
          <img src="{{ featured.teaser | default: featured.header.overlay_image }}" alt="{{ featured.title }}">
          <div class="card-content">
            <span class="article-category {{ featured.categories | first | downcase }}">{{ featured.categories | first }}</span>
            <h3>{{ featured.title }}</h3>
            <span class="article-meta">{{ featured.content | number_of_words | divided_by: 200 | at_least: 1 }} min read</span>
            <p class="article-description">{{ featured.excerpt | strip_html | truncate: 140 }}</p>
          </div>
        </a>
      </section>
      {% endif %}

      <section class="latest-Articles">
        <h2>Latest Articles</h2>
        <div class="article-grid" id="article-grid">

          {% for post in site.posts %}
          <a href="{{ post.url }}" class="article-card" data-category="{{ post.categories | first | downcase }}" data-title="{{ post.title }}">
            <img src="{{ post.teaser | default: post.header.overlay_image }}" alt="{{ post.title }}">
            <div class="card-content">
              <span class="article-category {{ post.categories | first | downcase }}">{{ post.categories | first }}</span>
              <h3>{{ post.title }}</h3>
              <span class="article-meta">{{ post.content | number_of_words | divided_by: 200 | at_least: 1 }} min read</span>
              <p class="article-description">{{ post.excerpt | strip_html | truncate: 140 }}</p>
            </div>
          </a>
          {% endfor %}

        </div>

        <p id="no-results" class="no-results" style="display:none;">No Articles match your search.</p>
      </section>

    </div>
  </div>
</div>

<style>
  /* Grid: 2 columns, cards match featured-card proportions */
  .article-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 28px;
  }

  .article-card,
  .featured-card {
    display: flex;
    flex-direction: column;
    text-decoration: none;
    color: inherit;
    border-radius: 8px;
    overflow: hidden;
    background: var(--paper, #FBFAF7);
    border: 1px solid var(--line, #D7D3C4);
    transition: transform 0.15s ease, box-shadow 0.15s ease;
  }

  .article-card:hover,
  .featured-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.08);
  }

  .article-card img,
  .featured-card img {
    width: 100%;
    aspect-ratio: 16 / 9;
    object-fit: cover;
    display: block;
  }

  .article-card .card-content,
  .featured-card .card-content {
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .article-card h3,
  .featured-card h3 {
    margin: 0;
    font-size: 1.1rem;
    line-height: 1.3;
  }

  .article-card .article-description,
  .featured-card .article-description {
    margin: 0;
    font-size: 0.95rem;
    color: var(--ink-soft, #545E56);
    line-height: 1.5;
  }

  .article-category {
    display: inline-block;
    width: fit-content;
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    padding: 3px 10px;
    border-radius: 999px;
    background: var(--stone-deep, #E3E0D3);
    color: var(--ink, #2B332E);
  }

  .article-meta {
    font-size: 0.8rem;
    color: var(--ink-soft, #545E56);
  }

  @media (max-width: 700px) {
    .article-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<script>
(function () {
  const searchInput = document.getElementById('article-search');
  const categoryButtons = document.querySelectorAll('.category-filter-btn');
  const cards = document.querySelectorAll('.article-card');
  const noResults = document.getElementById('no-results');

  let activeCategory = 'all';

  function applyFilters() {
    const query = searchInput.value.trim().toLowerCase();
    let visibleCount = 0;

    cards.forEach(function (card) {
      const category = card.getAttribute('data-category');
      const title = card.getAttribute('data-title').toLowerCase();

      const matchesCategory = activeCategory === 'all' || category === activeCategory;
      const matchesSearch = query === '' || title.includes(query);

      const show = matchesCategory && matchesSearch;

      card.style.display = show ? '' : 'none';
      if (show) visibleCount++;
    });

    noResults.style.display = visibleCount === 0 ? 'block' : 'none';
  }

  searchInput.addEventListener('input', applyFilters);

  categoryButtons.forEach(function (btn) {
    btn.addEventListener('click', function () {
      categoryButtons.forEach(function (b) { b.classList.remove('active'); });
      btn.classList.add('active');
      activeCategory = btn.getAttribute('data-category');
      applyFilters();
    });
  });
})();
</script>
