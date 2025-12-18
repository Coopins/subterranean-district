<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover" />
    <meta name="theme-color" content="#12132b" />
    <title>Subterranean District | The district beneath the surface.</title>
    <meta
      name="description"
      content="Culture, identity, city life, and underground storytelling — documented honestly, with intention."
    />

    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@300;400;500;600&display=swap"
      rel="stylesheet"
    />

    <style>
      :root {
        --ink: rgba(244, 244, 250, 0.96);
        --muted: rgba(244, 244, 250, 0.72);
        --faint: rgba(244, 244, 250, 0.55);

        --navy-1: #0b1234;
        --navy-2: #141a45;
        --twilight: #2a1d4a;
        --burgundy-1: #3a1830;

        --line: rgba(244, 244, 250, 0.14);
        --glass: rgba(255, 255, 255, 0.06);

        --shadow: 0 18px 60px rgba(6, 7, 22, 0.35);

        --radius-lg: 22px;
        --maxw: 1120px;
        --padx: clamp(18px, 4vw, 40px);
      }

      * { box-sizing: border-box; }
      html, body { height: 100%; }

      body {
        margin: 0;
        color: var(--ink);
        font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;

        /* Blue + burgundy blend (no black) */
        background:
          radial-gradient(1100px 680px at 18% 18%, rgba(80, 120, 255, 0.22), transparent 55%),
          radial-gradient(980px 620px at 82% 30%, rgba(160, 60, 110, 0.22), transparent 60%),
          linear-gradient(135deg, var(--navy-2) 0%, var(--twilight) 50%, var(--burgundy-1) 100%);

        background-attachment: fixed;
        overflow-x: hidden;
      }

      body::before {
        content: "";
        position: fixed;
        inset: 0;
        pointer-events: none;
        background-image:
          linear-gradient(to right, rgba(255,255,255,0.06) 1px, transparent 1px),
          linear-gradient(to bottom, rgba(255,255,255,0.05) 1px, transparent 1px);
        background-size: 88px 88px;
        opacity: 0.18;
        mix-blend-mode: overlay;
      }

      a { color: inherit; text-decoration: none; }

      .wrap {
        width: 100%;
        max-width: var(--maxw);
        margin: 0 auto;
        padding: 0 var(--padx);
      }

      header {
        position: sticky;
        top: 0;
        z-index: 50;
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        background: linear-gradient(to bottom, rgba(12, 14, 40, 0.62), rgba(12, 14, 40, 0.12));
        border-bottom: 1px solid rgba(255, 255, 255, 0.08);
      }

      .nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 16px 0;
        gap: 18px;
      }

      .brand {
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        letter-spacing: 0.08em;
        text-transform: lowercase;
        font-size: 18px;
        color: rgba(244, 244, 250, 0.92);
        white-space: nowrap;
      }

      nav ul {
        list-style: none;
        display: flex;
        align-items: center;
        gap: 18px;
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
        transition: background 180ms ease, border 180ms ease, color 180ms ease, transform 180ms ease;
      }

      .navlink:hover {
        background: rgba(255, 255, 255, 0.06);
        border-color: rgba(255, 255, 255, 0.12);
        color: rgba(244, 244, 250, 0.92);
        transform: translateY(-1px);
      }

      main {
        padding: clamp(36px, 5vw, 66px) 0 50px;
      }

      .hero {
        border-radius: var(--radius-lg);
        background: linear-gradient(180deg, rgba(255, 255, 255, 0.06), rgba(255, 255, 255, 0.03));
        border: 1px solid rgba(255, 255, 255, 0.11);
        box-shadow: var(--shadow);
        padding: clamp(26px, 4vw, 44px);
      }

      .eyebrow {
        font-size: 12px;
        letter-spacing: 0.22em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.58);
        margin: 0 0 16px;
      }

      h1 {
        margin: 0 0 10px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: clamp(42px, 4.8vw, 68px);
        line-height: 1.02;
      }

      .subhead {
        margin: 0 0 16px;
        font-weight: 600;
        font-size: clamp(16px, 1.7vw, 18px);
        color: rgba(244, 244, 250, 0.92);
      }

      .lede {
        margin: 0 0 22px;
        font-size: clamp(16px, 1.9vw, 20px);
        line-height: 1.55;
        color: rgba(244, 244, 250, 0.72);
        max-width: 60ch;
      }

      .actions {
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
      }

      .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
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
        transition: transform 180ms ease, background 180ms ease, border 180ms ease;
        user-select: none;
      }

      .btn:hover {
        transform: translateY(-1px);
        background: rgba(255, 255, 255, 0.085);
        border-color: rgba(255, 255, 255, 0.22);
      }

      .btn.primary {
        background: linear-gradient(135deg, rgba(80, 120, 255, 0.22), rgba(160, 60, 110, 0.22));
        border-color: rgba(255, 255, 255, 0.22);
      }

      footer {
        margin-top: 26px;
        padding: 16px 0 30px;
        border-top: 1px solid rgba(255, 255, 255, 0.09);
        color: rgba(244, 244, 250, 0.62);
        font-size: 13px;
      }

      .foot {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 12px;
        flex-wrap: wrap;
      }

      @media (max-width: 720px) {
        nav ul { gap: 10px; }
        .navlink { padding: 9px 8px; }
      }

      @media (prefers-reduced-motion: reduce) {
        .btn, .navlink { transition: none !important; }
      }
    </style>
  </head>

  <body>
    <header>
      <div class="wrap">
        <div class="nav">
          <a class="brand" href="#top" aria-label="Subterranean District home">subterranean district</a>
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
          <div class="eyebrow">A living archive</div>
          <h1>Subterranean District</h1>
          <div class="subhead">The district beneath the surface.</div>

          <p class="lede">
            Culture, identity, city life, and underground storytelling — documented honestly, with intention.
          </p>

          <div class="actions">
            <a class="btn primary" href="#manifesto">Manifesto</a>
            <a class="btn" href="#archive">Archive</a>
            <a class="btn" href="#about">About</a>
          </div>
        </section>

        <footer>
          <div class="foot">
            <div><strong style="color: rgba(244,244,250,0.82); font-weight: 600;">Subterranean District</strong></div>
            <div>The district beneath the surface.</div>
          </div>
        </footer>
      </div>
    </main>

    <script>
      // Smooth scrolling (Safari-friendly)
      document.querySelectorAll('a[href^="#"]').forEach((a) => {
        a.addEventListener("click", (e) => {
          const id = a.getAttribute("href");
          if (!id || id === "#") return;
          const el = document.querySelector(id);
          if (!el) return;
          e.preventDefault();
          el.scrollIntoView({ behavior: "smooth", block: "start" });
        });
      });
    </script>
  </body>
</html>
