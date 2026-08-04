---
layout: single          # Defines the layout template (single page view)
title: Articles         # Sets the page title in browser tabs/headers
permalink: /articles/   # Sets the explicit URL path (yoursite.com/articles/)
author_profile: false   # Disables the side author bio panel
sidebar: false          # Disables the standard sidebar layout
header:
  overlay_image: /Assets/4SWallpaper.jpg
  overlay_filter: 0.4                  # Darkens header image by 40% for text legibility
---

<!-- ======================================================================= -->
<!-- SECTION 2: HTML STRUCTURE                                               -->
<!-- Page layout, header content, filter UI, and article cards               -->
<!-- ======================================================================= -->

<!-- Main page structural container wrappers -->
<div class="custom-page">
  <div class="wrap">
    <div class="content">

      <!-- --- SECTION 2A: Page Header --- -->
      <p class="eyebrow">Writing</p> <!-- Small, decorative category label above title -->
      <h1>Articles</h1>          <!-- Main page heading -->
      <p class="lede">Reflections on parenting, meaning, and creativity — thoughts I hope are useful to you as much as they've been to me.</p> <!-- Introductory subheader -->

      <!-- --- SECTION 2B: Search Bar --- -->
      <div class="article-search-bar">
        <!-- Text box used by JavaScript to filter articles by title -->
        <input type="text" id="article-search" placeholder="Search articles..." aria-label="Search articles">
      </div>

      <!-- --- SECTION 2C: Category Filter Buttons --- -->
      <!-- 'data-category' attributes are read by JS to filter items -->
      <div class="category-filters" id="category-filters">
        <button class="category-filter-btn active" data-category="all">All</button>
        <button class="category-filter-btn" data-category="parenting">Parenting</button>
        <button class="category-filter-btn" data-category="meaning">Meaning</button>
        <button class="category-filter-btn" data-category="creativity">Creativity</button>
      </div>

      <hr class="divider"> <!-- Visual horizontal separator line -->

      <!-- --- SECTION 2D: Featured Article (Static - unaffected by search) --- -->
      <section class="featured-article">
        <h2>Featured</h2>
        <a href="/Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="featured-card">
          <img src="/Assets/therabbitlistened.jpg" alt="Featured article image">
          <div class="card-content">
            <span class="article-category parenting">Parenting</span>
            <h3>The Quiet Work of Showing Up</h3>
            <span class="article-meta">6 min read</span>
            <p class="article-description">Some of the most important parenting happens in the moments nobody's watching. A look at what consistency actually asks of us.</p>
          </div>
        </a>
      </section>

      <!-- --- SECTION 2E: Dynamic Article Grid (Targeted by JS) --- -->
      <section class="latest-articles">
        <h2>Latest Articles</h2>
        <div class="article-grid" id="article-grid">

          <!-- Individual Article Card 1 -->
          <!-- 'data-category' and 'data-title' allow fast client-side filtering via JS -->
          <a href="/Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="parenting" data-title="Why We Need Both Structure and Play">
            <img src="/Assets/therabbitlistened.jpg" alt="Why We Need Both Structure and Play">
            <div class="card-content">
              <span class="article-category parenting">Parenting</span>
              <h3>Why We Need Both Structure and Play</h3>
              <span class="article-meta">5 min read</span>
              <p class="article-description">Kids don't need one or the other — they need both, in the right proportions, at the right moments.</p>
            </div>
          </a>

          <!-- Individual Article Card 2 -->
          <a href="Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="meaning" data-title="Finding Meaning in Ordinary Days">
            <img src="Assets/therabbitlistened.jpg" alt="Finding Meaning in Ordinary Days">
            <div class="card-content">
              <span class="article-category meaning">Meaning</span>
              <h3>Finding Meaning in Ordinary Days</h3>
              <span class="article-meta">7 min read</span>
              <p class="article-description">Meaning rarely arrives as a lightning bolt. Usually it's stitched together from small, repeated choices.</p>
            </div>
          </a>

          <!-- Individual Article Card 3 -->
          <a href="Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="creativity" data-title="The Creative Habit Nobody Tells You About">
            <img src="Assets/therabbitlistened.jpg" alt="The Creative Habit Nobody Tells You About">
            <div class="card-content">
              <span class="article-category creativity">Creativity</span>
              <h3>The Creative Habit Nobody Tells You About</h3>
              <span class="article-meta">4 min read</span>
              <p class="article-description">The habit that matters most isn't inspiration — it's showing up to the blank page on the boring days.</p>
            </div>
          </a>

          <!-- Individual Article Card 4 -->
          <a href="Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="parenting" data-title="What My Kids Taught Me About Patience">
            <img src="Assets/therabbitlistened.jpg" alt="What My Kids Taught Me About Patience">
            <div class="card-content">
              <span class="article-category parenting">Parenting</span>
              <h3>What My Kids Taught Me About Patience</h3>
              <span class="article-meta">6 min read</span>
              <p class="article-description">I thought I was teaching them. Turns out the lessons went both directions.</p>
            </div>
          </a>

          <!-- Individual Article Card 5 -->
          <a href="Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="meaning" data-title="Sitting With Uncertainty">
            <img src="Assets/therabbitlistened.jpg" alt="Sitting With Uncertainty">
            <div class="card-content">
              <span class="article-category meaning">Meaning</span>
              <h3>Sitting With Uncertainty</h3>
              <span class="article-meta">8 min read</span>
              <p class="article-description">Not every question needs an answer right away. Some just need company while you carry them.</p>
            </div>
          </a>

          <!-- Individual Article Card 6 -->
          <a href="Articles/2026-07-16-Lessons-from-The-Rabbit-Listened.md" class="article-card" data-category="creativity" data-title="Making Space for Imperfect Work">
            <img src="Assets/therabbitlistened.jpg" alt="Making Space for Imperfect Work">
            <div class="card-content">
              <span class="article-category creativity">Creativity</span>
              <h3>Making Space for Imperfect Work</h3>
              <span class="article-meta">5 min read</span>
              <p class="article-description">Perfectionism doesn't protect your best work — it usually just keeps it from ever getting made.</p>
            </div>
          </a>

        </div>

        <!-- Fallback message shown by JS if zero cards match search/filters -->
        <p id="no-results" class="no-results" style="display:none;">No articles match your search.</p>
      </section>

    </div>
  </div>
