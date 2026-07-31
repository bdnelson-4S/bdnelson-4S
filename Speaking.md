---
layout: single
title: Speaking
permalink: /speaking/
header:
  overlay_image: /Assets/4SWallpaper.jpg
  overlay_filter: 0.4
---

<style>
  /* ==========================================================================
     1. GLOBAL PAGE CONTAINER & CSS VARIABLES
     ========================================================================== */
  #speaking-page {
    /* Color Palette Variables */
    --stone: #EFEDE4;
    --stone-deep: #E3E0D3;
    --ink: #2B332E;
    --ink-soft: #545E56;
    --sage: #6E7F63;
    --sage-deep: #3F4F3F;
    --clay: #B9855A;
    --clay-deep: #9C6E45;
    --line: #D7D3C4;
    --paper: #FBFAF7;

    /* Base Typography & Background */
    font-family: 'Work Sans', sans-serif;
    color: var(--ink);
    background: var(--stone);

    /* Full-Bleed Layout Override (Extends background across entire screen width) */
    margin: -1em -1em 0;
    padding: 0;
    max-width: none !important;
    width: 100vw !important;
    margin-left: calc(-50vw + 50%) !important;
    box-sizing: border-box;
  }

  /* Universal Box-Sizing (Prevents padding from causing horizontal scrolling) */
  #speaking-page *, 
  #speaking-page *::before, 
  #speaking-page *::after {
    box-sizing: inherit;
  }

  /* ==========================================================================
     2. PAGE LAYOUT WRAPPERS & CONTENT CENTERING
     ========================================================================== */
  /* Main Container (Sets max width and horizontal auto-margins for centering) */
  #speaking-page .wrap {
    width: 90%;
    max-width: 1100px;
    margin: 0 auto;
    padding: 48px 20px;
    position: relative;
  }

  /* Inner Content Alignment (Centers all inline text, headings, and dividers) */
  #speaking-page .content { 
    position: relative; 
    z-index: 1; 
    text-align: center;
  }

  /* ==========================================================================
     3. TYPOGRAPHY & TEXT ELEMENTS
     ========================================================================== */
  /* Eyebrow Label (Small uppercase text above main titles) */
  #speaking-page .eyebrow {
    font-size: 12.5px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--sage-deep);
    font-weight: 600;
    margin: 0 0 18px;
  }

  /* Main Title (Responsive clamp font size: scales smoothly between mobile and desktop) */
  #speaking-page h1 {
    font-family: 'Fraunces', serif;
    font-optical-sizing: auto;
    font-weight: 500;
    font-size: clamp(28px, 4vw, 40px);
    line-height: 1.25;
    letter-spacing: -0.01em;
    margin: 0 0 20px;
    color: var(--ink);
  }

  /* Section Headings */
  #speaking-page h2 {
    font-family: 'Fraunces', serif;
    font-optical-sizing: auto;
    font-weight: 500;
    font-size: clamp(20px, 3vw, 24px);
    line-height: 1.3;
    letter-spacing: -0.01em;
    margin: 0 0 16px;
    color: var(--ink);
  }

  /* Body / Lead Paragraphs (Centered block with restricted max-width for comfortable reading) */
  #speaking-page .lede {
    font-size: clamp(15px, 2vw, 17px);
    line-height: 1.65;
    color: var(--ink-soft);
    margin: 0 auto 16px auto;
    width: 100%;
    max-width: 750px;
  }

  /* Section Separator Lines */
  #speaking-page .divider {
    border: none;
    border-top: 1px solid var(--line);
    margin: 36px auto;
    max-width: 800px;
  }

  /* ==========================================================================
     4. TOPIC BUBBLES / CHIPS
     ========================================================================== */
  /* Topic List Container (Flexbox row with wrapping, centered horizontally) */
  #speaking-page .topic-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    list-style: none;
    padding: 0;
    margin: 20px auto;
    max-width: 850px;
  }

  /* Individual Topic Bubble Items */
  #speaking-page .topic-list li {
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 9px 16px;
    font-size: 14px;
    color: var(--ink);
    text-align: center;
  }

  /* ==========================================================================
     5. EXPERIENCE LIST
     ========================================================================== */
  /* Experience List Container */
  #speaking-page .experience-list {
    list-style: none;
    padding: 0;
    margin: 20px auto;
    max-width: 650px;
  }

  /* Experience Item (Centered flex row with top/bottom border dividers) */
  #speaking-page .experience-list li {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    padding: 14px 0;
    border-bottom: 1px solid var(--line);
    font-size: 16px;
    text-align: center;
  }

  /* Top border for the first list item */
  #speaking-page .experience-list li:first-child {
    border-top: 1px solid var(--line);
  }

  /* Bullet Dot Indicator before each item */
  #speaking-page .experience-list li::before {
    content: "";
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--sage);
    flex-shrink: 0;
  }

  /* ==========================================================================
     6. CALL-TO-ACTION (CTA) BUTTON
     ========================================================================== */
  /* Base Button Styling (Constrained max-width, flex layout for text + arrow) */
  #speaking-page .btn {
    display: inline-flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    width: 100%;
    max-width: 420px;
    text-decoration: none;
    padding: 16px 20px;
    border-radius: 10px;
    font-family: 'Work Sans', sans-serif;
    font-size: 16px;
    font-weight: 600;
    letter-spacing: 0.01em;
    transition: transform 0.15s ease, box-shadow 0.15s ease, background 0.15s ease;
    margin: 24px auto 0 auto;
    text-align: left;
  }

  /* Arrow Icon Animation */
  #speaking-page .btn .arrow {
    font-family: 'Fraunces', serif;
    font-weight: 400;
    font-size: 20px;
    transition: transform 0.15s ease;
  }

  /* Button Hover & Focus States */
  #speaking-page .btn:hover .arrow { transform: translateX(3px); }
  #speaking-page .btn:focus-visible { outline: 2px solid var(--sage-deep); outline-offset: 3px; }

  /* Primary Button Color Variant */
  #speaking-page .btn-primary { background: var(--sage-deep); color: var(--paper); }
  #speaking-page .btn-primary:hover { background: var(--ink); box-shadow: 0 6px 18px rgba(43,51,46,0.18); }

  /* Email Subtext inside Button */
  #speaking-page .btn small {
    display: block;
    font-family: 'Work Sans', sans-serif;
    font-weight: 400;
    font-size: 12.5px;
    letter-spacing: 0.01em;
    opacity: 0.8;
    margin-top: 3px;
    word-break: break-word; /* Prevents long email address from overflowing on small phones */
  }

  /* ==========================================================================
     7. MOBILE RESPONSIVE ADJUSTMENTS
     ========================================================================== */
  @media (max-width: 600px) {
    /* Slightly tighter padding on mobile screens */
    #speaking-page .wrap {
      padding: 36px 16px;
    }
    /* Scaled-down topic bubble font & padding */
    #speaking-page .topic-list li {
      font-size: 13px;
      padding: 7px 14px;
    }
    /* Scaled-down list item sizing */
    #speaking-page .experience-list li {
      font-size: 15px;
      padding: 12px 0;
    }
  }
