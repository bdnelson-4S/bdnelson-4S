---
# ==========================================================================
# 1. JEKYLL FRONT MATTER (PAGE METADATA & CONFIGURATION)
# ==========================================================================

layout: single                             # Uses the theme's 'single' page layout template
title: Contact                             # Sets the page <title> tag and main metadata heading
permalink: /contact/                       # Defines the static URL path for this page (yourdomain.com/contact/)
header:
  overlay_image: /Assets/4SWallpaper.jpg   # Sets a background hero image for the header banner
  overlay_filter: 0.4                       # Applies a 40% dark overlay tint over the hero image for readability
---

<!-- ==========================================================================
     2. EMBEDDED CSS STYLES (<style>)
     ========================================================================== -->
<style>
  /* Base Container & Custom Design System Tokens */
  #contact-page {
    /* Color Palette Variables */
    --stone: #EFEDE4;      /* Soft warm-grey background color */
    --stone-deep: #E3E0D3; /* Darker accent grey */
    --ink: #2B332E;        /* Deep charcoal for primary text */
    --ink-soft: #545E56;   /* Muted grey for body copy & subtext */
    --sage: #6E7F63;       /* Muted green accent */
    --sage-deep: #3F4F3F;  /* Deep green for primary buttons & headings */
    --clay: #B9855A;       /* Warm terracotta brown for accents/borders */
    --clay-deep: #9C6E45;  /* Darker terracotta for hover states */
    --line: #D7D3C4;       /* Subtle border/divider line color */
    --paper: #FBFAF7;      /* Clean off-white background for cards/badges */

    /* Global Typography & Layout Resets */
    font-family: 'Work Sans', sans-serif;
    color: var(--ink);
    background: var(--stone);
    margin: -1em -1em 0;                       /* Offsets default theme container margins */
    padding: 0;
    max-width: none !important;                /* Overrides layout constraints to allow full-width */
    width: 100vw !important;                   /* Forces page block to span 100% of the screen width */
    margin-left: calc(-50vw + 50%) !important; /* Horizontally centers full-bleed layout breakout */
  }

  /* Inner Layout Wrapper */
  #contact-page .wrap {
    width: 90%;             /* Sets responsive width on smaller screens */
    max-width: 1100px;      /* Caps maximum container width on large monitors */
    margin: 0 auto;         /* Centers the content block horizontally */
    padding: 56px 32px 56px;/* Vertical and horizontal inner padding */
    position: relative;     /* Establishes positioning context for child elements */
  }

  /* Main Content Stack */
  #contact-page .content { 
    position: relative; 
    z-index: 1;             /* Keeps text elements above any decorative backgrounds */
  }

  /* Section Eyebrow Tag (Small Category Label Above Title) */
  #contact-page .eyebrow {
    font-size: 12.5px;
    letter-spacing: 0.14em; /* Spreads out tracking for uppercase label style */
    text-transform: uppercase;
    color: var(--sage-deep);
    font-weight: 600;
    margin: 0 0 18px;
  }

  /* Main Heading (H1) */
  #contact-page h1 {
    font-family: 'Fraunces', serif;     /* Uses elegant serif font for heading */
    font-optical-sizing: auto;
    font-weight: 500;
    font-size: clamp(30px, 5vw, 40px);  /* Fluid typography: resizes between 30px and 40px */
    line-height: 1.25;
    letter-spacing: -0.01em;
    margin: 0 0 20px;
    color: var(--ink);
  }

  /* Subtitle / Intro Paragraph (Lede) */
  #contact-page .lede {
    font-size: 17px;
    line-height: 1.65;                  /* Adds line spacing for readability */
    color: var(--ink-soft);
    margin: 0 0 12px;
    max-width: 70%;                     /* Limits line width to keep text readable */
  }

  /* Warning / Caution Callout Box */
  #contact-page .caution {
    font-size: 14.5px;
    line-height: 1.6;
    color: var(--ink-soft);
    font-style: italic;
    margin: 20px 0 0;
    padding-left: 14px;
    border-left: 2px solid var(--clay); /* Vertical terracotta bar along the left edge */
  }

  /* Location Badges Container */
  #contact-page .locations {
    display: flex;
    flex-wrap: wrap;                   /* Allows badges to wrap on mobile devices */
    gap: 10px;                         /* Spacing between individual location pills */
    margin: 36px 0 40px;
  }

  /* Individual Location Badge/Pill Style */
  #contact-page .badge {
    display: flex;
    align-items: baseline;              /* Aligns badge text and dot indicator cleanly */
    gap: 8px;
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 999px;               /* Creates fully rounded pill shape */
    padding: 9px 16px;
    font-size: 14px;
  }

  /* Green Indicator Dot inside Location Badge */
  #contact-page .badge .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;                 /* Creates circular dot shape */
    background: var(--sage);
    flex-shrink: 0;                     /* Prevents dot from squeezing on narrow displays */
  }

  /* Badge Text Formatting */
  #contact-page .badge strong { font-weight: 600; color: var(--ink); }
  #contact-page .badge span.loc { color: var(--ink-soft); }

  /* Horizontal Divider Line */
  #contact-page .divider {
    border: none;
    border-top: 1px solid var(--line);  /* Clean 1px separator line */
    margin: 8px 0 40px;
  }

  /* Call-to-Action (CTA) Buttons Group */
  #contact-page .actions {
    display: flex;
    flex-direction: column;            /* Stacks buttons vertically */
    gap: 12px;                          /* Space between buttons */
    margin-bottom: 44px;
  }

  /* Base Button Styling */
  #contact-page .btn {
    display: flex;
    align-items: center;
    justify-content: space-between;    /* Pushes text to left and arrow icon to right */
    gap: 16px;
    text-decoration: none;
    padding: 18px 22px;
    border-radius: 10px;                /* Rounded rectangle edges */
    font-family: 'Work Sans', sans-serif;
    font-size: 16px;
    font-weight: 600;
    letter-spacing: 0.01em;
    transition: transform 0.15s ease, box-shadow 0.15s ease, background 0.15s ease; /* Smooth hover transition */
  }

  /* Right Arrow Icon inside Buttons */
  #contact-page .btn .arrow {
    font-family: 'Fraunces', serif;
    font-weight: 400;
    font-size: 20px;
    transition: transform 0.15s ease;  /* Prepares arrow for hover animation */
  }

  /* Button Hover & Accessibility States */
  #contact-page .btn:hover .arrow { transform: translateX(3px); }                           /* Slides arrow slightly right on hover */
  #contact-page .btn:focus-visible { outline: 2px solid var(--sage-deep); outline-offset: 3px; } /* Focus ring for keyboard accessibility */

  /* Primary Button Variant (Dark Green Solid) */
  #contact-page .btn-primary { background: var(--sage-deep); color: var(--paper); }
  #contact-page .btn-primary:hover { background: var(--ink); box-shadow: 0 6px 18px rgba(43,51,46,0.18); }

  /* Secondary Button Variant (Outlined / Off-White) */
  #contact-page .btn-secondary { background: var(--paper); color: var(--ink); border: 1px solid var(--line); }
  #contact-page .btn-secondary:hover { border-color: var(--clay-deep); box-shadow: 0 4px 14px rgba(43,51,46,0.08); }

  /* Subtitle text inside Buttons */
  #contact-page .btn small {
    display: block;                     /* Forces subtitle onto its own line inside button */
    font-family: 'Work Sans', sans-serif;
    font-weight: 400;
    font-size: 12.5px;
    letter-spacing: 0.01em;
    opacity: 0.8;
    margin-top: 3px;
  }

  /* Direct Contact Information Table/Rows */
  #contact-page .direct-row {
    display: flex;
    align-items: baseline;
    justify-content: space-between;     /* Aligns label to left and phone/email value to right */
    padding: 14px 0;
    border-bottom: 1px solid var(--line);
  }
  #contact-page .direct-row:first-of-type { border-top: 1px solid var(--line); } /* Top border for first item */

  /* Label text in direct contact row (Phone, Email) */
  #contact-page .direct-label {
    font-size: 12.5px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-soft);
    font-weight: 600;
  }

  /* Link formatting in direct contact row */
  #contact-page .direct-value { font-size: 16px; }
  #contact-page .direct-value a { color: var(--ink); text-decoration: none; border-bottom: 1px solid var(--clay); }
  #contact-page .direct-value a:hover { color: var(--clay-deep); }