</div>

<!-- ======================================================================= -->
<!-- SECTION 3: JAVASCRIPT                                                   -->
<!-- Client-side filtering logic for search input and category buttons       -->
<!-- ======================================================================= -->
<script>
(function () {
  // --- Step 3A: Target HTML Elements ---
  const searchInput = document.getElementById('article-search');       // Search box
  const categoryButtons = document.querySelectorAll('.category-filter-btn'); // Filter buttons list
  const cards = document.querySelectorAll('.article-card');             // All dynamic article cards
  const noResults = document.getElementById('no-results');             // Empty state message element
  
  let activeCategory = 'all'; // State variable tracking current active category

  // --- Step 3B: Primary Filtering Function ---
  function applyFilters() {
    const query = searchInput.value.trim().toLowerCase(); // Get clean, lowercase search string
    let visibleCount = 0;                                 // Reset visible card tracker

    // Loop through every article card to test visibility
    cards.forEach(function (card) {
      const category = card.getAttribute('data-category');             // Get card's category
      const title = card.getAttribute('data-title').toLowerCase();      // Get card's title

      // Match check 1: Category matches selected filter (or category is 'all')
      const matchesCategory = activeCategory === 'all' || category === activeCategory;
      // Match check 2: Title contains search input string (or search is empty)
      const matchesSearch = query === '' || title.includes(query);

      // Card is visible only if BOTH conditions pass
      const show = matchesCategory && matchesSearch;
      
      card.style.display = show ? '' : 'none'; // Toggle card display state in DOM
      if (show) visibleCount++;                // Increment visible counter
    });

    // Display 'No articles found' message if 0 cards match current criteria
    noResults.style.display = visibleCount === 0 ? 'block' : 'none';
  }

  // --- Step 3C: Event Listeners ---

  // Trigger search filter automatically whenever the user types in the input box
  searchInput.addEventListener('input', applyFilters);

  // Attach click listener to each category button
  categoryButtons.forEach(function (btn) {
    btn.addEventListener('click', function () {
      // Clear 'active' styling class from all buttons
      categoryButtons.forEach(function (b) { b.classList.remove('active'); });
      
      // Highlight clicked button
      btn.classList.add('active');
      
      // Update active category state and execute filter check
      activeCategory = btn.getAttribute('data-category');
      applyFilters();
    });
  });
})();
</script>
