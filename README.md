[night_github_readme.html](https://github.com/user-attachments/files/28383310/night_github_readme.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>21stDev — README</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,400&family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg: #000000;
  --surface: #0a0a0a;
  --border: #1a1a1a;
  --border-mid: #222;
  --text: #e8e8e8;
  --muted: #555;
  --dim: #333;
  --accent: #00D4A0;
  --accent-dim: rgba(0, 212, 160, 0.08);
  --accent-border: rgba(0, 212, 160, 0.2);
  --font-sans: 'Syne', sans-serif;
  --font-mono: 'DM Mono', monospace;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-sans);
  line-height: 1.6;
  min-height: 100vh;
  padding: 2.5rem 2rem;
  max-width: 760px;
  margin: 0 auto;
}

/* HEADER */
.header {
  border-bottom: 1px solid var(--border);
  padding-bottom: 2rem;
  margin-bottom: 2rem;
}

.org-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  margin-bottom: 1rem;
}
.org-badge::before {
  content: '';
  display: block;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--accent);
}

.name {
  font-size: clamp(2.2rem, 6vw, 3.4rem);
  font-weight: 800;
  letter-spacing: -0.04em;
  line-height: 1;
  color: #fff;
  margin-bottom: 0.4rem;
}

.handle {
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--muted);
  margin-bottom: 1.2rem;
}

.tagline {
  font-size: 14px;
  color: #777;
  max-width: 440px;
  line-height: 1.7;
  margin-bottom: 1.4rem;
}

.links {
  display: flex;
  gap: 0.6rem;
  flex-wrap: wrap;
}

.link-pill {
  display: inline-flex;
  align-items: center;
  gap: 5px;
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--muted);
  text-decoration: none;
  border: 1px solid var(--border-mid);
  padding: 5px 12px;
  border-radius: 2px;
  transition: all 0.15s ease;
  letter-spacing: 0.04em;
}
.link-pill:hover {
  color: var(--text);
  border-color: var(--dim);
}
.link-pill.primary {
  background: var(--accent-dim);
  border-color: var(--accent-border);
  color: var(--accent);
}
.link-pill.primary:hover {
  background: rgba(0,212,160,0.14);
}

/* SECTION */
section {
  margin-bottom: 2rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--border);
}
section:last-child { border-bottom: none; margin-bottom: 0; }

.section-label {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 0.14em;
  text-transform: uppercase;
  margin-bottom: 1.2rem;
}

/* STATUS */
.status-row {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}
.status-item {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
  color: #666;
  font-family: var(--font-mono);
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 8px 14px;
  border-radius: 2px;
  flex: 1;
  min-width: 200px;
}
.status-dot {
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background: var(--accent);
  flex-shrink: 0;
  box-shadow: 0 0 6px var(--accent);
  animation: pulse 2.5s ease-in-out infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.3; }
}

/* FEATURED */
.featured-card {
  background: var(--surface);
  border: 1px solid var(--border-mid);
  padding: 1.6rem;
  border-radius: 2px;
  position: relative;
  overflow: hidden;
}
.featured-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--accent), transparent);
  opacity: 0.6;
}
.featured-name {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: -0.02em;
  color: #fff;
  margin-bottom: 4px;
}
.featured-sub {
  font-size: 12px;
  font-family: var(--font-mono);
  color: var(--muted);
  margin-bottom: 1rem;
}
.featured-desc {
  font-size: 13px;
  color: #666;
  line-height: 1.7;
  margin-bottom: 1.2rem;
  max-width: 500px;
}
.flow {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--accent);
  background: var(--accent-dim);
  border: 1px solid var(--accent-border);
  padding: 8px 14px;
  margin-bottom: 1.2rem;
  letter-spacing: 0.02em;
}
.tag-row { display: flex; gap: 6px; flex-wrap: wrap; }
.tag {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--muted);
  border: 1px solid var(--border-mid);
  padding: 3px 8px;
  letter-spacing: 0.04em;
}

