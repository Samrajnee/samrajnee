<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samrajnee Bhattacharjee — Profile Preview</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

:root{
  --navy:#0e1628;
  --navy-mid:#16213a;
  --navy-card:#1b2740;
  --surface:#f5f3ee;
  --surface-2:#eae6dc;
  --white:#faf9f6;
  --gold:#c8a96e;
  --gold-lt:#e2c98a;
  --gold-dim:rgba(200,169,110,0.18);
  --txt:#1a1f30;
  --txt-mid:#3d4562;
  --txt-muted:#7a82a0;
  --divider:rgba(200,169,110,0.2);
}

html{scroll-behavior:smooth}

body{
  background:var(--surface);
  color:var(--txt);
  font-family:'DM Sans',sans-serif;
  font-weight:300;
  line-height:1.7;
  overflow-x:hidden;
  min-height:100vh;
}

/* grain overlay */
body::after{
  content:'';
  position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='g'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23g)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events:none;z-index:9999;opacity:1;
}

.wrap{max-width:840px;margin:0 auto;padding:0 32px}

/* ─── HERO ─── */
.hero{
  background:var(--navy);
  padding:72px 0 0;
  position:relative;
  overflow:hidden;
}

/* mesh blobs */
.hero::before{
  content:'';position:absolute;inset:0;
  background:
    radial-gradient(ellipse 55% 70% at 90% 10%,rgba(200,169,110,0.07) 0%,transparent 55%),
    radial-gradient(ellipse 35% 55% at 10% 90%,rgba(200,169,110,0.04) 0%,transparent 60%);
  pointer-events:none;
}

.hero-grid{
  display:grid;
  grid-template-columns:1fr auto;
  align-items:end;
  gap:40px;
  position:relative;
}

.eyebrow{
  font-size:10.5px;font-weight:500;
  letter-spacing:0.24em;text-transform:uppercase;
  color:var(--gold);margin-bottom:18px;
  opacity:0;animation:up .6s ease .05s forwards;
}

h1.name{
  font-family:'Fraunces',serif;
  font-size:clamp(44px,5.5vw,72px);
  font-weight:300;line-height:1.02;
  color:var(--white);letter-spacing:-0.025em;
  opacity:0;animation:up .65s ease .15s forwards;
}
h1.name em{font-style:italic;color:var(--gold-lt)}

.tagline{
  font-size:14.5px;font-weight:300;
  color:rgba(250,249,246,.5);
  max-width:400px;margin-top:18px;
  line-height:1.65;
  opacity:0;animation:up .65s ease .28s forwards;
}

.badges{
  display:flex;flex-wrap:wrap;gap:8px;
  margin-top:30px;margin-bottom:48px;
  opacity:0;animation:up .65s ease .38s forwards;
}

.badge{
  display:inline-flex;align-items:center;gap:5px;
  padding:5px 13px;
  border:1px solid rgba(200,169,110,.28);
  border-radius:100px;
  font-size:11px;font-weight:400;
  letter-spacing:0.05em;
  color:rgba(250,249,246,.65);
  background:rgba(255,255,255,.03);
  backdrop-filter:blur(6px);
  transition:border-color .3s,color .3s;
}
.badge:hover{border-color:var(--gold);color:var(--gold-lt)}
.dot{width:5px;height:5px;border-radius:50%;background:var(--gold)}

/* ─── STATS ─── */
.stats{
  display:grid;grid-template-columns:repeat(4,1fr);
  background:var(--navy-mid);
  border-top:1px solid rgba(200,169,110,.1);
  opacity:0;animation:up .6s ease .5s forwards;
}

.stat{
  padding:18px 0;text-align:center;
  border-right:1px solid rgba(200,169,110,.08);
}
.stat:last-child{border-right:none}

.stat-n{
  font-family:'Fraunces',serif;
  font-size:24px;font-weight:400;
  color:var(--gold-lt);line-height:1;
}
.stat-l{
  font-size:9.5px;font-weight:500;
  letter-spacing:.16em;text-transform:uppercase;
  color:rgba(250,249,246,.3);margin-top:5px;
}

/* ─── BODY ─── */
.body{padding:64px 0 80px}

.section{margin-bottom:56px}

.sec-label{
  font-size:9.5px;font-weight:500;
  letter-spacing:.26em;text-transform:uppercase;
  color:var(--gold);margin-bottom:26px;
  display:flex;align-items:center;gap:14px;
}
.sec-label::after{
  content:'';flex:1;height:1px;
  background:var(--divider);
}

/* About */
.about{
  font-family:'Fraunces',serif;
  font-size:18.5px;font-weight:300;
  line-height:1.8;color:var(--txt-mid);
  max-width:620px;
}
.about strong{color:var(--txt);font-weight:400}