</style>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<!-- ==========================================================================
     PAGE CONTENT HTML STRUCTURE
     ========================================================================== -->
<div id="speaking-page">
  <div class="wrap">
    <div class="content">

      <!-- Header Section -->
      <h1>Exploring Meaning Through Conversation</h1>
      <p class="lede">I enjoy speaking with students, professionals, community organizations, churches, and other groups on topics related to mental health, resilience, relationships, and the search for meaning. Whether presenting to a classroom, leading a workshop, or facilitating a webinar, my goal is not simply to share information but to create thoughtful conversations that encourage reflection and practical growth.</p>
      <p class="lede">My presentations draw from clinical practice, military service, parenting, and a lifelong interest in understanding what helps people build meaningful lives. Rather than offering simple answers, I hope to provide useful perspectives, ask worthwhile questions, and create space for honest discussion.</p>

      <hr class="divider">

      <!-- Topics Section -->
      <h2>Speaking Topics</h2>
      <p class="lede">Examples of topics I enjoy presenting include:</p>
      <ul class="topic-list">
        <li>Mental health and emotional well-being</li>
        <li>Resilience through adversity</li>
        <li>Meaning, purpose, and values</li>
        <li>Relationships and communication</li>
        <li>Suicide prevention and hope</li>
        <li>Military and veteran transitions</li>
        <li>Professional development for counselors</li>
        <li>Leadership and personal growth</li>
      </ul>
      <p class="lede">I'm always happy to tailor presentations to the needs of a specific audience.</p>

      <hr class="divider">

      <!-- Selected Experience Section -->
      <h2>Selected Speaking Experience</h2>
      <p class="lede">A gallery of presentations, workshops, webinars, and community events.</p>
      <ul class="experience-list">
        <li>Counseling Conference Presentation</li>
        <li>Graduate Guest Lecture</li>
        <li>Out of Darkness Suicide Prevention Walk</li>
        <li>Community Webinars</li>
        <li>Professional Trainings</li>
        <li>Future workshops and conference presentations</li>
      </ul>

      <hr class="divider">

      <!-- Call to Action Section -->
      <h2>Interested in Having Me Speak?</h2>
      <p class="lede">If you're planning a conference, classroom presentation, workshop, webinar, or community event, I'd be happy to discuss how I can contribute. Whether your audience is made up of students, clinicians, educators, community members, or organizational leaders, I strive to create presentations that are engaging, practical, and grounded in thoughtful conversation.</p>
      <p class="lede">Please feel free to reach out with information about your event, audience, and goals.</p>

      <a class="btn btn-primary" href="mailto:bnelson@elliementalhealth.com">
        <span>Get in Touch<small>bnelson@elliementalhealth.com</small></span>
        <span class="arrow">&rarr;</span>
      </a>

    </div>
  </div>
</div>
