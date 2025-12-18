<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover" />
    <meta name="theme-color" content="#141a45" />
    <title>Subterranean District | The district beneath the surface.</title>
    <meta
      name="description"
      content="Culture, identity, city life, and underground storytelling — documented honestly, with intention."
    />

    <!-- Fonts -->
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

        --navy: #141a45;
        --twilight: #2a1d4a;
        --burgundy: #3a1830;

        --line: rgba(244, 244, 250, 0.14);
        --glass: rgba(255, 255, 255, 0.06);
        --glass2: rgba(255, 255, 255, 0.085);

        --radius: 18px;
        --maxw: 1120px;
        --padx: clamp(18px, 4vw, 40px);
      }

      * { box-sizing: border-box; }
      html, body { height: 100%; }

      body {
        margin: 0;
        color: var(--ink);
        font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;

        /* Blue + burgundy blend */
        background:
          radial-gradient(1150px 720px at 16% 18%, rgba(80, 120, 255, 0.22), transparent 58%),
          radial-gradient(980px 620px at 82% 34%, rgba(160, 60, 110, 0.22), transparent 60%),
          linear-gradient(135deg, var(--navy) 0%, var(--twilight) 50%, var(--burgundy) 100%);

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
        background-size: 92px 92px;
        opacity: 0.16;
        mix-blend-mode: overlay;
      }

      a { color: inherit; text-decoration: none; }

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
        z-index: 20;
        padding: 18px 0 10px;
        backdrop-filter: blur(10px);
        background: linear-gradient(to bottom, rgba(20,26,69,0.72), rgba(20,26,69,0.16));
        border-bottom: 1px solid rgba(244,244,250,0.10);
      }

      .nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 18px;
      }

      .brand {
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        letter-spacing: 0.14em;
        text-transform: lowercase;
        font-size: 20px;
        color: rgba(244, 244, 250, 0.9);
        white-space: nowrap;
      }

      nav ul {
        list-style: none;
        display: flex;
        align-items: center;
        gap: 22px;
        margin: 0;
        padding: 0;
      }

      .navlink {
        font-size: 12px;
        letter-spacing: 0.16em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.72);
        padding: 10px 8px;
        border-radius: 999px;
        border: 1px solid transparent;
        transition: background 180ms ease, border 180ms ease, color 180ms ease;
      }

      .navlink:hover {
        background: rgba(255, 255, 255, 0.06);
        border-color: rgba(255, 255, 255, 0.12);
        color: rgba(244, 244, 250, 0.92);
      }

      /* Thin accent line (subtle) */
      .accent-line {
        margin-top: 14px;
        height: 1px;
        width: 100%;
        background: linear-gradient(
          to right,
          rgba(244,244,250,0.00),
          rgba(160,60,110,0.26),
          rgba(244,244,250,0.00)
        );
        opacity: 0.6;
      }

      /* Main / Hero */
      main {
        padding: clamp(42px, 6vw, 86px) 0 40px;
      }

      .hero {
        padding-top: clamp(24px, 5vw, 54px);
        padding-bottom: clamp(26px, 5vw, 54px);
        max-width: 760px;
      }

      .eyebrow {
        font-size: 12px;
        letter-spacing: 0.22em;
        text-transform: uppercase;
        color: rgba(244, 244, 250, 0.55);
        margin: 0 0 18px;
      }

      h1 {
        margin: 0 0 18px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: clamp(46px, 5.2vw, 74px);
        line-height: 1.02;
        letter-spacing: 0.01em;
      }

      .headline {
        margin: 0 0 18px;
        font-weight: 600;
        font-size: clamp(18px, 2vw, 20px);
        color: rgba(244, 244, 250, 0.92);
      }

      .lede {
        margin: 0 0 28px;
        font-size: clamp(18px, 2.1vw, 22px);
        line-height: 1.55;
        color: rgba(244, 244, 250, 0.68);
        max-width: 60ch;
      }

      .actions {
        display: flex;
        gap: 12px;
        flex-wrap: wrap;
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
        color: rgba(244, 244, 250, 0.9);
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

      .btn:active { transform: translateY(0px); }

      .btn.primary {
        border-color: rgba(160, 60, 110, 0.35);
        background: linear-gradient(
          135deg,
          rgba(80, 120, 255, 0.14),
          rgba(160, 60, 110, 0.18)
        );
      }

      /* Real sections so scrolling feels meaningful */
      section.block {
        scroll-margin-top: 96px;
        padding: 44px 0;
        border-top: 1px solid rgba(244,244,250,0.10);
      }

      .block-inner {
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        gap: 26px;
        padding: 18px 0 0;
      }

      .block h2 {
        margin: 0 0 14px;
        font-family: "DM Serif Display", serif;
        font-weight: 400;
        font-size: 28px;
        letter-spacing: 0.01em;
        color: rgba(244,244,250,0.92);
      }

      .block p {
        margin: 0 0 12px;
        color: rgba(244,244,250,0.70);
        line-height: 1.65;
        font-size: 16px;
        max-width: 70ch;
      }

      .callout {
        border: 1px solid rgba(255,255,255,0.14);
        background: rgba(255,255,255,0.05);
        border-radius: var(--radius);
        padding: 16px 16px;
        color: rgba(244,244,250,0.66);
        line-height: 1.6;
        font-size: 14px;
      }

      .callout .label {
        display: inline-block;
        font-size: 11px;
        letter-spacing: 0.22em;
        text-transform: uppercase;
        color: rgba(244,244,250,0.55);
        margin-bottom: 10px;
      }

      /* Footer (minimal, non-repetitive) */
      footer {
        padding: 28px 0 36px;
        border-top: 1px solid rgba(244,244,250,0.10);
        background: transparent; /* avoids the “hard seam” */
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
        flex-direction: column;
        gap: 8px;
      }

      .foot .meta {
        color: rgba(244, 244, 250, 0.50);
        font-size: 13px;
      }

      .foot .links {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
      }

      .foot .links a {
        color: rgba(244,244,250,0.62);
        font-size: 12px;
        letter-spacing: 0.16em;
        text-transform: uppercase;
        padding: 8px 10px;
        border-radius: 999px;
        border: 1px solid transparent;
      }

      .foot .links a:hover {
        color: rgba(244,244,250,0.92);
        background: rgba(255,255,255,0.06);
        border-color: rgba(255,255,255,0.12);
      }

      @media (max-width: 860px) {
        .block-inner { grid-template-columns: 1fr; }
      }

      @media (max-width: 760px) {
        nav ul { gap: 12px; }
        .navlink { padding: 10px 6px; }
        .hero { max-width: 100%; }
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
              <li><a class="navlink" href="#manifesto">Manifesto</a></li>
              <li><a class="navlink" href="#archive">Archive</a></li>
              <li><a class="navlink" href="#about">About</a></li>
            </ul>
          </nav>
        </div>

        <div class="accent-line" aria-hidden="true"></div>
      </div>
    </header>

    <main id="top">
      <div class="wrap">
        <section class="hero" aria-label="Hero">
          <div class="eyebrow">A living archive</div>

          <h1>Subterranean District</h1>

          <p class="headline">The district beneath the surface.</p>

          <p class="lede">
            Culture, identity, city life, and underground storytelling — documented honestly, with intention.
          </p>

          <div class="actions">
            <a class="btn primary" href="#manifesto">Manifesto</a>
            <a class="btn" href="#archive">Archive</a>
            <a class="btn" href="#about">About</a>
          </div>
        </section>

        <section id="manifesto" class="block" aria-label="Brand Manifesto">
          <h2>Brand Manifesto</h2>
          <div class="block-inner">
            <div>
              <p>
                This is where the manifesto lives. Keep the homepage version tight — a strong excerpt — then expand into a full page later if you want.
              </p>
              <p>
                For now, this section exists so the site feels real immediately and the navigation actually “lands” somewhere.
              </p>
            </div>
            <aside class="callout">
              <div class="label">Next</div>
              Add a short excerpt (6–12 lines) here pulled directly from your manifesto.
              Then we’ll build <span style="color: rgba(244,244,250,0.86);">manifesto.html</span> as the full read.
            </aside>
          </div>
        </section>

        <section id="archive" class="block" aria-label="Archive">
          <h2>Archive</h2>
          <div class="block-inner">
            <div>
              <p>
                This becomes your list of posts, issues, or entries. When you’re ready, we’ll convert this into a clean grid of cards (title, date, tag, excerpt).
              </p>
              <p>
                Even before posts exist, it should still feel intentional — like a sealed door you’ll open soon.
              </p>
            </div>
            <aside class="callout">
              <div class="label">Structure</div>
              Suggested: Issues, Essays, Photo Studies, Interviews, Field Notes.
            </aside>
          </div>
        </section>

        <section id="about" class="block" aria-label="About">
          <h2>About</h2>
          <div class="block-inner">
            <div>
              <p>
                A short statement about what Subterranean District is, what it’s trying to protect, and what it’s trying to reveal.
              </p>
              <p>
                Add submissions/collabs/contact details here when you’re ready.
              </p>
            </div>
            <aside class="callout">
              <div class="label">Tone</div>
              Keep it spare. One paragraph that reads like a vow.
            </aside>
          </div>
        </section>
      </div>
    </main>

    <footer>
      <div class="wrap">
        <div class="foot">
          <div class="left">
            <div class="meta">© <span id="y"></span> Subterranean District</div>
            <div class="meta">The district beneath the surface.</div>
          </div>

          <div class="links" aria-label="Footer links">
            <a href="#manifesto">Manifesto</a>
            <a href="#archive">Archive</a>
            <a href="#about">About</a>
          </div>
        </div>
      </div>
    </footer>

    <script>
      // Smooth scrolling (Safari-friendly) + avoids “tiny anchor” confusion
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

      document.getElementById("y").textContent = new Date().getFullYear();
    </script>
  </body>
</html>