/* Cards */
.card{
  background:var(--white);
  border:1px solid var(--surface-2);
  border-radius:14px;
  padding:32px;
  box-shadow:0 2px 18px rgba(14,22,40,.055),0 1px 3px rgba(14,22,40,.035);
  position:relative;overflow:hidden;
  transition:box-shadow .35s,transform .35s;
}
.card:hover{
  box-shadow:0 6px 36px rgba(14,22,40,.09),0 2px 6px rgba(14,22,40,.05);
  transform:translateY(-2px);
}
.card::before{
  content:'';
  position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--gold) 0%,transparent 75%);
}

.card-top{display:flex;align-items:flex-start;justify-content:space-between;gap:16px;margin-bottom:14px}

.card-title{
  font-family:'Fraunces',serif;
  font-size:22px;font-weight:400;
  color:var(--txt);letter-spacing:-.01em;
}

.status-pill{
  font-size:9.5px;font-weight:500;
  letter-spacing:.14em;text-transform:uppercase;
  color:var(--gold);
  background:rgba(200,169,110,.1);
  border:1px solid rgba(200,169,110,.22);
  padding:4px 10px;border-radius:100px;
  white-space:nowrap;flex-shrink:0;
}

.card-desc{
  font-size:14px;color:var(--txt-mid);
  line-height:1.72;margin-bottom:18px;
}

.chips{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:18px}
.chip{
  font-size:10.5px;font-weight:500;
  letter-spacing:.06em;color:var(--txt-mid);
  background:var(--surface-2);
  padding:3px 9px;border-radius:5px;
}

.cta{
  font-size:11.5px;font-weight:500;
  letter-spacing:.1em;text-transform:uppercase;
  color:var(--gold);text-decoration:none;
  display:inline-flex;align-items:center;gap:6px;
  transition:gap .2s;
}
.cta:hover{gap:10px}

/* 2-col mini cards */
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.mini-card{
  background:var(--white);
  border:1px solid var(--surface-2);
  border-radius:12px;padding:20px 22px;
  box-shadow:0 1px 6px rgba(14,22,40,.04);
  transition:box-shadow .3s,transform .3s;
}
.mini-card:hover{
  box-shadow:0 4px 18px rgba(14,22,40,.08);
  transform:translateY(-1px);
}
.mini-cat{
  font-size:9.5px;font-weight:500;
  letter-spacing:.2em;text-transform:uppercase;
  color:var(--gold);margin-bottom:9px;
}
.mini-body{font-size:13px;color:var(--txt-mid);line-height:1.85}

/* Timeline */
.tl-item{
  display:grid;grid-template-columns:110px 1fr;
  gap:24px;padding:22px 0;
  border-bottom:1px solid var(--divider);
}
.tl-item:last-child{border-bottom:none}
.tl-date{
  font-size:10.5px;font-weight:400;
  letter-spacing:.05em;color:var(--txt-muted);
  text-align:right;padding-top:4px;
}
.tl-role{
  font-family:'Fraunces',serif;
  font-size:15.5px;font-weight:400;
  color:var(--txt);margin-bottom:3px;
}
.tl-org{
  font-size:11.5px;font-weight:500;
  letter-spacing:.06em;color:var(--gold);
  margin-bottom:7px;
}
.tl-desc{font-size:13px;color:var(--txt-mid);line-height:1.65}
.tl-desc strong{color:var(--txt);font-weight:500}

