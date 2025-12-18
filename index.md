<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1, viewport-fit=cover"
    />
    <meta name="theme-color" content="#12132b" />
    <title>Subterranean District | The district beneath the surface.</title>
    <meta
      name="description"
      content="Culture, identity, city life, and underground storytelling — documented honestly, with intention."
    />

    <!-- Fonts (safe defaults; swap later if you want) -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@300;400;500;600&display=swap"
      rel="stylesheet"
    />

    <style>
      :root {
        /* Brand-true palette (no black) */
        --ink: rgba(244, 244, 250, 0.96);
        --muted: rgba(244, 244, 250, 0.72);
        --faint: rgba(244, 244, 250, 0.55);

        --navy-1: #0b1234;
        --navy-2: #141a45;
        --twilight: #2a1d4a;
        --burgundy-1: #3a1830;
        --burgundy-2: #5a223d;

        --line: rgba(244, 244, 250, 0.14);
        --glass: rgba(255, 255, 255, 0.06);
        --glass-2: rgba(255, 255, 255, 0.085);

        --shadow: 0 18px 60px rgba(6, 7, 22, 0.35);
        --shadow-soft: 0 10px 32px rgba(6, 7, 22, 0.22);

        --radius-lg: 22px;
        --radius-md: 16px;
        --radius-sm: 12px;

        --maxw: 1120px;
        --padx: clamp(18px, 4vw, 40px);
        --pady: clamp(18px, 3.2vw, 34px);
      }

      * {
        box-sizing: border-box;
      }

      html,
      body {
        height: 100%;
      }

      body {
        margin: 0;
        color: var(--ink);
        font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica,
          Arial, sans-serif;
        background: radial-gradient(
            1100px 680px at 18% 18%,
            rgba(80, 120, 255, 0.22),
            transparent 55%
          ),
          radial-gradient(
            980px 620px at 82% 30%,
            rgba(160, 60, 110, 0.22),
            transparent 60%
          ),
          linear-gradient(135deg, var(--navy-2) 0%, var(--twilight) 48%, var(--burgundy-1) 100%);
        background-attachment: fixed;
        overflow-x: hidden;
      }

      /* Subtle “district grid” texture */
      body::before {
        content: "";
        position: fixed;
        inset: 0;
        pointer-events: none;
        background-image:
          linear-gradient(to right, rgba(255,255,255,0.06) 1px, transparent 1px),
          linear-gradient(to bottom, rgba(255,255,255,0.05) 1px, transparent 1px);
        background-size: 88px 88px;
        opacity: 0.22;
        mix-blend-mode: overlay;
      }

      a {
        color: inherit;
        text-decoration: none;
      }

      .wrap {
        width: 100%;
        max-width: var(--maxw);
        margin: 0 auto;
        padding: 0 var(--padx);
      }

      /* Header */
      header {
        position: sticky;
        top: 0;
        z-index: 50;
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        background: linear-gradient(
          to bottom,
          rgba(12, 14, 40, 0.72),
          rgba(12, 14, 40, 0.18)
        );
        border-bottom: 1px solid rgba(255, 255, 255, 0.08);
      }

      .nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 14px 0;
        gap: 18px;
      }

      .brand {
        display: flex;
        align-items: baseline;
        gap: 10px;
        min-width: 220px;
      }

      .brand h1 {
        margin: 0;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        letter-spacing: 0.08em;
        text-transform: lowercase;
        font-size: 18px;
        color: rgba(244, 244, 250, 0.92);
        white-space: nowrap;
      }

      .brand .tag {
        display: none;
        color: var(--faint);
        font-size: 12px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      nav ul {
        list-style: none;
        display: flex;
        align-items: center;
        gap: 16px;
        margin: 0;
        padding: 0;
      }

      .navlink {
        font-size: 12px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.78);
        padding: 10px 10px;
        border-radius: 999px;
        border: 1px solid transparent;
        transition: transform 180ms ease, background 180ms ease, border 180ms ease,
          color 180ms ease;
      }

      .navlink:hover {
        background: rgba(255, 255, 255, 0.06);
        border-color: rgba(255, 255, 255, 0.12);
        color: rgba(244, 244, 250, 0.92);
        transform: translateY(-1px);
      }

      .navlink[aria-current="page"] {
        background: rgba(255, 255, 255, 0.08);
        border-color: rgba(255, 255, 255, 0.16);
        color: rgba(244, 244, 250, 0.95);
      }

      /* Hero */
      main {
        position: relative;
        padding: clamp(24px, 4vw, 44px) 0 42px;
      }

      .hero {
        display: grid;
        grid-template-columns: 1.1fr 0.9fr;
        gap: clamp(18px, 3vw, 34px);
        align-items: start;
        padding: clamp(18px, 3.2vw, 28px);
        border-radius: var(--radius-lg);
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.06),
          rgba(255, 255, 255, 0.03)
        );
        border: 1px solid rgba(255, 255, 255, 0.11);
        box-shadow: var(--shadow);
      }

      .eyebrow {
        font-size: 12px;
        letter-spacing: 0.22em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.58);
        margin: 8px 0 14px;
      }

      .hero h2 {
        margin: 0 0 10px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: clamp(40px, 4.4vw, 64px);
        line-height: 1.02;
        letter-spacing: 0.01em;
      }

      .hero h3 {
        margin: 0 0 14px;
        font-weight: 600;
        font-size: clamp(16px, 1.6vw, 18px);
        color: rgba(244, 244, 250, 0.92);
      }

      .lede {
        margin: 0 0 20px;
        font-size: clamp(16px, 1.75vw, 20px);
        line-height: 1.55;
        color: rgba(244, 244, 250, 0.72);
        max-width: 54ch;
      }

      .actions {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-top: 8px;
      }

      .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        height: 44px;
        padding: 0 16px;
        border-radius: 999px;
        border: 1px solid rgba(255, 255, 255, 0.16);
        background: rgba(255, 255, 255, 0.06);
        color: rgba(244, 244, 250, 0.92);
        font-size: 12px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        cursor: pointer;
        transition: transform 180ms ease, background 180ms ease, border 180ms ease,
          box-shadow 180ms ease;
        user-select: none;
      }

      .btn:hover {
        transform: translateY(-1px);
        background: rgba(255, 255, 255, 0.085);
        border-color: rgba(255, 255, 255, 0.22);
        box-shadow: var(--shadow-soft);
      }

      .btn:active {
        transform: translateY(0px);
      }

      .btn.primary {
        background: linear-gradient(
          135deg,
          rgba(80, 120, 255, 0.22),
          rgba(160, 60, 110, 0.22)
        );
        border-color: rgba(255, 255, 255, 0.22);
      }

      /* Right column feature card */
      .feature {
        border-radius: var(--radius-md);
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.06),
          rgba(255, 255, 255, 0.035)
        );
        border: 1px solid rgba(255, 255, 255, 0.12);
        padding: 16px;
        box-shadow: 0 10px 40px rgba(6, 7, 22, 0.25);
        position: relative;
        overflow: hidden;
      }

      .feature::before {
        content: "";
        position: absolute;
        inset: -40%;
        background: radial-gradient(
          420px 240px at 30% 35%,
          rgba(80, 120, 255, 0.22),
          transparent 60%
        );
        opacity: 0.75;
        pointer-events: none;
      }

      .feature .kicker {
        position: relative;
        font-size: 12px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.62);
        margin: 2px 0 10px;
      }

      .feature .title {
        position: relative;
        margin: 0 0 10px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: 26px;
        line-height: 1.15;
      }

      .feature .meta {
        position: relative;
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
        color: rgba(244, 244, 250, 0.64);
        font-size: 13px;
        margin: 0 0 12px;
      }

      .pill {
        position: relative;
        display: inline-flex;
        align-items: center;
        gap: 8px;
        padding: 8px 10px;
        border-radius: 999px;
        border: 1px solid rgba(255, 255, 255, 0.14);
        background: rgba(255, 255, 255, 0.04);
      }

      .feature p {
        position: relative;
        margin: 0 0 14px;
        color: rgba(244, 244, 250, 0.72);
        line-height: 1.55;
        font-size: 14px;
      }

      .feature .mini-actions {
        position: relative;
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
      }

      .btn.small {
        height: 40px;
        padding: 0 14px;
        font-size: 11px;
      }

      /* Sections below fold */
      .below {
        margin-top: 22px;
        display: grid;
        grid-template-columns: 1fr;
        gap: 16px;
      }

      .grid3 {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 14px;
      }

      .card {
        border-radius: var(--radius-md);
        background: rgba(255, 255, 255, 0.045);
        border: 1px solid rgba(255, 255, 255, 0.11);
        padding: 16px;
        box-shadow: 0 10px 30px rgba(6, 7, 22, 0.18);
      }

      .card .label {
        font-size: 12px;
        letter-spacing: 0.2em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.62);
        margin: 0 0 8px;
      }

      .card h4 {
        margin: 0 0 8px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: 22px;
      }

      .card p {
        margin: 0 0 12px;
        color: rgba(244, 244, 250, 0.7);
        line-height: 1.55;
        font-size: 14px;
      }

      .newsletter {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 14px;
        padding: 16px;
        border-radius: var(--radius-md);
        border: 1px solid rgba(255, 255, 255, 0.12);
        background: linear-gradient(
          90deg,
          rgba(80, 120, 255, 0.10),
          rgba(160, 60, 110, 0.10)
        );
      }

      .newsletter .copy {
        max-width: 62ch;
      }

      .newsletter .copy .label {
        margin-bottom: 6px;
      }

      .newsletter form {
        display: flex;
        gap: 10px;
        align-items: center;
        flex-wrap: wrap;
        justify-content: flex-end;
      }

      .input {
        height: 44px;
        min-width: min(360px, 70vw);
        padding: 0 14px;
        border-radius: 999px;
        border: 1px solid rgba(255, 255, 255, 0.16);
        background: rgba(255, 255, 255, 0.06);
        color: rgba(244, 244, 250, 0.92);
        outline: none;
      }

      .input::placeholder {
        color: rgba(244, 244, 250, 0.5);
      }

      .input:focus {
        border-color: rgba(255, 255, 255, 0.26);
        background: rgba(255, 255, 255, 0.08);
      }

      /* Footer */
      footer {
        margin-top: 34px;
        padding: 18px 0 30px;
        border-top: 1px solid rgba(255, 255, 255, 0.09);
        color: rgba(244, 244, 250, 0.62);
      }

      .foot {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 14px;
        flex-wrap: wrap;
      }

      .foot .left {
        display: flex;
        gap: 10px;
        align-items: center;
        flex-wrap: wrap;
      }

      .dot {
        width: 6px;
        height: 6px;
        border-radius: 999px;
        background: rgba(244, 244, 250, 0.5);
      }

      /* Responsive */
      @media (max-width: 940px) {
        .hero {
          grid-template-columns: 1fr;
        }
        .grid3 {
          grid-template-columns: 1fr;
        }
        .newsletter {
          flex-direction: column;
          align-items: stretch;
        }
        .newsletter form {
          justify-content: flex-start;
        }
        .brand .tag {
          display: none;
        }
      }

      /* Reduced motion */
      @media (prefers-reduced-motion: reduce) {
        .btn,
        .navlink {
          transition: none !important;
        }
        html:focus-within {
          scroll-behavior: auto;
        }
      }
    </style>
  </head>

  <body>
    <header>
      <div class="wrap">
        <div class="nav">
          <a class="brand" href="#top" aria-label="Subterranean District home">
            <h1>subterranean district</h1>
            <span class="tag">the district beneath the surface</span>
          </a>

          <nav aria-label="Primary">
            <ul>
              <li><a class="navlink" href="#manifesto">Brand Manifesto</a></li>
              <li><a class="navlink" href="#archive">Archive</a></li>
              <li><a class="navlink" href="#about">About</a></li>
            </ul>
          </nav>
        </div>
      </div>
    </header>

    <main id="top">
      <div class="wrap">
        <section class="hero" aria-label="Hero">
          <!-- Left column -->
          <div>
            <div class="eyebrow">A living archive</div>
            <h2>Subterranean District</h2>
            <h3>The district beneath the surface.</h3>

            <p class="lede">
              Culture, identity, city life, and underground storytelling —
              documented honestly, with intention.
            </p>

            <div class="actions">
              <a class="btn primary" href="#manifesto">Manifesto</a>
              <a class="btn" href="#archive">Archive</a>
              <a class="btn" href="#about">About</a>
            </div>
          </div>

          <!-- Right column -->
          <aside class="feature" aria-label="Featured dispatch">
            <div class="kicker">Featured dispatch</div>
            <h3 class="title">Issue 0: The Places People Don’t Look</h3>

            <div class="meta">
              <span class="pill">Field notes</span>
              <span class="pill">Drafting now</span>
              <span class="pill">Winter 2025</span>
            </div>

            <p>
              A quiet opening. A blueprint of the District’s voice: intimate,
              grounded, and unafraid of the real.
            </p>

            <div class="mini-actions">
              <a class="btn small primary" href="#archive">View archive</a>
              <a class="btn small" href="#manifesto">Read manifesto</a>
            </div>
          </aside>
        </section>

        <section class="below" aria-label="Below the fold">
          <div class="grid3">
            <article class="card" id="manifesto">
              <div class="label">Manifesto</div>
              <h4>The why</h4>
              <p>
                Our declaration of purpose, identity, and vision — written for
                the alleys, basements, and late-night corridors.
              </p>
              <a class="btn small" href="#manifesto" data-scroll="true"
                >Open</a
              >
            </article>

            <article class="card" id="archive">
              <div class="label">Archive</div>
              <h4>The record</h4>
              <p>
                Essays, interviews, photo sets, and fragments — organized as a
                living archive over time.
              </p>
              <a class="btn small" href="#archive" data-scroll="true"
                >Browse</a
              >
            </article>

            <article class="card" id="about">
              <div class="label">About</div>
              <h4>The method</h4>
              <p>
                A publication for underground storytelling. We document with
                care, without spectacle.
              </p>
              <a class="btn small" href="#about" data-scroll="true"
                >Read</a
              >
            </article>
          </div>

          <div class="newsletter" aria-label="Newsletter signup">
            <div class="copy">
              <div class="label">Stay close</div>
              <div style="font-family: 'DM Serif Display', serif; font-size: 22px; margin-bottom: 6px;">
                Notes from the District
              </div>
              <div style="color: rgba(244,244,250,0.72); line-height: 1.5; font-size: 14px;">
                Occasional dispatches when something is worth documenting. No noise.
              </div>
            </div>

            <!-- Placeholder form (wire to your email tool later) -->
            <form onsubmit="return false;">
              <input class="input" type="email" placeholder="Email address" aria-label="Email address" />
              <button class="btn primary" type="submit">Subscribe</button>
            </form>
          </div>
        </section>

        <footer>
          <div class="foot">
            <div class="left">
              <strong style="color: rgba(244,244,250,0.82); font-weight: 600;">Subterranean District</strong>
              <span class="dot" aria-hidden="true"></span>
              <span>The district beneath the surface.</span>
            </div>
            <div class="right" style="display: flex; gap: 12px; flex-wrap: wrap;">
              <a class="navlink" href="#top">Top</a>
              <a class="navlink" href="#manifesto">Manifesto</a>
              <a class="navlink" href="#archive">Archive</a>
            </div>
          </div>
        </footer>
      </div>
    </main>

    <script>
      // Smooth scrolling (Safari-safe) without relying on CSS only
      document.querySelectorAll('a[href^="#"]').forEach((a) => {
        a.addEventListener("click", (e) => {
          const id = a.getAttribute("href");
          if (!id || id === "#") return;
          const el = document.querySelector(id);
          if (!el) return;

          e.preventDefault();
          el.scrollIntoView({ behavior: "smooth", block: "start" });

          // Simple current-state highlight for nav
          document.querySelectorAll(".navlink").forEach((n) => n.removeAttribute("aria-current"));
          if (a.classList.contains("navlink")) a.setAttribute("aria-current", "page");
        });
      });
    </script>
  </body>
</html>