/* STACK GRID */
.stack-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
}
.stack-cell {
  background: var(--bg);
  padding: 12px 16px;
}
.stack-layer {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 5px;
}
.stack-items {
  font-size: 12px;
  color: #888;
  font-family: var(--font-mono);
  line-height: 1.8;
}

/* PROJECTS TABLE */
.project-list { display: flex; flex-direction: column; gap: 1px; }
.project-row {
  display: grid;
  grid-template-columns: 160px 1fr auto;
  gap: 1rem;
  align-items: center;
  padding: 12px 0;
  border-bottom: 1px solid var(--border);
}
.project-row:last-child { border-bottom: none; }
.project-name {
  font-size: 13px;
  font-weight: 600;
  color: #ccc;
  letter-spacing: -0.01em;
}
.project-desc {
  font-size: 12px;
  color: var(--muted);
  font-family: var(--font-mono);
}
.project-status {
  font-family: var(--font-mono);
  font-size: 10px;
  padding: 3px 8px;
  border-radius: 2px;
  white-space: nowrap;
}
.project-status.live { background: var(--accent-dim); color: var(--accent); border: 1px solid var(--accent-border); }
.project-status.building { background: rgba(255,180,0,0.07); color: #c8960c; border: 1px solid rgba(200,150,12,0.2); }
.project-status.concept { background: #0a0a0a; color: #444; border: 1px solid var(--border); }

/* CONNECT */
.connect-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 8px;
}
.connect-item {
  display: flex;
  flex-direction: column;
  gap: 2px;
  padding: 12px 14px;
  border: 1px solid var(--border);
  background: var(--surface);
  cursor: pointer;
}
.connect-item a { text-decoration: none; color: inherit; display: contents; }
.connect-platform {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
}
.connect-handle {
  font-size: 13px;
  font-weight: 600;
  color: #aaa;
}
.connect-item:hover .connect-handle { color: var(--accent); }

/* FOOTER */
.footer {
  padding-top: 1.6rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
}
.footer-loc {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
}
.footer-motto {
  font-family: var(--font-mono);
  font-size: 11px;
  color: #2a2a2a;
  letter-spacing: 0.04em;
}
</style>
</head>
<body>

<!-- HEADER -->
<header class="header">
  <div class="org-badge">Open to work · Abuja, Nigeria</div>
  <h1 class="name">Night</h1>
  <div class="handle">@21stDev</div>
  <p class="tagline">Full-stack engineer building trust infrastructure for African commerce. Shipping in TypeScript, Solana, and React Native.</p>
  <div class="links">
    <a href="https://payhold.vercel.app" class="link-pill primary">↗ PayHold</a>
    <a href="https://21stdeveloper.vercel.app" class="link-pill">Portfolio</a>
    <a href="https://x.com/21stjalal" class="link-pill">X / Twitter</a>
    <a href="https://linkedin.com/in/21stdev" class="link-pill">LinkedIn</a>
  </div>
</header>

<!-- NOW -->
<section>
  <div class="section-label">// now</div>
  <div class="status-row">
    <div class="status-item"><span class="status-dot"></span>Shipping PayHold mobile (RN · Expo)</div>
    <div class="status-item"><span class="status-dot"></span>Expanding into real estate &amp; logistics</div>
    <div class="status-item"><span class="status-dot"></span>Building Muqaddimah (YouTube · Ibn Khaldun)</div>
    <div class="status-item"><span class="status-dot"></span>Partner · noOnes</div>
  </div>
</section>

<!-- FEATURED -->
<section>
  <div class="section-label">// featured</div>
  <div class="featured-card">
    <div class="featured-name">PayHold</div>
    <div class="featured-sub">Nigeria's Trust Layer for Commerce · payhold.ng</div>
    <p class="featured-desc">
      Escrow and deal management infrastructure built for African commerce — covering general trade, real estate, and logistics. Designed to be the settlement layer between buyers and sellers who don't yet trust each other.
    </p>
    <div class="flow">Buyer funds → Seller delivers with proof → Auto-release</div>
    <div class="tag-row">
      <span class="tag">Next.js</span>
      <span class="tag">Express.js</span>
      <span class="tag">PostgreSQL</span>
      <span class="tag">Prisma</span>
      <span class="tag">React Native</span>
      <span class="tag">Paystack</span>
      <span class="tag">Vercel</span>
      <span class="tag">Railway</span>
    </div>
  </div>
</section>

<!-- STACK -->
<section>
  <div class="section-label">// stack</div>
  <div class="stack-grid">
    <div class="stack-cell">
      <div class="stack-layer">Frontend</div>
      <div class="stack-items">Next.js · React<br>Tailwind CSS · Framer Motion</div>
    </div>
    <div class="stack-cell">
      <div class="stack-layer">Mobile</div>
      <div class="stack-items">React Native · Expo<br>Expo Router · Reanimated</div>
    </div>
    <div class="stack-cell">
      <div class="stack-layer">Backend</div>
      <div class="stack-items">Express.js · Node.js<br>REST · JWT · NextAuth</div>
    </div>
    <div class="stack-cell">
      <div class="stack-layer">Data</div>
      <div class="stack-items">PostgreSQL · Prisma<br>Supabase · Redis</div>
    </div>
    <div class="stack-cell">
      <div class="stack-layer">Web3</div>
      <div class="stack-items">Solana · Anchor<br>SPL Tokens · Metaplex</div>
    </div>
    <div class="stack-cell">
      <div class="stack-layer">Deploy</div>
      <div class="stack-items">Vercel · Railway<br>Docker · GitHub Actions</div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section>
  <div class="section-label">// projects</div>
  <div class="project-list">
    <div class="project-row">
      <div class="project-name">PayHold</div>
      <div class="project-desc">Escrow &amp; deal management · Next.js · RN</div>
      <span class="project-status live">live</span>
    </div>
    <div class="project-row">
      <div class="project-name">ROSCAChain</div>
      <div class="project-desc">Decentralised rotating savings · Solana · Anchor</div>
      <span class="project-status building">building</span>
    </div>
    <div class="project-row">
      <div class="project-name">Muqaddimah</div>
      <div class="project-desc">YouTube documentary series · Ibn Khaldun</div>
      <span class="project-status building">building</span>
    </div>
    <div class="project-row">
      <div class="project-name">21stDev Portfolio</div>
      <div class="project-desc">Personal site · React · Vite · GSAP</div>
      <span class="project-status live">live</span>
    </div>
    <div class="project-row">
      <div class="project-name">CasualCrave</div>
      <div class="project-desc">Mood-powered local discovery · React</div>
      <span class="project-status concept">collab</span>
    </div>
  </div>
</section>

<!-- CONNECT -->
<section>
  <div class="section-label">// connect</div>
  <div class="connect-grid">
    <div class="connect-item">
      <a href="https://x.com/21stjalal" target="_blank">
        <div class="connect-platform">X / Twitter</div>
        <div class="connect-handle">@21stjalal</div>
      </a>
    </div>
    <div class="connect-item">
      <a href="https://linkedin.com/in/21stdev" target="_blank">
        <div class="connect-platform">LinkedIn</div>
        <div class="connect-handle">21stdev</div>
      </a>
    </div>
    <div class="connect-item">
      <a href="https://payhold.vercel.app" target="_blank">
        <div class="connect-platform">Product</div>
        <div class="connect-handle">payhold.ng</div>
      </a>
    </div>
    <div class="connect-item">
      <a href="https://21stdeveloper.vercel.app" target="_blank">
        <div class="connect-platform">Portfolio</div>
        <div class="connect-handle">21stdeveloper.vercel.app</div>
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <span class="footer-loc">📍 Abuja · Nigeria</span>
  <span class="footer-motto">writing infrastructure, one commit at a time.</span>
</footer>

</body>
</html>
