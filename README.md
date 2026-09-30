# Shakx-media-
Official shakx media website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shakx Media — edit · shoot · create</title>
  <!-- Elegant & eye-catching fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
  <style>
    /* ---------- GLOBAL RESET & VARIABLES ---------- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --pink: #FF3B7F;
      --red: #E01A4F;
      --black: #0A0A0A;
      --white: #FFFFFF;
      --off-white: #F8F5F2;
      --gray-light: #E6E1DE;
      --gray-mid: #2C2C2C;
      --font-sans: 'Inter', sans-serif;
      --font-serif: 'Playfair Display', serif;
      --shadow-sm: 0 4px 12px rgba(0, 0, 0, 0.05);
      --shadow-md: 0 12px 32px rgba(0, 0, 0, 0.08);
      --radius-md: 16px;
      --radius-lg: 24px;
    }

    body {
      background-color: var(--black);
      color: var(--white);
      font-family: var(--font-sans);
      font-weight: 400;
      line-height: 1.5;
      -webkit-font-smoothing: antialiased;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img, svg {
      display: block;
      max-width: 100%;
    }

    /* ---------- TYPOGRAPHY ---------- */
    h1, h2, h3 {
      font-family: var(--font-serif);
      font-weight: 500;
      letter-spacing: -0.02em;
    }

    h1 {
      font-size: clamp(2.8rem, 8vw, 5.5rem);
      line-height: 1.1;
    }

    h2 {
      font-size: clamp(2rem, 5vw, 3.2rem);
      line-height: 1.2;
      margin-bottom: 1rem;
    }

    h3 {
      font-size: 1.6rem;
      font-weight: 600;
      font-family: var(--font-sans);
      letter-spacing: -0.01em;
    }

    .text-pink { color: var(--pink); }
    .text-red { color: var(--red); }
    .text-white { color: var(--white); }
    .text-black { color: var(--black); }

    /* ---------- LAYOUT UTILITIES ---------- */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    .section {
      padding: 6rem 0;
    }

    .section-header {
      text-align: center;
      margin-bottom: 4rem;
    }

    .section-header h2 {
      margin-bottom: 0.75rem;
    }

    .section-header .subhead {
      font-size: 1.2rem;
      color: #aaa;
      max-width: 600px;
      margin: 0 auto;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2.5rem;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2rem;
    }

    @media (max-width: 900px) {
      .grid-2, .grid-3 {
        grid-template-columns: 1fr;
      }
    }

    /* ---------- BUTTONS ---------- */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 1rem 2.2rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 1rem;
      transition: all 0.2s ease;
      border: 2px solid transparent;
      cursor: pointer;
      font-family: var(--font-sans);
    }

    .btn-primary {
      background: var(--pink);
      color: var(--black);
      border-color: var(--pink);
    }

    .btn-primary:hover {
      background: var(--red);
      border-color: var(--red);
      color: var(--white);
      transform: translateY(-2px);
    }

    .btn-outline {
      background: transparent;
      color: var(--white);
      border-color: var(--white);
    }

    .btn-outline:hover {
      background: var(--white);
      color: var(--black);
      border-color: var(--white);
    }

    /* ---------- HEADER / NAV ---------- */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.5rem 2rem;
      max-width: 1400px;
      margin: 0 auto;
    }

    .logo-container {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .logo-svg {
      width: 48px;
      height: 48px;
      flex-shrink: 0;
    }

    .logo-text {
      font-family: var(--font-serif);
      font-size: 1.8rem;
      font-weight: 600;
      letter-spacing: -0.02em;
      color: var(--white);
      line-height: 1;
    }

    .logo-text span {
      color: var(--pink);
    }

    .nav-links {
      display: flex;
      gap: 2.5rem;
      align-items: center;
      font-weight: 500;
    }

    .nav-links a {
      font-size: 0.95rem;
      letter-spacing: 0.01em;
      color: #ccc;
      transition: color 0.2s;
    }

    .nav-links a:hover {
      color: var(--pink);
    }

    .nav-cta {
      background: var(--pink);
      color: var(--black);
      padding: 0.6rem 1.6rem;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.9rem;
      transition: all 0.2s;
    }

    .nav-cta:hover {
      background: var(--red);
      color: var(--white);
    }

    @media (max-width: 800px) {
      .navbar {
        flex-direction: column;
        gap: 1.5rem;
      }
      .nav-links {
        flex-wrap: wrap;
        justify-content: center;
        gap: 1.2rem;
      }
    }

    /* ---------- HERO SLIDER ---------- */
    .hero {
      position: relative;
      background: var(--black);
      padding: 2rem 2rem 5rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    }

    .slider-container {
      max-width: 1400px;
      margin: 0 auto;
      position: relative;
      border-radius: var(--radius-lg);
      overflow: hidden;
      box-shadow: 0 30px 50px -20px rgba(0, 0, 0, 0.8);
    }

    .slider {
      display: flex;
      transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }

    .slide {
      min-width: 100%;
      position: relative;
      aspect-ratio: 16 / 7;
      background: var(--gray-mid);
      display: flex;
      align-items: flex-end;
      justify-content: flex-start;
      padding: 3rem;
      isolation: isolate;
    }

    /* Simulated portfolio slides – placeholder images with gradient overlays */
    .slide-1 {
      background: linear-gradient(135deg, #1E1E1E 0%, #2A0A1A 100%),
                  radial-gradient(circle at 80% 20%, rgba(255, 59, 127, 0.4), transparent 60%);
    }
    .slide-2 {
      background: linear-gradient(45deg, #0A0A0A 0%, #2C0E1E 100%),
                  radial-gradient(circle at 30% 70%, rgba(224, 26, 79, 0.5), transparent 70%);
    }
    .slide-3 {
      background: linear-gradient(225deg, #0F0F0F 0%, #1F1F1F 100%),
                  radial-gradient(circle at 70% 40%, rgba(255, 59, 127, 0.35), transparent 65%);
    }
    .slide-4 {
      background: linear-gradient(120deg, #1C1C1C 0%, #2E0B1C 100%),
                  radial-gradient(circle at 20% 30%, rgba(224, 26, 79, 0.45), transparent 65%);
    }

    .slide-content {
      position: relative;
      z-index: 2;
      max-width: 600px;
    }

    .slide-tag {
      display: inline-block;
      background: var(--pink);
      color: var(--black);
      padding: 0.3rem 1rem;
      border-radius: 40px;
      font-weight: 700;
      font-size: 0.75rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    .slide-title {
      font-family: var(--font-serif);
      font-size: clamp(2rem, 6vw, 4rem);
      font-weight: 600;
      line-height: 1.05;
      text-shadow: 0 4px 20px rgba(0,0,0,0.5);
    }

    .slide-title span {
      color: var(--pink);
    }

    .slider-controls {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin-top: 2rem;
    }

    .slider-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.25);
      border: none;
      cursor: pointer;
      transition: all 0.3s;
    }

    .slider-dot.active {
      background: var(--pink);
      width: 32px;
      border-radius: 20px;
    }

    /* ---------- SERVICES / EDITING TOOLS SHOWCASE ---------- */
    .tools-badge {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      margin-top: 2rem;
    }

    .tool-icon {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      width: 72px;
      height: 72px;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s;
    }

    .tool-icon:hover {
      border-color: var(--pink);
      background: rgba(255, 59, 127, 0.1);
    }

    .tool-icon svg {
      width: 34px;
      height: 34px;
      stroke: var(--white);
      stroke-width: 1.8;
      fill: none;
    }

    /* ---------- BOOKING SECTION ---------- */
    .booking-card {
      background: #111;
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: var(--radius-lg);
      padding: 2.5rem;
      box-shadow: var(--shadow-md);
    }

    .booking-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }

    @media (max-width: 800px) {
      .booking-grid {
        grid-template-columns: 1fr;
      }
    }

    .form-group {
      margin-bottom: 1.5rem;
    }

    .form-group label {
      display: block;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      font-weight: 600;
      color: #aaa;
      margin-bottom: 0.5rem;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      padding: 1rem 1.2rem;
      background: #1A1A1A;
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      font-family: var(--font-sans);
      font-size: 1rem;
      color: var(--white);
      transition: border 0.2s;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: var(--pink);
    }

    .calendar-grid {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 0.5rem;
      margin-top: 0.5rem;
    }

    .calendar-day {
      aspect-ratio: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      background: #1A1A1A;
      border-radius: 10px;
      font-size: 0.85rem;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.15s;
      border: 1px solid transparent;
    }

    .calendar-day:hover {
      border-color: var(--pink);
      background: rgba(255, 59, 127, 0.1);
    }

    .calendar-day.selected {
      background: var(--pink);
      color: var(--black);
      font-weight: 700;
    }

    .calendar-day.disabled {
      opacity: 0.25;
      pointer-events: none;
    }

    .calendar-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1rem;
      font-weight: 600;
    }

    .payment-icons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      margin-top: 1rem;
      align-items: center;
    }

    .payment-icons svg {
      height: 28px;
      width: auto;
      opacity: 0.6;
      transition: opacity 0.2s;
    }

    .payment-icons svg:hover {
      opacity: 1;
    }

    .secure-badge {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.85rem;
      color: #aaa;
      margin-top: 1.2rem;
    }

    .secure-badge svg {
      width: 20px;
      height: 20px;
      stroke: var(--pink);
    }

    /* ---------- VISION / PRIVACY PAGES (modals) ---------- */
    .page-overlay {
      display: none;
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.85);
      backdrop-filter: blur(8px);
      z-index: 1000;
      align-items: center;
      justify-content: center;
      padding: 2rem;
    }

    .page-overlay.active {
      display: flex;
    }

    .page-modal {
      background: #111;
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: var(--radius-lg);
      max-width: 900px;
      width: 100%;
      max-height: 85vh;
      overflow-y: auto;
      padding: 3rem;
      position: relative;
      box-shadow: 0 40px 80px rgba(0,0,0,0.8);
    }

    .close-modal {
      position: absolute;
      top: 1.5rem;
      right: 1.5rem;
      background: none;
      border: none;
      color: var(--white);
      font-size: 2rem;
      cursor: pointer;
      line-height: 1;
      opacity: 0.6;
      transition: opacity 0.2s;
    }

    .close-modal:hover {
      opacity: 1;
      color: var(--pink);
    }

    .page-modal h1 {
      font-size: 2.8rem;
      margin-bottom: 1.5rem;
      color: var(--pink);
    }

    .page-modal h2 {
      font-size: 1.6rem;
      margin-top: 2rem;
      margin-bottom: 0.75rem;
      color: var(--white);
      font-family: var(--font-sans);
      font-weight: 600;
    }

    .page-modal p {
      margin-bottom: 1.2rem;
      color: #ccc;
    }

    .page-modal ul {
      margin-left: 1.5rem;
      margin-bottom: 1.5rem;
      color: #ccc;
    }

    .page-modal li {
      margin-bottom: 0.5rem;
    }

    /* ---------- FOOTER ---------- */
    .footer {
      border-top: 1px solid rgba(255, 255, 255, 0.08);
      padding: 3rem 0;
      margin-top: 4rem;
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 2rem;
    }

    .footer-phone {
      font-weight: 600;
      font-size: 1.2rem;
      color: var(--white);
    }

    .footer-phone span {
      color: var(--pink);
    }

    .footer-links {
      display: flex;
      gap: 2rem;
      font-size: 0.9rem;
      color: #aaa;
    }

    .footer-links a:hover {
      color: var(--pink);
    }

    /* ---------- RESPONSIVE ---------- */
    @media (max-width: 600px) {
      .container { padding: 0 1.5rem; }
      .section { padding: 3.5rem 0; }
      .slide { padding: 2rem 1.5rem; aspect-ratio: 4 / 3; }
      .booking-card { padding: 1.5rem; }
      .page-modal { padding: 2rem; }
    }
  </style>