</style>

<!-- ==========================================================================
     3. EXTERNAL FONT IMPORTS (GOOGLE FONTS)
     ========================================================================== -->

<!-- Preconnects to Google Fonts servers to speed up font loading -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<!-- Loads 'Fraunces' (Serif) and 'Work Sans' (Sans-Serif) font families -->
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<!-- ==========================================================================
     4. HTML CONTENT STRUCTURE
     ========================================================================== -->

<!-- Main Page Outer Wrapper -->
<div id="contact-page">
  <div class="wrap">
    <div class="content">

      <!-- Eyebrow Category Tag -->
      <p class="eyebrow">Contact</p>

      <!-- Main Page Header -->
      <h1>Let's start a conversation.</h1>

      <!-- Intro Subtitle Text -->
      <p class="lede">I'm happy to answer questions about counseling, speaking engagements, or other professional inquiries.</p>

      <!-- Confidentiality Warning Box -->
      <p class="caution">Please don't include confidential or urgent mental health information in email.</p>

      <!-- Location Badges Section -->
      <div class="locations">
        <div class="badge">
          <span class="dot"></span>
          <strong>In person</strong>
          <span class="loc">Smyrna, TN</span>
        </div>
        <div class="badge">
          <span class="dot"></span>
          <strong>Telehealth</strong>
          <span class="loc">across Tennessee</span>
        </div>
      </div>

      <!-- Section Separator Line -->
      <hr class="divider">

      <!-- Action Buttons Container -->
      <div class="actions">

        <!-- Psychology Today Scheduling Button (Primary) -->
        <a class="btn btn-primary" href="https://www.psychologytoday.com/us/therapists/ben-nelson-smyrna-tn/1408270" target="_blank" rel="noopener" data-role="schedule">
          <span>Schedule a Counseling Appointment<small>Book on Psychology Today</small></span>
          <span class="arrow">&rarr;</span>
        </a>

        <!-- Phone Call Button (Secondary) -->
        <a class="btn btn-secondary" href="tel:+16152476831">
          <span>Call Ellie Mental Health to Book Over the Phone<small>(615) 247-6831</small></span>
          <span class="arrow">&rarr;</span>
        </a>

        <!-- Direct Email Button (Secondary) -->
        <a class="btn btn-secondary" href="mailto:Bnelson@elliementalhealth.com">
          <span>Connect With Me<small>Email Me Any </small></span>
          <span class="arrow">&rarr;</span>
        </a>

      </div>

      <!-- Direct Phone & Email List Section -->
      <div class="direct">

        <!-- Direct Phone Number Row -->
        <div class="direct-row">
          <span class="direct-label">Phone</span>
          <span class="direct-value"><a href="tel:+16152476831">(615) 247-6831</a></span>
        </div>

        <!-- Direct Email Row -->
        <div class="direct-row">
          <span class="direct-label">Email</span>
          <span class="direct-value"><a href="mailto:Bnelson@elliementalhealth.com">Bnelson@elliementalhealth.com</a></span>
        </div>

      </div>

      <!-- Closing Paragraph Text -->
      <p class="lede" style="margin-top: 32px;">Whether you're seeking counseling, inviting me to speak, or simply hoping to connect, I appreciate you reaching out..</p>

    </div>
  </div>
</div>
