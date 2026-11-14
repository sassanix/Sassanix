<!-- No DOCTYPE here: Jekyll wraps this file in the Hacker layout, and a DOCTYPE inside the layout body renders as visible text. -->
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sassanix Official Page</title>
<!-- Note: the live page is wrapped in the Hacker theme layout by Jekyll, so head tags here do not reach the served head. The served title and description come from the layout and _config.yml. -->
<meta name="description" content="Listen to my latest mixes and see my latest creations.">
<meta property="og:title" content="Sassanix Official Page">
<meta property="og:description" content="Listen to my latest mixes and see my latest creations.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://sassanix.com/">
<meta name="twitter:card" content="summary">
<meta name="theme-color" content="#101114">
<link rel="icon" href="LS8Mx.gif" type="image/gif">
<style>
/* Note: the live page is wrapped in the Hacker theme layout. Heading colors, fonts, and the body background below override Hacker styles. */
:root {
  --bg: #101114;
  --surface: #1a1c20;
  --surface-2: #22252b;
  --text: #f2f2f2;
  --muted: #b8bec7;
  --border: #2e3238;
  --accent: #4da3ff;
  --accent-text: #0a0f16;
  --max: 880px;
  --radius: 14px;
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  color: var(--text);
  background-color: var(--bg);
  background-image: none;
  line-height: 1.65;
}
h1, h2, h3 {
  color: var(--text);
  font-family: inherit;
  font-weight: 700;
  text-shadow: none;
}
a { color: var(--accent); text-shadow: none; }
a:hover { color: #7dbdff; }
a:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 2px;
  border-radius: 4px;
}
.skip {
  position: absolute;
  left: -9999px;
  top: 0;
  background: var(--accent);
  color: var(--accent-text);
  padding: 8px 14px;
  z-index: 10;
}
.skip:focus { left: 12px; top: 12px; }
.wrap {
  width: 100%;
  max-width: var(--max);
  margin: 0 auto;
  padding: 0 20px;
}
.site-header {
  display: block;
  position: sticky;
  top: 0;
  z-index: 5;
  background: var(--bg);
  border-bottom: 1px solid var(--border);
}
.site-header .wrap {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  min-height: 64px;
}
.wordmark {
  margin: 0;
  font-size: 18px;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  white-space: nowrap;
  color: var(--text);
  font-family: inherit;
}
.wordmark a {
  color: var(--text);
  text-decoration: none;
}
.site-nav {
  display: flex;
  flex-wrap: wrap;
  gap: 4px 20px;
  justify-content: flex-end;
}
.site-nav a {
  color: var(--text);
  text-decoration: none;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  padding: 6px 2px;
}
.site-nav a:hover { color: var(--accent); }
.hero { padding: 56px 0 8px; }
.hero h1 {
  margin: 0 0 12px;
  font-size: clamp(42px, 6vw, 60px);
  line-height: 1.05;
  letter-spacing: -0.02em;
  color: var(--text);
  font-family: inherit;
}
/* Hacker sets #main_content h1 to 30px with ID specificity. This restores the hero size. */
#main_content .hero h1 {
  font-size: clamp(42px, 6vw, 60px);
}
.hero p {
  margin: 0 0 24px;
  max-width: 640px;
  color: var(--muted);
  font-size: 18px;
}
.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}
.btn {
  display: inline-block;
  padding: 11px 20px;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 700;
  font-size: 15px;
  border: 1px solid transparent;
}
.btn-primary {
  background: var(--accent);
  color: var(--accent-text);
  border-color: var(--accent);
}
.btn-primary:hover { background: #7dbdff; color: var(--accent-text); border-color: #7dbdff; }
.btn-secondary {
  background: transparent;
  color: var(--text);
  border-color: var(--border);
}
.btn-secondary:hover { color: var(--text); border-color: var(--accent); }
section { scroll-margin-top: 84px; }
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  margin: 28px 0;
}
.card h2 {
  margin: 0 0 8px;
  font-size: 24px;
  line-height: 1.25;
  color: var(--text);
  font-family: inherit;
}
.card .section-note {
  margin: 0 0 16px;
  color: var(--muted);
}
.player {
  width: 100%;
  height: 400px;
  border: 0;
  border-radius: 10px;
  background: #000;
  display: block;
}
.mixcloud-link {
  display: inline-block;
  margin-top: 14px;
  font-weight: 600;
}
.about-layout {
  display: flex;
  gap: 24px;
  align-items: flex-start;
}
/* Hacker mobile CSS adds 20px side padding to every img, which squeezes the logo into an oval on phones. Clear it here. */
.logo-img {
  width: 120px;
  height: 120px;
  flex-shrink: 0;
  padding: 0;
  margin: 0;
  border-radius: 50%;
  object-fit: cover;
  border: 1px solid var(--border);
  background: var(--surface-2);
}
.about-layout p { margin: 0 0 14px; }
.about-layout p:last-child { margin-bottom: 0; }
.project-list {
  margin: 0;
  padding: 0;
  list-style: none;
}
/* Hacker sets a bullet image directly on ul li, which beats the inherited list-style above. Clear it on the items. */
.project-list li, .contact-list li {
  list-style: none;
}
.project {
  padding: 16px 0;
  border-top: 1px solid var(--border);
}
.project:first-child { border-top: 0; padding-top: 4px; }
.project:last-child { padding-bottom: 0; }
.project h3 {
  margin: 0 0 4px;
  font-size: 18px;
  line-height: 1.3;
  color: var(--text);
  font-family: inherit;
}
.project p { margin: 0 0 8px; color: var(--muted); }
.project-links {
  display: flex;
  flex-wrap: wrap;
  gap: 6px 16px;
  font-size: 14px;
  font-weight: 600;
}
.project-links a { text-decoration: none; }
.project-links a:hover { text-decoration: underline; }
.projects-more {
  display: inline-block;
  margin-top: 16px;
  font-weight: 600;
}
.contact-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  list-style: none;
  margin: 16px 0 0;
  padding: 0;
}
.contact-list a {
  display: inline-block;
  padding: 8px 16px;
  border: 1px solid var(--border);
  border-radius: 999px;
  color: var(--text);
  text-decoration: none;
  font-weight: 600;
  font-size: 14px;
  background: var(--surface-2);
}
.contact-list a:hover { border-color: var(--accent); color: var(--text); }
.coffee { text-align: center; margin: 36px 0 8px; }
footer {
  border-top: 1px solid var(--border);
  color: var(--muted);
  text-align: center;
  padding: 24px 0 36px;
  font-size: 14px;
}
@media (max-width: 640px) {
  .hero { padding-top: 40px; }
  .hero p { font-size: 17px; }
  .card { padding: 20px; }
  .about-layout { flex-direction: column; }
  .player { height: 360px; }
  /* Phone: stack the wordmark above the nav so the nav gets full width instead of squeezing into four tall rows beside it. */
  .site-header .wrap {
    flex-direction: column;
    justify-content: center;
    gap: 2px;
    min-height: 0;
    padding: 10px 20px;
  }
  .site-nav { justify-content: center; gap: 2px 14px; }
  .site-nav a { font-size: 13px; }
  section { scroll-margin-top: 118px; }
}
@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
}
</style>
</head>
<body>
<a class="skip" href="#mixes">Skip to latest mixes</a>
<div class="site-header" role="banner">
<div class="wrap">
<p class="wordmark"><a href="#top">Sassanix</a></p>
<nav class="site-nav" aria-label="Main navigation">
<a href="#mixes">Latest Mixes</a>
<a href="#about">About Me</a>
<a href="#projects">Open Source</a>
<a href="#contact">Contact Me</a>
</nav>
</div>
</div>
<main class="wrap" id="top">
<div class="hero">
<h1>Sassanix</h1>
<p>Listen to my latest mixes and see my latest creations.</p>
<div class="hero-actions">
<a class="btn btn-primary" href="#mixes">Listen to latest mixes</a>
<a class="btn btn-secondary" href="#contact">Get in touch</a>
</div>
</div>
<section class="card" id="mixes" aria-labelledby="mixes-heading">
<h2 id="mixes-heading">Latest Mixes</h2>
<iframe class="player" title="Latest Sassanix mixes on Mixcloud" loading="lazy" src="https://www.mixcloud.com/widget/iframe/?feed=%2FSassanix%2F"></iframe>
<a class="mixcloud-link" href="https://www.mixcloud.com/Sassanix/" target="_blank" rel="noopener">View all mixes on Mixcloud</a>
</section>
<section class="card" id="about" aria-labelledby="about-heading">
<h2 id="about-heading">About Me</h2>
<div class="about-layout">
<img class="logo-img" src="LS8Mx.gif" alt="Sassanix logo" width="120" height="120" decoding="async">
<div>
<p>I started getting into electronic music in 1999 while walking in a mall and hearing Paul van Dyk (PVD) blasting. Since then, I have been an advocate and a fan of various musical genres.</p>
<p>I have been mixing different styles of electronic music, including trance, since 2010, when I felt I needed to showcase my music to others. I am excited to make more mixes and to mix live.</p>
</div>
</div>
</section>
<section class="card" id="projects" aria-labelledby="projects-heading">
<h2 id="projects-heading">Open Source Projects</h2>
<p class="section-note">Recent open source work, most recently updated first.</p>
<ul class="project-list">
<li class="project">
<h3>Warracker</h3>
<p>An open source, self-hostable warranty tracker to monitor expirations, store receipts, and files. You own the data, your rules.</p>
<div class="project-links">
<a href="https://warracker.com" target="_blank" rel="noopener">Visit warracker.com</a>
<a href="https://github.com/sassanix/Warracker" target="_blank" rel="noopener">View on GitHub</a>
</div>
</li>
<li class="project">
<h3>wttrterminal</h3>
<p>Weather in your terminal using wttr.in, with setup for Windows PowerShell and Linux Bash.</p>
<div class="project-links">
<a href="https://github.com/sassanix/wttrterminal" target="_blank" rel="noopener">View on GitHub</a>
</div>
</li>
</ul>
<a class="projects-more" href="https://github.com/sassanix?tab=repositories" target="_blank" rel="noopener">View all repositories on GitHub</a>
</section>
<section class="card" id="contact" aria-labelledby="contact-heading">
<h2 id="contact-heading">Contact Me</h2>
<p class="section-note">Feel free to reach out to me through any of the following platforms:</p>
<ul class="contact-list">
<li><a href="https://www.reddit.com/message/compose/?to=Sassanix" target="_blank" rel="noopener">Reddit</a></li>
<!-- TODO: verify Discord link. It uses the old discordapp.com domain and discriminator format. Replace with your current Discord profile or server invite if this no longer works. -->
<li><a href="https://discordapp.com/users/Sassanix#0801/" target="_blank" rel="noopener">Discord</a></li>
<li><a href="https://www.mixcloud.com/Sassanix/" target="_blank" rel="noopener">Mixcloud</a></li>
<li><a href="https://open.spotify.com/user/sassanix" target="_blank" rel="noopener">Spotify</a></li>
<li><a href="https://www.facebook.com/sassanix" target="_blank" rel="noopener">Facebook</a></li>
<li><a href="https://soundcloud.com/sassanix" target="_blank" rel="noopener">Soundcloud</a></li>
<li><a href="https://www.reddit.com/r/sassanix" target="_blank" rel="noopener">Reddit Community</a></li>
</ul>
</section>
<!-- Buy Me a Coffee button. No defer: the script does not render the button with defer. -->
<div class="coffee">
<script
type="text/javascript"
src="https://cdnjs.buymeacoffee.com/1.0.0/button.prod.min.js"
data-name="bmc-button"
data-slug="sassanix"
data-color="#FFDD00"
data-emoji=""
data-font="Arial"
data-text="Buy me a coffee"
data-outline-color="#000000"
data-font-color="#000000"
data-coffee-color="#ffffff">
</script>
</div>
</main>
<footer>
<div class="wrap">
<p>&copy; 2026 Sassanix Music. All rights reserved.</p>
</div>
</footer>
</body>
</html>
