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
  /* Logo colours sampled from LS8Mx.gif: red #f3241e, cream #ffe7c1. */
  --accent: #f3241e;
  --accent-hover: #ff5a4e;
  --cream: #ffe7c1;
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
  color: var(--cream);
  font-family: inherit;
  font-weight: 700;
  text-shadow: none;
}
a { color: var(--accent); text-shadow: none; }
a:hover { color: var(--accent-hover); }
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
  color: var(--cream);
  font-family: inherit;
}
.wordmark a {
  color: var(--cream);
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
  color: var(--cream);
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
.btn-primary:hover { background: var(--accent-hover); color: var(--accent-text); border-color: var(--accent-hover); }
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
  color: var(--cream);
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
  display: flex;
  gap: 16px;
  align-items: flex-start;
  padding: 16px 0;
  border-top: 1px solid var(--border);
}
/* Project logos. Padding and margin are cleared here for the same reason as .logo-img: Hacker mobile CSS adds 20px side padding to every img. */
.project-logo {
  width: 56px;
  height: 56px;
  flex-shrink: 0;
  padding: 0;
  margin: 0;
  object-fit: contain;
}
.weather-logo {
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--surface-2);
  border: 1px solid var(--border);
  border-radius: 12px;
  color: var(--cream);
}
.weather-logo svg {
  width: 32px;
  height: 32px;
}
.project-body { min-width: 0; }
.project:first-child { border-top: 0; padding-top: 4px; }
.project:last-child { padding-bottom: 0; }
.project h3 {
  margin: 0 0 4px;
  font-size: 18px;
  line-height: 1.3;
  color: var(--cream);
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
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: 1px solid var(--border);
  border-radius: 999px;
  color: var(--text);
  text-decoration: none;
  font-weight: 600;
  font-size: 14px;
  background: var(--surface-2);
}
.contact-list svg {
  width: 18px;
  height: 18px;
  flex-shrink: 0;
}
.contact-list a:hover { border-color: var(--accent); color: var(--text); }
.contact-subheading {
  margin: 20px 0 0;
  font-size: 16px;
}
.contact-subheading + .contact-list { margin-top: 8px; }
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
<img class="project-logo" src="warracker-logo.png" alt="Warracker logo" width="56" height="56" decoding="async">
<div class="project-body">
<h3>Warracker</h3>
<p>An open source, self-hostable warranty tracker to monitor expirations, store receipts, and files. You own the data, your rules.</p>
<div class="project-links">
<a href="https://warracker.com" target="_blank" rel="noopener">Visit warracker.com</a>
<a href="https://github.com/sassanix/Warracker" target="_blank" rel="noopener">View on GitHub</a>
</div>
</div>
</li>
<li class="project">
<!-- Weather icon: Lucide cloud-sun, ISC licence. -->
<span class="project-logo weather-logo" aria-hidden="true"><svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" focusable="false"><path d="M12 2v2"/><path d="m4.93 4.93 1.41 1.41"/><path d="M20 12h2"/><path d="m19.07 4.93-1.41 1.41"/><path d="M15.947 12.65a4 4 0 0 0-5.925-4.128"/><path d="M13 22H7a5 5 0 1 1 4.9-6H13a3 3 0 0 1 0 6Z"/></svg></span>
<div class="project-body">
<h3>wttrterminal</h3>
<p>Weather in your terminal using wttr.in, with setup for Windows PowerShell and Linux Bash.</p>
<div class="project-links">
<a href="https://github.com/sassanix/wttrterminal" target="_blank" rel="noopener">View on GitHub</a>
</div>
</div>
</li>
</ul>
<a class="projects-more" href="https://github.com/sassanix?tab=repositories" target="_blank" rel="noopener">View all repositories on GitHub</a>
</section>
<section class="card" id="contact" aria-labelledby="contact-heading">
<h2 id="contact-heading">Contact Me</h2>
<p class="section-note">Feel free to reach out to me through any of the following platforms:</p>
<!-- Brand icons: Simple Icons v16.37.0 (CC0-1.0). Mixcloud and Facebook colours lightened for the dark background. GitHub mark in white, its brand colour is near black. -->
<ul class="contact-list">
<li><a href="https://www.reddit.com/message/compose/?to=Sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#FF4500" aria-hidden="true" focusable="false"><path d="M12 0C5.373 0 0 5.373 0 12c0 3.314 1.343 6.314 3.515 8.485l-2.286 2.286C.775 23.225 1.097 24 1.738 24H12c6.627 0 12-5.373 12-12S18.627 0 12 0Zm4.388 3.199c1.104 0 1.999.895 1.999 1.999 0 1.105-.895 2-1.999 2-.946 0-1.739-.657-1.947-1.539v.002c-1.147.162-2.032 1.15-2.032 2.341v.007c1.776.067 3.4.567 4.686 1.363.473-.363 1.064-.58 1.707-.58 1.547 0 2.802 1.254 2.802 2.802 0 1.117-.655 2.081-1.601 2.531-.088 3.256-3.637 5.876-7.997 5.876-4.361 0-7.905-2.617-7.998-5.87-.954-.447-1.614-1.415-1.614-2.538 0-1.548 1.255-2.802 2.803-2.802.645 0 1.239.218 1.712.585 1.275-.79 2.881-1.291 4.64-1.365v-.01c0-1.663 1.263-3.034 2.88-3.207.188-.911.993-1.595 1.959-1.595Zm-8.085 8.376c-.784 0-1.459.78-1.506 1.797-.047 1.016.64 1.429 1.426 1.429.786 0 1.371-.369 1.418-1.385.047-1.017-.553-1.841-1.338-1.841Zm7.406 0c-.786 0-1.385.824-1.338 1.841.047 1.017.634 1.385 1.418 1.385.785 0 1.473-.413 1.426-1.429-.046-1.017-.721-1.797-1.506-1.797Zm-3.703 4.013c-.974 0-1.907.048-2.77.135-.147.015-.241.168-.183.305.483 1.154 1.622 1.964 2.953 1.964 1.33 0 2.47-.81 2.953-1.964.057-.137-.037-.29-.184-.305-.863-.087-1.795-.135-2.769-.135Z"/></svg>Reddit</a></li>
<!-- TODO: verify Discord link. It uses the old discordapp.com domain and discriminator format. Replace with your current Discord profile or server invite if this no longer works. -->
<li><a href="https://discordapp.com/users/Sassanix#0801/" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#5865F2" aria-hidden="true" focusable="false"><path d="M20.317 4.3698a19.7913 19.7913 0 00-4.8851-1.5152.0741.0741 0 00-.0785.0371c-.211.3753-.4447.8648-.6083 1.2495-1.8447-.2762-3.68-.2762-5.4868 0-.1636-.3933-.4058-.8742-.6177-1.2495a.077.077 0 00-.0785-.037 19.7363 19.7363 0 00-4.8852 1.515.0699.0699 0 00-.0321.0277C.5334 9.0458-.319 13.5799.0992 18.0578a.0824.0824 0 00.0312.0561c2.0528 1.5076 4.0413 2.4228 5.9929 3.0294a.0777.0777 0 00.0842-.0276c.4616-.6304.8731-1.2952 1.226-1.9942a.076.076 0 00-.0416-.1057c-.6528-.2476-1.2743-.5495-1.8722-.8923a.077.077 0 01-.0076-.1277c.1258-.0943.2517-.1923.3718-.2914a.0743.0743 0 01.0776-.0105c3.9278 1.7933 8.18 1.7933 12.0614 0a.0739.0739 0 01.0785.0095c.1202.099.246.1981.3728.2924a.077.077 0 01-.0066.1276 12.2986 12.2986 0 01-1.873.8914.0766.0766 0 00-.0407.1067c.3604.698.7719 1.3628 1.225 1.9932a.076.076 0 00.0842.0286c1.961-.6067 3.9495-1.5219 6.0023-3.0294a.077.077 0 00.0313-.0552c.5004-5.177-.8382-9.6739-3.5485-13.6604a.061.061 0 00-.0312-.0286zM8.02 15.3312c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9555-2.4189 2.157-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.9555 2.4189-2.1569 2.4189zm7.9748 0c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9554-2.4189 2.1569-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.946 2.4189-2.1568 2.4189Z"/></svg>Discord</a></li>
<li><a href="https://www.mixcloud.com/Sassanix/" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#7C4DFF" aria-hidden="true" focusable="false"><path d="M2.462 8.596l1.372 6.49h.319l1.372-6.49h2.462v6.808H6.742v-5.68l.232-.81h-.402l-1.43 6.49H2.854l-1.44-6.49h-.391l.222.81v5.68H0V8.596zM24 8.63v1.429L21.257 12 24 13.941v1.43l-3.235-2.329h-.348l-3.226 2.329v-1.43l2.734-1.94-2.733-1.942V8.63l3.225 2.338h.348zm-7.869 2.75v1.24H9.304v-1.24z"/></svg>Mixcloud</a></li>
<li><a href="https://open.spotify.com/user/sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#1ED760" aria-hidden="true" focusable="false"><path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z"/></svg>Spotify</a></li>
<li><a href="https://soundcloud.com/sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#FF5500" aria-hidden="true" focusable="false"><path d="M23.999 14.165c-.052 1.796-1.612 3.169-3.4 3.169h-8.18a.68.68 0 0 1-.675-.683V7.862a.747.747 0 0 1 .452-.724s.75-.513 2.333-.513a5.364 5.364 0 0 1 2.763.755 5.433 5.433 0 0 1 2.57 3.54c.282-.08.574-.121.868-.12.884 0 1.73.358 2.347.992s.948 1.49.922 2.373ZM10.721 8.421c.247 2.98.427 5.697 0 8.672a.264.264 0 0 1-.53 0c-.395-2.946-.22-5.718 0-8.672a.264.264 0 0 1 .53 0ZM9.072 9.448c.285 2.659.37 4.986-.006 7.655a.277.277 0 0 1-.55 0c-.331-2.63-.256-5.02 0-7.655a.277.277 0 0 1 .556 0Zm-1.663-.257c.27 2.726.39 5.171 0 7.904a.266.266 0 0 1-.532 0c-.38-2.69-.257-5.21 0-7.904a.266.266 0 0 1 .532 0Zm-1.647.77a26.108 26.108 0 0 1-.008 7.147.272.272 0 0 1-.542 0 27.955 27.955 0 0 1 0-7.147.275.275 0 0 1 .55 0Zm-1.67 1.769c.421 1.865.228 3.5-.029 5.388a.257.257 0 0 1-.514 0c-.21-1.858-.398-3.549 0-5.389a.272.272 0 0 1 .543 0Zm-1.655-.273c.388 1.897.26 3.508-.01 5.412-.026.28-.514.283-.54 0-.244-1.878-.347-3.54-.01-5.412a.283.283 0 0 1 .56 0Zm-1.668.911c.4 1.268.257 2.292-.026 3.572a.257.257 0 0 1-.514 0c-.241-1.262-.354-2.312-.023-3.572a.283.283 0 0 1 .563 0Z"/></svg>Soundcloud</a></li>
<li><a href="https://github.com/sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#FFFFFF" aria-hidden="true" focusable="false"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>GitHub</a></li>
</ul>
<h3 class="contact-subheading">Social media pages</h3>
<ul class="contact-list">
<li><a href="https://www.facebook.com/sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#4A8DFF" aria-hidden="true" focusable="false"><path d="M9.101 23.691v-7.98H6.627v-3.667h2.474v-1.58c0-4.085 1.848-5.978 5.858-5.978.401 0 .955.042 1.468.103a8.68 8.68 0 0 1 1.141.195v3.325a8.623 8.623 0 0 0-.653-.036 26.805 26.805 0 0 0-.733-.009c-.707 0-1.259.096-1.675.309a1.686 1.686 0 0 0-.679.622c-.258.42-.374.995-.374 1.752v1.297h3.919l-.386 2.103-.287 1.564h-3.246v8.245C19.396 23.238 24 18.179 24 12.044c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.628 3.874 10.35 9.101 11.647Z"/></svg>Facebook</a></li>
<li><a href="https://www.reddit.com/r/sassanix" target="_blank" rel="noopener"><svg class="contact-icon" width="18" height="18" viewBox="0 0 24 24" fill="#FF4500" aria-hidden="true" focusable="false"><path d="M12 0C5.373 0 0 5.373 0 12c0 3.314 1.343 6.314 3.515 8.485l-2.286 2.286C.775 23.225 1.097 24 1.738 24H12c6.627 0 12-5.373 12-12S18.627 0 12 0Zm4.388 3.199c1.104 0 1.999.895 1.999 1.999 0 1.105-.895 2-1.999 2-.946 0-1.739-.657-1.947-1.539v.002c-1.147.162-2.032 1.15-2.032 2.341v.007c1.776.067 3.4.567 4.686 1.363.473-.363 1.064-.58 1.707-.58 1.547 0 2.802 1.254 2.802 2.802 0 1.117-.655 2.081-1.601 2.531-.088 3.256-3.637 5.876-7.997 5.876-4.361 0-7.905-2.617-7.998-5.87-.954-.447-1.614-1.415-1.614-2.538 0-1.548 1.255-2.802 2.803-2.802.645 0 1.239.218 1.712.585 1.275-.79 2.881-1.291 4.64-1.365v-.01c0-1.663 1.263-3.034 2.88-3.207.188-.911.993-1.595 1.959-1.595Zm-8.085 8.376c-.784 0-1.459.78-1.506 1.797-.047 1.016.64 1.429 1.426 1.429.786 0 1.371-.369 1.418-1.385.047-1.017-.553-1.841-1.338-1.841Zm7.406 0c-.786 0-1.385.824-1.338 1.841.047 1.017.634 1.385 1.418 1.385.785 0 1.473-.413 1.426-1.429-.046-1.017-.721-1.797-1.506-1.797Zm-3.703 4.013c-.974 0-1.907.048-2.77.135-.147.015-.241.168-.183.305.483 1.154 1.622 1.964 2.953 1.964 1.33 0 2.47-.81 2.953-1.964.057-.137-.037-.29-.184-.305-.863-.087-1.795-.135-2.769-.135Z"/></svg>Reddit Community</a></li>
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
<p>&copy; 2026 Sassanix. All rights reserved.</p>
</div>
</footer>
</body>
</html>
