---
layout: single
title: Contact
permalink: /contact/
header:
  overlay_image: /Assets/4SWallpaper.jpg
  overlay_filter: 0.4
---

<style>
  #contact-page {
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
    font-family: 'Work Sans', sans-serif;
    color: var(--ink);
    background: var(--stone);
    margin: -1em -1em 0;
    padding: 0;
  }

  #contact-page .wrap {
    max-width: 640px;
    margin: 0 auto;
    padding: 56px 24px 56px;
    position: relative;
  }

  #contact-page .content { position: relative; z-index: 1; }

  #contact-page .eyebrow {
    font-size: 12.5px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--sage-deep);
    font-weight: 600;
    margin: 0 0 18px;
  }

  #contact-page h1 {
    font-family: 'Fraunces', serif;
    font-optical-sizing: auto;
    font-weight: 500;
    font-size: clamp(30px, 5vw, 40px);
    line-height: 1.25;
    letter-spacing: -0.01em;
    margin: 0 0 20px;
    color: var(--ink);
  }

  #contact-page .lede {
    font-size: 17px;
    line-height: 1.65;
    color: var(--ink-soft);
    margin: 0 0 12px;
    max-width: 54ch;
  }

  #contact-page .caution {
    font-size: 14.5px;
    line-height: 1.6;
    color: var(--ink-soft);
    font-style: italic;
    margin: 20px 0 0;
    padding-left: 14px;
    border-left: 2px solid var(--clay);
  }

  #contact-page .locations {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin: 36px 0 40px;
  }

  #contact-page .badge {
    display: flex;
    align-items: baseline;
    gap: 8px;
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 9px 16px;
    font-size: 14px;
  }

  #contact-page .badge .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--sage);
    flex-shrink: 0;
  }

  #contact-page .badge strong { font-weight: 600; color: var(--ink); }
  #contact-page .badge span.loc { color: var(--ink-soft); }

  #contact-page .divider {
    border: none;
    border-top: 1px solid var(--line);
    margin: 8px 0 40px;
  }

  #contact-page .actions {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 44px;
  }

  #contact-page .btn {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    text-decoration: none;
    padding: 18px 22px;
    border-radius: 10px;
    font-family: 'Work Sans', sans-serif;
    font-size: 16px;
    font-weight: 600;
    letter-spacing: 0.01em;
    transition: transform 0.15s ease, box-shadow 0.15s ease, background 0.15s ease;
  }

  #contact-page .btn .arrow {
    font-family: 'Fraunces', serif;
    font-weight: 400;
    font-size: 20px;
    transition: transform 0.15s ease;
  }

  #contact-page .btn:hover .arrow { transform: translateX(3px); }
  #contact-page .btn:focus-visible { outline: 2px solid var(--sage-deep); outline-offset: 3px; }

  #contact-page .btn-primary { background: var(--sage-deep); color: var(--paper); }
  #contact-page .btn-primary:hover { background: var(--ink); box-shadow: 0 6px 18px rgba(43,51,46,0.18); }

  #contact-page .btn-secondary { background: var(--paper); color: var(--ink); border: 1px solid var(--line); }
  #contact-page .btn-secondary:hover { border-color: var(--clay-deep); box-shadow: 0 4px 14px rgba(43,51,46,0.08); }

  #contact-page .btn small {
    display: block;
    font-family: 'Work Sans', sans-serif;
    font-weight: 400;
    font-size: 12.5px;
    letter-spacing: 0.01em;
    opacity: 0.8;
    margin-top: 3px;
  }

  #contact-page .direct-row {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding: 14px 0;
    border-bottom: 1px solid var(--line);
  }
  #contact-page .direct-row:first-of-type { border-top: 1px solid var(--line); }

  #contact-page .direct-label {
    font-size: 12.5px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-soft);
    font-weight: 600;
  }

  #contact-page .direct-value { font-size: 16px; }
  #contact-page .direct-value a { color: var(--ink); text-decoration: none; border-bottom: 1px solid var(--clay); }
  #contact-page .direct-value a:hover { color: var(--clay-deep); }
</style>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<div id="contact-page">
  <div class="wrap">
    <div class="content">
      <p class="eyebrow">Contact</p>
      <h1>Let's start a conversation.</h1>
      <p class="lede">I'm happy to answer questions about counseling, speaking engagements, or other professional inquiries.</p>
      <p class="caution">Please don't include confidential or urgent mental health information in email.</p>

      <div class="locations">
        <div class="badge"><span class="dot"></span><strong>In person</strong><span class="loc">Smyrna, TN</span></div>
        <div class="badge"><span class="dot"></span><strong>Telehealth</strong><span class="loc">across Tennessee</span></div>
      </div>

      <hr class="divider">

      <div class="actions">
        <a class="btn btn-primary" href="https://www.psychologytoday.com/us/therapists/ben-nelson-smyrna-tn/1408270" target="_blank" rel="noopener" data-role="schedule">
          <span>Schedule an Appointment<small>Book online</small></span>
          <span class="arrow">&rarr;</span>
        </a>
        <a class="btn btn-secondary" href="tel:+16152476831">
          <span>Call the Practice<small>(615) 247-6831</small></span>
          <span class="arrow">&rarr;</span>
        </a>
        <a class="btn btn-secondary" href="mailto:Bnelson@elliementalhealth.com">
          <span>Get in Touch<small>Email the office</small></span>
          <span class="arrow">&rarr;</span>
        </a>
      </div>

      <div class="direct">
        <div class="direct-row">
          <span class="direct-label">Phone</span>
          <span class="direct-value"><a href="tel:+16152476831">(615) 247-6831</a></span>
        </div>
        <div class="direct-row">
          <span class="direct-label">Email</span>
          <span class="direct-value"><a href="mailto:Bnelson@elliementalhealth.com">Bnelson@elliementalhealth.com</a></span>
        </div>
      </div>
    </div>
  </div>
</div>


</div>

      <p class="lede" style="margin-top: 32px;">Your new sentences go here.</p>
    </div>
  </div>
</div>
