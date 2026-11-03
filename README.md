<!doctype html>
<html lang="nl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#09251A">
<meta name="description" content="NEXT Roleplay — jouw volgende verhaal begint hier.">
<title>NEXT Roleplay | FiveM</title>
<style>
:root {
  --site-primary:#12452D;
  --site-on-primary:#F1FFF6;
  --site-secondary:#39E879;
  --site-on-secondary:#09251A;
  --site-background:#09251A;
  --site-on-background:#F1FFF6;
  --site-font-body:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",sans-serif;
  --site-font-heading:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",sans-serif;
  --site-heading-scale:1;
  --site-spacing-scale:1;
  --site-radius-scale:1;
  --site-decoration-opacity:1;
  color-scheme:light dark;
}

* { box-sizing:border-box }
html { scroll-behavior:smooth }
body {
  margin:0;
  background:var(--site-background);
  color:var(--site-on-background);
  font-family:var(--site-font-body);
}
#app {
  min-height:100vh;
  width:100%;
  border-radius:0;
  overflow:hidden;
  background-color:light-dark(var(--site-background),var(--site-background));
  color:var(--site-on-background);
}
a { color:inherit;text-decoration:none }
button { font:inherit }
.container { width:min(1120px,calc(100% - 40px));margin:auto }

header {
  position:sticky;
  top:0;
  z-index:5;
  background:color-mix(in srgb,var(--site-background) 91%,transparent);
  backdrop-filter:blur(14px);
  border-bottom:1px solid #39e87922;
}
.nav {
  height:76px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}
.brand {
  display:flex;
  align-items:center;
  gap:11px;
  font-weight:950;
  letter-spacing:.08em;
}
.mark {
  width:39px;
  height:39px;
  display:grid;
  place-items:center;
  border-radius:12px;
  background:var(--site-secondary);
  color:var(--site-on-secondary);
  font-size:22px;
}
.brand span:last-child { font-size:16px }
nav {
  display:flex;
  gap:27px;
  color:#c1d7c9;
  font-size:13px;
  font-weight:750;
}
nav a:hover { color:var(--site-secondary) }

.cta,.primary {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:9px;
  padding:13px 19px;
  border:0;
  border-radius:10px;
  background:var(--site-secondary);
  color:var(--site-on-secondary);
  font-weight:900;
  font-size:13px;
  cursor:pointer;
  transition:.2s;
}
.cta:hover,.primary:hover {
  transform:translateY(-2px);
  box-shadow:0 10px 30px #39e87933;
}
.secondary {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:13px 19px;
  border:1px solid #cfffff33;
  border-radius:10px;
  color:#e7f6ec;
  font-weight:800;
  font-size:13px;
  background:#ffffff06;
}
.menu {
  display:none;
  background:transparent;
  color:white;
  border:1px solid #ffffff33;
  border-radius:9px;
  padding:9px 12px;
}