</head>
<body>

  <!-- ========== NAVBAR ========== -->
  <nav class="navbar">
    <div class="logo-container">
      <!-- TRANSPARENT 1:1 LOGO — Editing tools (camera + computer) -->
      <svg class="logo-svg" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
        <!-- Camera body left -->
        <rect x="8" y="32" width="48" height="36" rx="8" stroke="#FF3B7F" stroke-width="3.5" fill="transparent"/>
        <circle cx="32" cy="50" r="10" stroke="white" stroke-width="3" fill="transparent"/>
        <circle cx="32" cy="50" r="4" fill="#FF3B7F" />
        <!-- Computer / screen right -->
        <rect x="56" y="24" width="36" height="28" rx="4" stroke="white" stroke-width="3" fill="transparent"/>
        <rect x="64" y="52" width="20" height="8" rx="2" fill="white" />
        <line x1="70" y1="60" x2="78" y2="60" stroke="white" stroke-width="3" stroke-linecap="round"/>
        <line x1="74" y1="52" x2="74" y2="60" stroke="white" stroke-width="3" stroke-linecap="round"/>
        <!-- connection / spark -->
        <path d="M46 50 L56 38" stroke="#FF3B7F" stroke-width="3" stroke-linecap="round" stroke-dasharray="4 4"/>
      </svg>
      <div class="logo-text">SHAKX<span>.</span></div>
    </div>
    <div class="nav-links">
      <a href="#" onclick="openModal('vision'); return false;">Vision</a>
      <a href="#" onclick="openModal('privacy'); return false;">Privacy</a>
      <a href="#booking">Booking</a>
      <a href="#booking" class="nav-cta">Book now</a>
    </div>
  </nav>

  <!-- ========== HERO SLIDER ========== -->
  <section class="hero">
    <div class="slider-container">
      <div class="slider" id="slider">
        <!-- Slide 1 -->
        <div class="slide slide-1">
          <div class="slide-content">
            <span class="slide-tag">Editorial</span>
            <h1 class="slide-title">Neon <span>Nights</span><br>Campaign</h1>
          </div>
        </div>
        <!-- Slide 2 -->
        <div class="slide slide-2">
          <div class="slide-content">
            <span class="slide-tag">Music Video</span>
            <h1 class="slide-title">Velvet <span>Pulse</span><br>Visuals</h1>
          </div>
        </div>
        <!-- Slide 3 -->
        <div class="slide slide-3">
          <div class="slide-content">
            <span class="slide-tag">Brand Film</span>
            <h1 class="slide-title">Lumière <span>Studios</span><br>Story</h1>
          </div>
        </div>
        <!-- Slide 4 -->
        <div class="slide slide-4">
          <div class="slide-content">
            <span class="slide-tag">Portrait</span>
            <h1 class="slide-title">Crimson <span>Grace</span><br>Series</h1>
          </div>
        </div>
      </div>
    </div>
    <div class="slider-controls" id="sliderDots">
      <button class="slider-dot active" data-index="0"></button>
      <button class="slider-dot" data-index="1"></button>
      <button class="slider-dot" data-index="2"></button>
      <button class="slider-dot" data-index="3"></button>
    </div>

    <!-- Editing tool icons (camera / computer) as visual identity -->
    <div class="tools-badge">
      <div class="tool-icon">
        <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"/>
          <circle cx="12" cy="13" r="4"/>
        </svg>
      </div>
      <div class="tool-icon">
        <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="3" width="20" height="14" rx="2" ry="2"/>
          <line x1="8" y1="21" x2="16" y2="21"/>
          <line x1="12" y1="17" x2="12" y2="21"/>
        </svg>
      </div>
      <div class="tool-icon">
        <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <polygon points="23 7 16 12 23 17 23 7"/>
          <rect x="1" y="5" width="15" height="14" rx="2" ry="2"/>
        </svg>
      </div>
    </div>
  </section>

  <!-- ========== BOOKING SECTION ========== -->
  <section class="section container" id="booking">
    <div class="section-header">
      <h2>Book a <span class="text-pink">session</span></h2>
      <p class="subhead">Choose your slot, secure payment, and let's create something stunning.</p>
    </div>

    <div class="booking-card">
      <div class="booking-grid">
        <!-- Left column: calendar -->
        <div>
          <h3 style="margin-bottom: 1.5rem; font-family: var(--font-sans);">Real‑time availability</h3>
          <div class="calendar-header">
            <span>September 2026</span>
            <span style="color: var(--pink); font-size: 0.9rem;">• Live</span>
          </div>
          <div class="calendar-grid" id="calendarGrid">
            <!-- Generated with JS, but we'll keep static for demo clarity -->
          </div>
          <p style="font-size: 0.8rem; color: #777; margin-top: 1rem;">Selected date: <span id="selectedDateDisplay" style="color: var(--pink); font-weight: 600;">—</span></p>
        </div>

        <!-- Right column: form + payment -->
        <div>
          <h3 style="margin-bottom: 1.5rem; font-family: var(--font-sans);">Your details</h3>
          <div class="form-group">
            <label>Full name</label>
            <input type="text" placeholder="e.g. Alex Rivera">
          </div>
          <div class="form-group">
            <label>Email</label>
            <input type="email" placeholder="hello@example.com">
          </div>
          <div class="form-group">
            <label>Service</label>
            <select>
              <option>Photo shoot</option>
              <option>Video production</option>
              <option>Editing & color grading</option>
              <option>Motion graphics</option>
            </select>
          </div>

          <!-- Secure payment gateway mock -->
          <div style="background: #1A1A1A; border-radius: 16px; padding: 1.5rem; margin-top: 1.5rem;">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem;">
              <span style="font-weight: 600;">Secure payment</span>
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="var(--pink)" stroke-width="2">
                <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
                <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
              </svg>
            </div>
            <div class="payment-icons">
              <!-- visa -->
              <svg viewBox="0 0 48 32" width="48" height="32"><rect width="48" height="32" rx="4" fill="#1A1A1A"/><path d="M22 21h-3l2-12h3l-2 12zm8-12c-1-.4-2.5-.8-4-.8-4 0-6.5 2-6.5 5 0 2.2 1.5 3.5 3.5 4.2 1.5.5 2 .9 2 1.5 0 .8-1 1.2-2 1.2-1.5 0-2.8-.5-3.8-1l-.5 2.5c1 .5 2.8 1 4.8 1 4.2 0 6.8-2 6.8-5.2 0-2.2-1.5-3.8-3.8-4.5-1.5-.5-2.5-.9-2.5-1.6 0-.5.5-1 1.8-1 1 0 2 .3 2.8.8l.4-2.4zM38 9h-2.5c-1 0-1.8.3-2.2 1.2L28 21h3l.8-2h4l.5 2H41l-3-12zm-4.5 8l1.5-4.5.8 4.5h-2.3z" fill="#fff" opacity="0.7"/></svg>
              <!-- mastercard -->
              <svg viewBox="0 0 48 32" width="48" height="32"><rect width="48" height="32" rx="4" fill="#1A1A1A"/><circle cx="18" cy="16" r="8" fill="#E01A4F" opacity="0.8"/><circle cx="30" cy="16" r="8" fill="#FF3B7F" opacity="0.8"/><path d="M24 10.5c1.5 1.5 2.5 3.5 2.5 5.5s-1 4-2.5 5.5c-1.5-1.5-2.5-3.5-2.5-5.5s1-4 2.5-5.5z" fill="#fff" opacity="0.9"/></svg>
              <!-- amex -->
              <svg viewBox="0 0 48 32" width="48" height="32"><rect width="48" height="32" rx="4" fill="#1A1A1A"/><rect x="8" y="10" width="32" height="12" rx="2" fill="#2C2C2C"/><text x="24" y="22" font-family="Arial" font-size="10" fill="#fff" text-anchor="middle" opacity="0.7">AMEX</text></svg>
            </div>
            <div class="secure-badge">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
                <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
              </svg>
              <span>256‑bit SSL encrypted · PCI compliant</span>
            </div>
            <button class="btn btn-primary" style="width: 100%; margin-top: 1.5rem;" onclick="alert('Demo: payment gateway simulation. In production, this connects to Stripe / Paystack.')">Confirm & pay</button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== FOOTER ========== -->
  <footer class="footer">
    <div class="container footer-content">
      <div class="footer-phone">📞 <span>0755 285 835</span></div>
      <div class="footer-links">
        <a href="#" onclick="openModal('vision'); return false;">Vision</a>
        <a href="#" onclick="openModal('privacy'); return false;">Privacy policy</a>
        <a href="#booking">Book</a>
      </div>
      <div style="font-size: 0.8rem; color: #555;">© 2026 Shakx Media</div>
    </div>
  </footer>

  <!-- ========== VISION PAGE MODAL ========== -->
  <div class="page-overlay" id="visionModal">
    <div class="page-modal">
      <button class="close-modal" onclick="closeModal('vision')">×</button>
      <h1>Our Vision</h1>
      <p><strong>Shakx Media</strong> exists to merge technical precision with raw creative energy. We believe every frame, every color grade, and every cut should tell a story that resonates.</p>
      <h2>Redefining visual storytelling</h2>
      <p>We're building a space where photographers, videographers, and editors can collaborate seamlessly. Our platform connects you with top-tier editing tools and real-time booking — no friction, just flow.</p>
      <h2>Technology meets art</h2>
      <p>From high-speed cameras to advanced post-production suites, we invest in the tools that make magic possible. But technology is only half the equation — the other half is your unique perspective.</p>
      <ul>
        <li>Empower creators with intuitive booking and secure payments.</li>
        <li>Deliver consistent, cinematic quality across every project.</li>
        <li>Foster a community that values bold, unapologetic creativity.</li>
      </ul>
      <p style="margin-top: 2rem; color: var(--pink); font-weight: 600;">— The Shakx Media team</p>
    </div>
  </div>

  <!-- ========== PRIVACY POLICY MODAL ========== -->
  <div class="page-overlay" id="privacyModal">
    <div class="page-modal">
      <button class="close-modal" onclick="closeModal('privacy')">×</button>
      <h1>Privacy Policy</h1>
      <p>Last updated: September 2026</p>
      <p>At Shakx Media, we take your privacy seriously. This policy explains how we collect, use, and protect your personal information.</p>
      <h2>1. Information we collect</h2>
      <ul>
        <li>Contact details (name, email, phone) when you book a session.</li>
        <li>Payment information processed via our secure PCI-compliant gateway.</li>
        <li>Usage data to improve our booking interface.</li>
      </ul>
      <h2>2. How we use your data</h2>
      <p>We use your information solely to manage bookings, process payments, and communicate about your sessions. We never sell your data to third parties.</p>
      <h2>3. Data security</h2>
      <p>All transactions are encrypted using 256-bit SSL. Payment details are tokenized and never stored on our servers.</p>
      <h2>4. Your rights</h2>
      <p>You can request access, correction, or deletion of your personal data at any time by contacting us at <span style="color: var(--p