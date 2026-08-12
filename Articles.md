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

      <section class="featured-article">
        <h2>Featured</h2>
        <!-- Corrected link from .md to Jekyll's built HTML route -->
        <a href="2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="featured-card">
          <img src="/Assets/therabbitlistened.jpg" alt="Featured article image">
          <div class="card-content">
            <span class="article-category parenting">Parenting</span>
            <h3>Lessons from The Rabbit Listened</h3>
            <span class="article-meta">6 min read</span>
            <p class="article-description">Some of the most important parenting happens in the moments nobody's watching. A look at what consistency actually asks of us.</p>
          </div>
        </a>
      </section>

      <section class="latest-Articles">
        <h2>Latest Articles</h2>
        <div class="article-grid" id="article-grid">

          <a href="_posts/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="parenting" data-title="Lessons from The Rabbit Listened">
            <img src="/Assets/therabbitlistened.jpg" alt="Lessons from The Rabbit Listened">
            <div class="card-content">
              <span class="article-category parenting">Parenting</span>
              <h3>Lessons from The Rabbit Listened</h3>
              <span class="article-meta">5 min read</span>
              <p class="article-description">Kids don't need one or the other — they need both, in the right proportions, at the right moments.</p>
            </div>
          </a>

        </div>

        <p id="no-results" class="no-results" style="display:none;">No Articles match your search.</p>
      </section>

    </div>
  </div>
</div>

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