.hero {
  position:relative;
  padding:100px 0 90px;
  isolation:isolate;
}
.hero:before {
  content:"";
  position:absolute;
  z-index:-1;
  pointer-events:none;
  opacity:var(--site-decoration-opacity);
  width:600px;
  height:600px;
  right:-140px;
  top:-180px;
  border-radius:50%;
  background:radial-gradient(circle,#39e8792b,transparent 68%);
}
.hero-grid {
  display:grid;
  grid-template-columns:1.15fr .85fr;
  gap:60px;
  align-items:center;
}
.eyebrow,.kicker {
  color:var(--site-secondary);
  font-size:10px;
  font-weight:900;
  letter-spacing:.16em;
  text-transform:uppercase;
}
.eyebrow {
  display:inline-flex;
  align-items:center;
  gap:9px;
  padding:9px 13px;
  border:1px solid #39e87944;
  background:#39e8790d;
  border-radius:99px;
}
.pulse {
  width:7px;
  height:7px;
  border-radius:50%;
  background:var(--site-secondary);
  box-shadow:0 0 12px var(--site-secondary);
}
h1,h2,h3 { font-family:var(--site-font-heading) }
h1 {
  margin:24px 0 18px;
  font-size:clamp(46px,7vw,82px);
  line-height:.99;
  letter-spacing:-.065em;
  font-weight:1000;
}
h1 em { font-style:normal;color:var(--site-secondary) }
.copy {
  max-width:530px;
  color:#b4c9bb;
  font-size:16px;
  line-height:1.8;
}
.actions {
  display:flex;
  gap:12px;
  flex-wrap:wrap;
  margin-top:28px;
}
.note {
  margin-top:21px;
  color:#789987;
  font-size:11px;
  letter-spacing:.05em;
}
.server-card {
  padding:27px;
  border:1px solid #69ed9730;
  border-radius:22px;
  background:linear-gradient(145deg,#12452df2,#0a2a1cf2);
  box-shadow:0 30px 90px #0004;
}
.card-top {
  display:flex;
  justify-content:space-between;
  color:#b7d2c0;
  font-size:10px;
  font-weight:850;
  letter-spacing:.13em;
}
.live { color:var(--site-secondary) }
.emblem {
  width:82px;
  height:82px;
  display:grid;
  place-items:center;
  margin:34px auto 20px;
  border-radius:24px;
  background:var(--site-secondary);
  color:var(--site-on-secondary);
  font-size:42px;
  font-weight:1000;
  box-shadow:0 0 55px #39e87933;
}
.server-card h2 { text-align:center;margin:0;font-size:24px }
.sub {
  text-align:center;
  color:#9bb8a5;
  font-size:12px;
  margin:8px 0 27px;
}
.info {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}
.cell {
  padding:13px;
  border-radius:12px;
  background:#03180f55;
  border:1px solid #ffffff10;
}
.cell small {
  display:block;
  color:#86a995;
  font-size:9px;
  text-transform:uppercase;
  letter-spacing:.12em;
  margin-bottom:7px;
}
.cell strong { font-size:13px }

.section { padding:82px 0 }
.alt {
  background:#12452d55;
  border-block:1px solid #39e87915;
}
.section-head { max-width:650px;margin-bottom:36px }
h2.title {
  font-size:clamp(30px,4vw,45px);
  letter-spacing:-.05em;
  line-height:1.1;
  margin:12px 0;
}
.desc {
  color:#a7beaf;
  line-height:1.75;
  font-size:14px;
}
.features {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px;
}
.feature {
  padding:25px;
  border-radius:16px;
  background:var(--site-primary);
  border:1px solid #8bffb11a;
  min-height:185px;
}
.ico {
  width:42px;
  height:42px;
  display:grid;
  place-items:center;
  background:#39e87920;
  color:var(--site-secondary);
  border-radius:12px;
  font-size:20px;
}
.feature h3 { font-size:17px;margin:18px 0 8px }
.feature p {
  margin:0;
  color:#a7beaf;
  font-size:12px;
  line-height:1.75;
}
.team {
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:14px;
}
.member {
  padding:22px 18px;
  background:#12452da6;
  border:1px solid #8bffb11a;
  border-radius:15px;
}
.owner { border-color:#39e87966 }
.avatar {
  width:46px;
  height:46px;
  display:grid;
  place-items:center;
  border-radius:14px;
  background:#39e87922;
  color:var(--site-secondary);
  font-weight:1000;
  font-size:17px;
  margin-bottom:18px;
}
.member strong { display:block;font-size:14px }
.member span {
  display:block;
  margin-top:6px;
  color:#91b19d;
  font-size:11px;
}
.join-panel {
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:25px;
  padding:35px;
  border-radius:20px;
  background:linear-gradient(110deg,#12452d,#0e3825);
  border:1px solid #39e87933;
}
.join-panel h2 { font-size:30px;letter-spacing:-.05em;margin:8px 0 }
.join-panel p { color:#b0c9b9;font-size:13px;margin:0 }
footer { padding:30px 0;color:#789987;font-size:11px }
.footer-row {
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}
.footer-brand { color:#e6f5eb;font-weight:900;letter-spacing:.1em }
.toast {
  position:fixed;
  bottom:22px;
  left:50%;
  transform:translate(-50%,20px);
  opacity:0;
  pointer-events:none;
  padding:12px 17px;
  background:#e8fff0;
  color:#09251a;
  border-radius:10px;
  font-size:12px;
  font-weight:800;
  transition:.25s;
  z-index:10;
}
.toast.show { opacity:1;transform:translate(-50%,0) }

@media(max-width:800px) {
  .hero-grid { grid-template-columns:1fr;gap:38px }
  .hero { padding:70px 0 }
  .server-card { max-width:520px }
  .features { grid-template-columns:1fr 1fr }
  .team { grid-template-columns:1fr 1fr }
}
@media(max-width:560px) {
  .container { width:calc(100% - 30px) }
  nav {
    display:none;
    position:absolute;
    top:76px;
    left:0;
    right:0;
    padding:20px;
    background:#09251a;
    flex-direction:column;
    border-bottom:1px solid #39e87933;
  }
  nav.open { display:flex }
  .menu { display:block }
  .nav>.cta { display:none }
  .features,.team { grid-template-columns:1fr }
  .join-panel {
    align-items:flex-start;
    flex-direction:column;
    padding:25px;
  }
  .footer-row { align-items:flex-start;flex-direction:column }
  .section { padding:62px 0 }
}
</style>
</head>

<body>
<div id="app">
<header>
<div class="container nav">
<a class="brand" href="#home">
<span class="mark">N</span>
<span>NEXT ROLEPLAY</span>
</a>
<nav id="nav">
<a href="#over">Over ons</a>
<a href="#features">Waarom NEXT</a>
<a href="#team">Staffteam</a>
<a href="#join">Join de server</a>
</nav>
<a class="cta" href="#join">SPEEL MEE ↗</a>
<button class="menu" id="menu" aria-label="Menu openen" aria-expanded="false">☰</button>
</div>
</header>

<main id="home">
<section class="hero">
<div class="container hero-grid">
<div>
<div class="eyebrow"><span class="pulse"></span> JOUW VERHAAL. JOUW NEXT STEP.</div>
<h1>DIT IS JOUW<br><em>NEXT</em> LEVEL.</h1>
<p class="copy">
Welkom bij NEXT Roleplay. Duik in een wereld waar jouw keuzes het verschil maken, ontmoet nieuwe mensen en schrijf samen een verhaal dat helemaal van jou is.
</p>
<div class="actions">
<a class="primary" href="#join">ONTDEK DE SERVER ↗</a>
<a class="secondary" href="#over">MEER OVER ONS</a>
</div>
<div class="note">FIVEM ROLEPLAY • COMMUNITY • JOUW AVONTUUR</div>
</div>

<aside class="server-card">
<div class="card-top">
<span>NEXT NETWORK</span>
<span class="live">● COMMUNITY</span>
</div>
<div class="emblem">N</div>
<h2>NEXT ROLEPLAY</h2>
<p class="sub">Jouw volgende verhaal begint hier.</p>
<div class="info">
<div class="cell"><small>Eigenaar</small><strong>LabinoGames</strong></div>
<div class="cell"><small>Platform</small><strong>FiveM</strong></div>
<div class="cell"><small>Discord</small><strong>Link volgt</strong></div>
<div class="cell"><small>Joincode</small><strong>Wordt aangevuld</strong></div>
</div>
</aside>
</div>
</section>

<section class="section alt" id="over">
<div class="container">
<div class="section-head">
<div class="kicker">WELKOM BIJ NEXT</div>
<h2 class="title">Meer dan een server.<br>Een wereld om in te leven.</h2>
<p class="desc">
Bij NEXT Roleplay draait het om samen beleven, creativiteit en plezier. Of je nu je eerste stappen zet of al een ervaren roleplayer bent: jouw verhaal krijgt hier alle ruimte.
</p>
</div>
<div class="features" id="features">
<article class="feature">
<div class="ico">✦</div>
<h3>Jouw eigen verhaal</h3>
<p>Maak keuzes, bouw relaties op en geef je personage een eigen identiteit.</p>
</article>
<article class="feature">
<div class="ico">⌘</div>
<h3>Een sterke community</h3>
<p>Ontmoet andere spelers en maak samen onvergetelijke roleplay-momenten.</p>
</article>
<article class="feature">
<div class="ico">⬡</div>
<h3>Een team dat klaarstaat</h3>
<p>Ons staffteam helpt mee aan een fijne en aangename speelervaring.</p>
</article>
</div>
</div>
</section>

<section class="section" id="team">
<div class="container">
<div class="section-head">
<div class="kicker">DE MENSEN ACHTER NEXT</div>
<h2 class="title">Maak kennis met het team.</h2>
<p class="desc">Een community bouw je samen. Dit zijn de mensen die NEXT Roleplay mee vormgeven.</p>
</div>
<div class="team">
<article class="member owner">
<div class="avatar">L</div>
<strong>LabinoGames</strong>
<span>Eigenaar</span>
</article>
<article class="member">
<div class="avatar">I</div>
<strong>Iben</strong>
<span>Website Developer</span>
</article>
<article class="member">
<div class="avatar">B</div>
<strong>Benny</strong>
<span>STAFF-Team</span>
</article>
<article class="member">
<div class="avatar">V</div>
<strong>Vince</strong>
<span>STAFF-Team</span>
</article>
</div>
</div>
</section>

<section class="section alt" id="join">
<div class="container">
<div class="join-panel">
<div>
<div class="kicker">KLAAR VOOR JOUW NEXT?</div>
<h2>Jouw avontuur wacht.</h2>
<p>Sluit je aan bij NEXT Roleplay en ontdek wat er mogelijk is.</p>
</div>
<div class="actions" style="margin:0">
<button class="primary" id="discord">JOIN DISCORD ↗</button>
<button class="secondary" id="fivem">FIVEM JOINCODE</button>
</div>
</div>
<p style="color:#789987;font-size:11px;margin:15px 2px 0">
De Discord-link en FiveM Cfx-joincode worden toegevoegd zodra ze beschikbaar zijn.
</p>
</div>
</section>
</main>

<footer>
<div class="container footer-row">
<div class="footer-brand">NEXT ROLEPLAY</div>
<div>© <span id="year"></span> NEXT Roleplay · Alle rechten voorbehouden</div>
<div>Website door Iben</div>
</div>
</footer>

<div class="toast" id="toast" role="status" aria-live="polite"></div>
</div>

<script>
// Vul hieronder de echte links en code in zodra je ze hebt.
const CONFIG = {
  discordUrl: "",
  fivemJoinCode: "",
  domain: "www.nextroleplay.be"
};

const nav = document.getElementById("nav");
const menu = document.getElementById("menu");

menu.addEventListener("click", () => {
  const open = nav.classList.toggle("open");
  menu.setAttribute("aria-expanded", String(open));
});

nav.querySelectorAll("a").forEach(a => {
  a.addEventListener("click", () => {
    nav.classList.remove("open");
    menu.setAttribute("aria-expanded", "false");
  });
});

document.getElementById("year").textContent = new Date().getFullYear();

let timer;

function toast(message) {
  const element = document.getElementById("toast");
  element.textContent = message;
  element.classList.add("show");
  clearTimeout(timer);
  timer = setTimeout(() => element.classList.remove("show"), 2600);
}

document.getElementById("discord").addEventListener("click", () => {
  if (CONFIG.discordUrl) {
    window.open(CONFIG.discordUrl, "_blank", "noopener");
  } else {
    toast("Discord-link nog niet ingesteld. Vul deze in bij CONFIG in het HTML-bestand.");
  }
});

document.getElementById("fivem").addEventListener("click", () => {
  if (!CONFIG.fivemJoinCode) {
    toast("Cfx-joincode nog niet ingesteld. Vul deze in bij CONFIG in het HTML-bestand.");
    return;
  }

  const code = CONFIG.fivemJoinCode.trim()
    .replace(/^https?:\/\/cfx\.re\/join\//i, "")
    .replace(/^cfx\.re\/join\//i, "");

  if (!code) {
    toast("Vul een geldige Cfx-joincode in bij CONFIG.");
    return;
  }

  window.open("https://cfx.re/join/" + encodeURIComponent(code), "_blank", "noopener");
});
</script>
</body>
</html>
```