/* Honours */
.honours{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.hon{
  background:var(--white);border:1px solid var(--surface-2);
  border-radius:10px;padding:18px 20px;
  box-shadow:0 1px 5px rgba(14,22,40,.04);
  transition:box-shadow .3s;
}
.hon:hover{box-shadow:0 4px 16px rgba(14,22,40,.07)}
.hon-title{
  font-family:'Fraunces',serif;
  font-size:14.5px;font-weight:400;
  color:var(--txt);margin-bottom:4px;
}
.hon-sub{font-size:11.5px;color:var(--txt-muted);letter-spacing:.02em}

/* Connect */
.connect{display:flex;flex-wrap:wrap;gap:10px;align-items:center}
.link{
  display:inline-flex;align-items:center;gap:7px;
  padding:8px 16px;
  border:1px solid var(--surface-2);border-radius:8px;
  font-size:12.5px;font-weight:400;
  color:var(--txt-mid);text-decoration:none;
  background:var(--white);
  box-shadow:0 1px 4px rgba(14,22,40,.04);
  transition:border-color .25s,color .25s,box-shadow .25s;
}
.link:hover{
  border-color:var(--gold);color:var(--txt);
  box-shadow:0 3px 12px rgba(200,169,110,.12);
}

/* Footer */
footer{
  background:var(--navy);
  padding:28px 0;text-align:center;
  font-size:11px;color:rgba(250,249,246,.25);
  letter-spacing:.1em;
}

/* Animations */
@keyframes up{
  from{opacity:0;transform:translateY(14px)}
  to{opacity:1;transform:translateY(0)}
}
.ani{opacity:0;animation:up .55s ease forwards}

/* Responsive */
@media(max-width:600px){
  .hero-grid{grid-template-columns:1fr}
  .stats{grid-template-columns:repeat(2,1fr)}
  .grid2{grid-template-columns:1fr}
  .honours{grid-template-columns:1fr}
  .tl-item{grid-template-columns:1fr;gap:4px}
  .tl-date{text-align:left}
}
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="wrap">
    <div class="hero-grid">
      <div>
        <p class="eyebrow">CSE · MAKAUT · Kolkata, India</p>
        <h1 class="name">Samrajnee<br><em>Bhattacharjee</em></h1>
        <p class="tagline">
          Full-stack engineer building infrastructure for academia —<br>
          precision-first, placement-ready.
        </p>
        <div class="badges">
          <span class="badge"><span class="dot"></span> Open to SWE Internships &amp; Placements 2026</span>
          <span class="badge">SGPA 8.83 / 10</span>
          <span class="badge">Kolkata, India</span>
        </div>
      </div>
    </div>
  </div>
  <div class="stats">
    <div class="stat"><div class="stat-n">8.83</div><div class="stat-l">SGPA / 10</div></div>
    <div class="stat"><div class="stat-n">45%</div><div class="stat-l">TTH Reduction</div></div>
    <div class="stat"><div class="stat-n">4</div><div class="stat-l">Languages</div></div>
    <div class="stat"><div class="stat-n">3+</div><div class="stat-l">Live Projects</div></div>
  </div>
</section>

<!-- BODY -->
<main class="body">
  <div class="wrap">

    <!-- ABOUT -->
    <section class="section">
      <p class="sec-label">About</p>
      <p class="about ani">
        Third-year CSE undergraduate at MAKAUT with a dual identity: I write <strong>production-grade full-stack code</strong> and I've led cross-functional teams, managed <strong>international partnerships</strong>, and shipped live products. Currently building <strong>CampusChain</strong> — a distributed campus governance and identity platform — and targeting placements at <strong>product MNCs, consulting &amp; fintech</strong>.
      </p>
    </section>

    <!-- FEATURED PROJECT -->
    <section class="section">
      <p class="sec-label">Featured Project</p>
      <div class="card ani">
        <div class="card-top">
          <h2 class="card-title">CampusChain</h2>
          <span class="status-pill">Active · 2025–Present</span>
        </div>
        <p class="card-desc">
          A full-stack student-institution platform covering campus governance, digital identity &amp; reputation systems, and operational workflows. Built with event-driven architecture, role-based access control, and a clean service layer — designed to scale.
        </p>
        <div class="chips">
          <span class="chip">React</span><span class="chip">Vite</span><span class="chip">TailwindCSS</span>
          <span class="chip">Node.js</span><span class="chip">Express</span>
          <span class="chip">Prisma</span><span class="chip">PostgreSQL</span>
          <span class="chip">REST API</span>
        </div>
        <a href="https://github.com/Samrajnee" class="cta">View on GitHub →</a>
      </div>
    </section>

    <!-- OTHER PROJECTS -->
    <section class="section">
      <p class="sec-label">Other Work</p>
      <div class="grid2 ani">
        <div class="mini-card">
          <p class="mini-cat">Developer Portfolio</p>
          <p class="mini-body">Responsive personal site via GitHub Pages — HTML5, CSS3, JS. Mobile-first, end-to-end deployed.</p>
        </div>
        <div class="mini-card">
          <p class="mini-cat">Global Innovation Summit</p>
          <p class="mini-body">Front-end event website for Swastikk AI Tech. Live at globalinnovationsummit.netlify.app</p>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section class="section">
      <p class="sec-label">Technical Skills</p>
      <div class="grid2 ani">
        <div class="mini-card">
          <p class="mini-cat">Languages</p>
          <p class="mini-body">Java (DSA) · Python · C · JavaScript · HTML5 · CSS3</p>
        </div>
        <div class="mini-card">
          <p class="mini-cat">Frameworks &amp; Tools</p>
          <p class="mini-body">React · Vite · Tailwind · Node.js · Express · Prisma · Git</p>
        </div>
        <div class="mini-card">
          <p class="mini-cat">Databases</p>
          <p class="mini-body">PostgreSQL · MySQL · Oracle XE · Prisma ORM</p>
        </div>
        <div class="mini-card">
          <p class="mini-cat">CS Foundations</p>
          <p class="mini-body">OOP · DBMS · OS · Computer Networks · Data Structures</p>
        </div>
      </div>
    </section>

    <!-- EXPERIENCE -->
    <section class="section">
      <p class="sec-label">Experience</p>
      <div class="ani">
        <div class="tl-item">
          <span class="tl-date">May – Jul 2025</span>
          <div>
            <p class="tl-role">Full-Stack Developer Intern</p>
            <p class="tl-org">MSME Times · Remote</p>
            <p class="tl-desc">Led platform development strategy, backend data workflow organisation, and digital performance optimisation for a business media outlet targeting the MSME sector.</p>
          </div>
        </div>
        <div class="tl-item">
          <span class="tl-date">Mar – Jun 2025</span>
          <div>
            <p class="tl-role">Assistant Manager — Human Resources</p>
            <p class="tl-org">MSME &amp; Startups Accelerator Forum · Remote</p>
            <p class="tl-desc">Redesigned end-to-end hiring workflows, reducing average time-to-hire by <strong>45%</strong>. Led a 5-member team against tight operational deadlines.</p>
          </div>
        </div>
        <div class="tl-item">
          <span class="tl-date">May 2024 – Jun 2025</span>
          <div>
            <p class="tl-role">Chief Management Officer (Co-founder)</p>
            <p class="tl-org">Swastikk AI Tech Pvt. Ltd. · Jamshedpur</p>
            <p class="tl-desc">Negotiated an MoU with Emmy Pencil (CEO, Nexus Mars &amp; Gugu Robotics, Nigeria). Established research collaboration with George Mason University, USA. Directed the Global Innovation Summit end-to-end.</p>
          </div>
        </div>
        <div class="tl-item">
          <span class="tl-date">Mar – Apr 2025</span>
          <div>
            <p class="tl-role">Executive Associate to the Director</p>
            <p class="tl-org">MSME &amp; Startups Accelerator Forum · Remote</p>
            <p class="tl-desc">Coordinated digital strategy and served as primary liaison for high-profile clients, sponsors, and strategic partners.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- HONOURS -->
    <section class="section">
      <p class="sec-label">Honours &amp; Recognition</p>
      <div class="honours ani">
        <div class="hon">
          <p class="hon-title">Award of Excellence</p>
          <p class="hon-sub">Steel Authority of India (SAIL)</p>
        </div>
        <div class="hon">
          <p class="hon-title">Grand Finalist</p>
          <p class="hon-sub">Smart Bengal Hackathon · Govt. of West Bengal</p>
        </div>
        <div class="hon">
          <p class="hon-title">Best Speaker of the Event</p>
          <p class="hon-sub">Public Speaking &amp; Leadership Award</p>
        </div>
        <div class="hon">
          <p class="hon-title">School Topper</p>
          <p class="hon-sub">First Class with Distinction · Secondary &amp; Higher Secondary Boards</p>
        </div>
      </div>
    </section>

    <!-- LANGUAGES -->
    <section class="section">
      <p class="sec-label">Languages</p>
      <div class="grid2 ani">
        <div class="mini-card">
          <p class="mini-cat">Native / Bilingual</p>
          <p class="mini-body">Bengali (C2) · Hindi (C2)</p>
        </div>
        <div class="mini-card">
          <p class="mini-cat">Professional / Working</p>
          <p class="mini-body">English (C1 Full Professional) · German (A2–B1)</p>
        </div>
      </div>
    </section>

    <!-- CONNECT -->
    <section class="section">
      <p class="sec-label">Connect</p>
      <div class="connect ani">
        <a href="mailto:samrajnee30@gmail.com" class="link">✉ samrajnee30@gmail.com</a>
        <a href="https://linkedin.com/in/samrajneebhattacharjee" class="link">in LinkedIn</a>
        <a href="https://github.com/Samrajnee" class="link">⌥ GitHub</a>
        <a href="https://instagram.com/so_called_sam" class="link">◎ @so_called_sam</a>
      </div>
    </section>

  </div>
</main>

<footer>
  <div class="wrap">
    Samrajnee Bhattacharjee &nbsp;·&nbsp; MAKAUT &nbsp;·&nbsp; Kolkata, India &nbsp;·&nbsp; 2025
  </div>
</footer>

<script>
// Animate sections on scroll
const obs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.style.animationDelay = '0s';
      e.target.style.animationPlayState = 'running';
      obs.unobserve(e.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll('.ani').forEach(el => {
  el.style.animationPlayState = 'paused';
  obs.observe(el);
});
</script>

</body>
</html>
