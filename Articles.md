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
        <input type="text" id="article-search" placeholder="Search articles..." aria-label="Search articles">
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
        <a href="/articles/the-quiet-work-of-showing-up.html" class="featured-card">
          <img src="/assets/images/featured-placeholder.jpg" alt="Featured article image">
          <div class="card-content">
            <span class="article-category parenting">Parenting</span>
            <h3>The Quiet Work of Showing Up</h3>
            <span class="article-meta">6 min read</span>
            <p class="article-description">Some of the most important parenting happens in the moments nobody's watching. A look at what consistency actually asks of us.</p>
          </div>
        </a>
      </section>

      <section class="latest-articles">
        <h2>Latest Articles</h2>
        <div class="article-grid" id="article-grid">

          <a href="/articles/why-we-need-both-structure-and-play.html" class="article-card" data-category="parenting" data-title="Why We Need Both Structure and Play">
            <img src="/assets/images/article-placeholder-1.jpg" alt="Why We Need Both Structure and Play">
            <div class="card-content">
              <span class="article-category parenting">Parenting</span>
              <h3>Why We Need Both Structure and Play</h3>
              <span class="article-meta">5 min read</span>
              <p class="article-description">Kids don't need one or the other — they need both, in the right proportions, at the right moments.</p>
            </div>
          </a>

          <a href="/articles/finding-meaning-in-ordinary-days.html" class="article-card" data-category="meaning" data-title="Finding Meaning in Ordinary Days">
            <img src="/assets/images/article-placeholder-2.jpg" alt="Finding Meaning in Ordinary Days">
            <div class="card-content">
              <span class="article-category meaning">Meaning</span>
              <h3>Finding Meaning in Ordinary Days</h3>
              <span class="article-meta">7 min read</span>
              <p class="article-description">Meaning rarely arrives as a lightning bolt. Usually it's stitched together from small, repeated choices.</p>
            </div>
          </a>

          <a href="/articles/the-creative-habit-nobody-tells-you-about.html" class="article-card" data-category="creativity" data-title="The Creative Habit Nobody Tells You About">
            <img src="/assets/images/article-placeholder-3.jpg" alt="The Creative Habit Nobody Tells You About">
            <div class="card-content">
              <span class="article-category creativity">Creativity</span>
              <h3>The Creative Habit Nobody Tells You About</h3>
              <span class="article-meta">4 min read</span>
              <p class="article-description">The habit that matters most isn't inspiration — it's showing up to the blank page on the boring days.</p>
            </div>
          </a>

          <a href="/articles/what-my-kids-taught-me-about-patience.html" class="article-card" data-category="parenting" data-title="What My Kids Taught Me About Patience">
            <img src="/assets/images/article-placeholder-4.jpg" alt="What My Kids Taught Me About Patience">
            <div class="card-content">
              <span class="article-category parenting">Parenting</span>
              <h3>What My Kids Taught Me About Patience</h3>
              <span class="article-meta">6 min read</span>
              <p class="article-description">I thought I was teaching them. Turns out the lessons went both directions.</p>
            </div>
          </a>

          <a href="/articles/sitting-with-uncertainty.html" class="article-card" data-category="meaning" data-title="Sitting With Uncertainty">
            <img src="/assets/images/article-placeholder-5.jpg" alt="Sitting With Uncertainty">
            <div class="card-content">
              <span class="article-category meaning">Meaning</span>
              <h3>Sitting With Uncertainty</h3>
              <span class="article-meta">8 min read</span>
              <p class="article-description">Not every question needs an answer right away. Some just need company while you carry them.</p>
            </div>
          </a>

          <a href="/articles/making-space-for-imperfect-work.html" class="article-card" data-category="creativity" data-title="Making Space for Imperfect Work">
            <img src="/assets/images/article-placeholder-6.jpg" alt="Making Space for Imperfect Work">
            <div class="card-content">
              <span class="article-category creativity">Creativity</span>
              <h3>Making Space for Imperfect Work</h3>
              <span class="article-meta">5 min read</span>
              <p class="article-description">Perfectionism doesn't protect your best work — it usually just keeps it from ever getting made.</p>
            </div>
          </a>

        </div>

        <p id="no-results" class="no-results" style="display:none;">No articles match your search.</p>
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
