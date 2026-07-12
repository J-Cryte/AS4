<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>AS4 — AI Systems For South African Businesses</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --void:#0C0C10;
  --s1:#111116;
  --s2:#17171E;
  --s3:#1E1E27;
  --iron:#26262F;
  --iron2:#32323E;
  --white:#F0EEE8;
  --fog:#84837C;
  --fog2:#A8A79F;
  --gold:#E8A030;
  --gold2:#F5C870;
  --gold-dim:rgba(232,160,48,0.09);
  --gold-border:rgba(232,160,48,0.18);
}
html{scroll-behavior:smooth}
body{background:var(--void);color:var(--white);font-family:'Inter',sans-serif;font-size:16px;line-height:1.7;-webkit-font-smoothing:antialiased;overflow-x:hidden}
::-webkit-scrollbar{width:3px}
::-webkit-scrollbar-track{background:var(--void)}
::-webkit-scrollbar-thumb{background:var(--iron2);border-radius:2px}

/* ── TYPOGRAPHY ── */
.sg{font-family:'Space Grotesk',sans-serif}
.jb{font-family:'JetBrains Mono',monospace}

/* ── LAYOUT ── */
.wrap{max-width:1120px;margin:0 auto;padding:0 44px}

/* ── NAV ── */
nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(12,12,16,0.92);backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);border-bottom:1px solid var(--iron)}
.nav-in{max-width:1120px;margin:0 auto;padding:0 44px;height:60px;display:flex;align-items:center;justify-content:space-between}
.logo{font-family:'Space Grotesk',sans-serif;font-size:19px;font-weight:700;letter-spacing:-0.025em;color:var(--white);text-decoration:none;display:flex;align-items:baseline;gap:1px}
.logo-4{color:var(--gold)}
.nav-links{display:flex;align-items:center;gap:28px;list-style:none}
.nav-links a{font-size:13px;font-weight:500;color:var(--fog);text-decoration:none;transition:color .18s}
.nav-links a:hover{color:var(--white)}
.nav-cta{background:var(--gold)!important;color:#0C0C10!important;font-weight:700!important;padding:8px 20px;border-radius:3px;transition:opacity .18s!important}
.nav-cta:hover{opacity:.86!important}

/* ── HERO ── */
.hero{min-height:100vh;display:flex;align-items:center;padding-top:60px;position:relative;overflow:hidden}
.hero-bg{position:absolute;inset:0;pointer-events:none}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(var(--iron) 1px,transparent 1px),linear-gradient(90deg,var(--iron) 1px,transparent 1px);background-size:64px 64px;opacity:.11;mask-image:radial-gradient(ellipse 85% 75% at 50% 40%,black 15%,transparent 100%)}
.hero-glow{position:absolute;top:10%;right:5%;width:640px;height:480px;background:radial-gradient(ellipse,rgba(232,160,48,0.065) 0%,transparent 65%);pointer-events:none}
.hero-glow2{position:absolute;bottom:0;left:0;width:400px;height:300px;background:radial-gradient(ellipse,rgba(232,160,48,0.04) 0%,transparent 70%);pointer-events:none}
.hero-content{position:relative;z-index:2;padding:80px 0}

.location-tag{display:inline-flex;align-items:center;gap:8px;margin-bottom:36px}
.location-dot{width:5px;height:5px;background:var(--gold);border-radius:50%;animation:ldot 2.8s ease-in-out infinite}
@keyframes ldot{0%,100%{opacity:1;box-shadow:0 0 0 0 rgba(232,160,48,0.5)}50%{opacity:.6;box-shadow:0 0 0 5px rgba(232,160,48,0)}}
.location-tag span{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--fog);letter-spacing:0.1em;text-transform:uppercase}

.hero-title{font-family:'Space Grotesk',sans-serif;font-size:clamp(44px,6vw,86px);font-weight:700;letter-spacing:-0.038em;line-height:1.0;margin-bottom:24px;max-width:820px}
.hero-title em{font-style:normal;color:var(--gold)}

.hero-sub{font-size:clamp(15px,1.6vw,18px);color:var(--fog2);max-width:480px;line-height:1.68;margin-bottom:44px}

.hero-actions{display:flex;align-items:center;gap:18px;flex-wrap:wrap;margin-bottom:72px}
.btn-primary{display:inline-flex;align-items:center;gap:7px;background:var(--gold);color:#0C0C10;font-family:'Inter',sans-serif;font-size:14px;font-weight:700;padding:13px 26px;border-radius:3px;text-decoration:none;transition:opacity .18s,transform .18s;letter-spacing:0.01em}
.btn-primary:hover{opacity:.87;transform:translateY(-1px)}
.btn-ghost{display:inline-flex;align-items:center;gap:7px;background:transparent;color:var(--fog2);font-family:'Inter',sans-serif;font-size:14px;font-weight:500;padding:13px 0;text-decoration:none;transition:color .18s}
.btn-ghost:hover{color:var(--white)}

.hero-stats{display:grid;grid-template-columns:repeat(4,1fr);border-top:1px solid var(--iron);padding-top:36px;gap:0}
.hstat{padding-right:32px;border-right:1px solid var(--iron)}
.hstat:last-child{border-right:none}
.hstat-n{font-family:'JetBrains Mono',monospace;font-size:28px;font-weight:500;color:var(--white);display:block;line-height:1;letter-spacing:-0.02em}
.hstat-n em{font-style:normal;color:var(--gold);font-size:18px}
.hstat-l{font-size:11px;color:var(--fog);letter-spacing:0.08em;text-transform:uppercase;margin-top:7px;display:block;line-height:1.4}

/* ── TICKER ── */
.ticker{overflow:hidden;padding:13px 0;border-top:1px solid var(--iron);border-bottom:1px solid var(--iron);background:var(--s1)}
.ticker-track{display:flex;animation:tick 34s linear infinite;white-space:nowrap}
.ti{display:inline-flex;align-items:center;gap:18px;padding:0 32px;font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--fog);letter-spacing:.09em}
.ti .d{width:3px;height:3px;background:var(--gold);border-radius:50%;flex-shrink:0}
@keyframes tick{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

/* ── SECTION BASE ── */
.sec{padding:104px 0}
.sec-label{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--gold);letter-spacing:0.14em;text-transform:uppercase;display:block;margin-bottom:20px}
.sec-title{font-family:'Space Grotesk',sans-serif;font-size:clamp(22px,2.8vw,36px);font-weight:700;letter-spacing:-0.025em;line-height:1.18}

/* ── PAIN ── */
.pain-wrap{background:var(--s1);padding:80px 0;border-top:1px solid var(--iron);border-bottom:1px solid var(--iron)}
.pain-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--iron);margin-top:52px}
.pain-card{background:var(--s1);padding:36px 28px;transition:background .2s}
.pain-card:hover{background:var(--s2)}
.pain-icon{font-size:22px;margin-bottom:14px;display:block}
.pain-card h3{font-family:'Space Grotesk',sans-serif;font-size:16px;font-weight:600;margin-bottom:9px;letter-spacing:-0.01em}
.pain-card p{font-size:13.5px;color:var(--fog);line-height:1.68}
.pain-fix{font-size:11.5px;color:var(--gold);margin-top:13px;font-weight:600;letter-spacing:0.03em;display:block}

/* ── SERVICES — TIER SYSTEM ── */
.services-wrap{background:var(--void)}

/* Tier band — each tier is a full-width block with increasing visual weight */
.tier-band{border-top:1px solid var(--iron);position:relative}
.tier-band:last-child{border-bottom:1px solid var(--iron)}

.tier-header{display:grid;grid-template-columns:280px 1fr;gap:0;align-items:stretch}
.tier-label-col{padding:48px 44px;border-right:1px solid var(--iron);display:flex;flex-direction:column;justify-content:center;position:sticky;top:60px}
.tier-num{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--fog);letter-spacing:0.12em;margin-bottom:12px;display:block}
.tier-name{font-family:'Space Grotesk',sans-serif;font-size:22px;font-weight:700;letter-spacing:-0.02em;line-height:1.2;margin-bottom:10px}
.tier-tag{font-size:12px;color:var(--fog);line-height:1.5;max-width:200px}
.tier-badge{display:inline-block;font-size:10px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;padding:4px 10px;border-radius:2px;margin-top:16px}

/* Tier 1 */
.tier-1 .tier-label-col{background:var(--s1)}
.tier-1 .tier-name{color:var(--white)}
.tier-1 .tier-badge{background:var(--iron);color:var(--fog2)}

/* Tier 2 */
.tier-2 .tier-label-col{background:var(--s2)}
.tier-2 .tier-name{color:var(--white)}
.tier-2 .tier-badge{background:rgba(232,160,48,0.08);color:var(--gold);border:1px solid var(--gold-border)}

/* Tier 3 */
.tier-3 .tier-label-col{background:var(--s3)}
.tier-3 .tier-name{color:var(--gold)}
.tier-3 .tier-badge{background:var(--gold);color:#0C0C10}

.tier-services-col{display:grid;gap:1px;background:var(--iron)}

/* Tier 1 background */
.tier-1 .tier-services-col{background:var(--iron)}
.tier-1 .svc-item{background:var(--s1)}
.tier-1 .svc-item:hover{background:var(--s2)}

/* Tier 2 background */
.tier-2 .tier-services-col{background:var(--iron)}
.tier-2 .svc-item{background:var(--s2)}
.tier-2 .svc-item:hover{background:var(--s3)}

/* Tier 3 background */
.tier-3 .tier-services-col{background:var(--iron)}
.tier-3 .svc-item{background:var(--s3)}
.tier-3 .svc-item:hover{background:rgba(232,160,48,0.04)}

.svc-item{padding:36px 44px;transition:background .2s;position:relative;display:grid;grid-template-columns:1fr auto;align-items:start;gap:24px}
.svc-item-text{}
.svc-item h3{font-family:'Space Grotesk',sans-serif;font-size:17px;font-weight:600;letter-spacing:-0.01em;margin-bottom:8px}
.svc-item p{font-size:13.5px;color:var(--fog);line-height:1.68;max-width:540px}
.svc-item-arr{color:var(--iron2);font-size:16px;transition:color .2s,transform .2s;padding-top:4px;flex-shrink:0}
.svc-item:hover .svc-item-arr{color:var(--gold);transform:translate(3px,-3px)}

/* Tier 3 item arrow always gold-tinted */
.tier-3 .svc-item-arr{color:rgba(232,160,48,0.3)}
.tier-3 .svc-item:hover .svc-item-arr{color:var(--gold)}

/* ── PROCESS ── */
.process-sec{background:var(--s1);border-top:1px solid var(--iron)}
.process-list{margin-top:56px}
.p-step{display:grid;grid-template-columns:56px 1fr 340px;gap:40px;padding:44px 0;border-bottom:1px solid var(--iron);align-items:start}
.p-step:last-child{border-bottom:none}
.p-num{font-family:'JetBrains Mono',monospace;font-size:13px;color:var(--gold);padding-top:2px}
.p-step h3{font-family:'Space Grotesk',sans-serif;font-size:19px;font-weight:600;letter-spacing:-0.01em;margin-bottom:9px}
.p-step > div:nth-child(2) p{font-size:14px;color:var(--fog);line-height:1.7}
.p-meta{font-size:13px;color:var(--fog);line-height:1.7;padding-top:2px}
.p-tag{font-family:'JetBrains Mono',monospace;font-size:10.5px;color:var(--fog2);background:var(--iron);padding:3px 9px;border-radius:2px;display:inline-block;margin-bottom:8px;letter-spacing:0.04em}

/* ── RESULTS ── */
.results-sec{background:var(--void)}
.results-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--iron);border:1px solid var(--iron);border-radius:4px;overflow:hidden;margin-top:56px;margin-bottom:64px}
.r-cell{background:var(--s1);padding:32px 24px;text-align:center}
.r-big{font-family:'JetBrains Mono',monospace;font-size:40px;font-weight:500;color:var(--white);letter-spacing:-0.03em;display:block;line-height:1}
.r-big .a{color:var(--gold)}
.r-lbl{font-size:11px;color:var(--fog);text-transform:uppercase;letter-spacing:.08em;margin-top:10px;display:block;line-height:1.4}

.case-block{background:var(--s2);border:1px solid var(--iron);border-left:3px solid var(--gold);border-radius:4px;padding:44px;display:grid;grid-template-columns:1fr 1fr;gap:52px;align-items:center}
.case-q{font-family:'Space Grotesk',sans-serif;font-size:18px;font-weight:500;line-height:1.58;color:var(--white);letter-spacing:-0.01em}
.case-q::before{content:'\201C';color:var(--gold)}
.case-q::after{content:'\201D';color:var(--gold)}
.case-who{margin-top:18px}
.case-who strong{color:var(--white);font-size:13.5px;font-weight:600;display:block}
.case-who span{color:var(--fog);font-size:13px}
.c-num-row{display:flex;align-items:baseline;gap:14px;padding:16px 0;border-bottom:1px solid var(--iron)}
.c-num-row:last-child{border-bottom:none}
.c-n{font-family:'JetBrains Mono',monospace;font-size:24px;color:var(--gold2);font-weight:500;min-width:70px}
.c-d{font-size:13.5px;color:var(--fog)}

/* ── PRICING ── */
.pricing-sec{background:var(--s1);border-top:1px solid var(--iron)}
.pricing-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:56px}
.pc{background:var(--void);border:1px solid var(--iron);border-radius:4px;padding:40px 32px;position:relative;transition:border-color .2s}
.pc:hover{border-color:var(--iron2)}
.pc.hot{border-color:var(--gold);background:var(--s2)}
.pc.hot::before{content:'MOST POPULAR';position:absolute;top:-1px;left:50%;transform:translateX(-50%);background:var(--gold);color:#0C0C10;font-size:9.5px;font-weight:700;letter-spacing:.13em;padding:4px 13px;border-radius:0 0 3px 3px;white-space:nowrap}
.pc-tier{font-family:'JetBrains Mono',monospace;font-size:10px;font-weight:500;letter-spacing:.14em;text-transform:uppercase;color:var(--fog);display:block;margin-bottom:16px}
.pc-price{font-family:'Space Grotesk',sans-serif;font-size:42px;font-weight:700;letter-spacing:-0.03em;color:var(--white);line-height:1;display:block;margin-bottom:5px}
.pc-price .cur{font-size:20px;color:var(--fog);font-weight:500;vertical-align:super}
.pc-cycle{font-size:12.5px;color:var(--fog);display:block;margin-bottom:24px}
.pc-desc{font-size:13.5px;color:var(--fog2);line-height:1.65;margin-bottom:24px;padding-bottom:24px;border-bottom:1px solid var(--iron)}
.pc-includes{font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--gold);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:14px;display:block}
.pc-feats{list-style:none;display:flex;flex-direction:column;gap:10px;margin-bottom:32px}
.pc-feats li{font-size:13.5px;color:var(--fog2);display:flex;align-items:flex-start;gap:9px;line-height:1.5}
.pc-feats li::before{content:'→';color:var(--gold);flex-shrink:0;font-size:11px;margin-top:2px}
.btn-tier{display:block;width:100%;text-align:center;font-family:'Inter',sans-serif;font-size:13.5px;font-weight:600;padding:12px 20px;border-radius:3px;text-decoration:none;cursor:pointer;transition:all .18s}
.btn-tier-ghost{background:transparent;color:var(--fog2);border:1px solid var(--iron2)}
.btn-tier-ghost:hover{border-color:var(--fog);color:var(--white)}
.btn-tier-gold{background:var(--gold);color:#0C0C10;border:1px solid var(--gold)}
.btn-tier-gold:hover{opacity:.87}

.pc-retainer{display:flex;align-items:center;justify-content:space-between;margin-bottom:24px;padding:10px 14px;background:var(--iron);border-radius:3px;border:1px solid var(--iron2)}
.pc-retainer-price{font-family:'JetBrains Mono',monospace;font-size:16px;font-weight:500;color:var(--white)}
.pc-retainer-price em{font-style:normal;font-size:11px;color:var(--fog);margin-left:1px}
.pc-retainer-label{font-size:11px;color:var(--fog);letter-spacing:0.05em;text-transform:uppercase}
.pc.hot .pc-retainer{background:rgba(232,160,48,0.08);border-color:rgba(232,160,48,0.2)}
.pc.hot .pc-retainer-price{color:var(--gold)}
.pc.hot .pc-retainer-price em{color:var(--gold2)}
.rand-note{text-align:center;margin-top:18px;font-size:13px;color:var(--fog)}
.rand-note span{color:var(--gold)}

/* ── CTA ── */
.cta-sec{background:var(--s2);border-top:1px solid var(--iron)}
.cta-in{display:grid;grid-template-columns:1fr auto;align-items:center;gap:64px;padding:88px 0}
.cta-chip{display:inline-block;background:var(--gold-dim);color:var(--gold2);font-family:'JetBrains Mono',monospace;font-size:10.5px;font-weight:500;letter-spacing:.1em;text-transform:uppercase;padding:5px 13px;border-radius:2px;margin-bottom:18px;border:1px solid var(--gold-border)}
.cta-in h2{font-family:'Space Grotesk',sans-serif;font-size:clamp(21px,2.8vw,34px);font-weight:700;letter-spacing:-0.025em;max-width:500px;margin-bottom:14px;line-height:1.18}
.cta-in p{color:var(--fog2);font-size:15.5px;max-width:440px;line-height:1.6}
.cta-sub{font-size:12px;color:var(--fog);text-align:center;margin-top:12px}

/* ── FOOTER ── */
footer{padding:52px 0 32px;border-top:1px solid var(--iron)}
.ft{display:grid;grid-template-columns:1.5fr 1fr 1fr 1fr;gap:52px;padding-bottom:36px;border-bottom:1px solid var(--iron);margin-bottom:28px}
.ft-brand .logo{display:inline-flex;margin-bottom:12px}
.ft-brand p{font-size:13.5px;color:var(--fog);line-height:1.7;max-width:230px}
.ft-loc{font-size:11px;color:var(--fog);margin-top:11px;font-family:'JetBrains Mono',monospace;letter-spacing:.04em}
.ft-col h4{font-size:10.5px;font-weight:600;letter-spacing:.12em;text-transform:uppercase;color:var(--fog);margin-bottom:16px}
.ft-col ul{list-style:none;display:flex;flex-direction:column;gap:9px}
.ft-col a{font-size:13.5px;color:var(--fog);text-decoration:none;transition:color .18s}
.ft-col a:hover{color:var(--white)}
.ft-bot{display:flex;justify-content:space-between;align-items:center}
.ft-bot p{font-size:11.5px;color:var(--fog)}
.ft-bot a{font-size:11.5px;color:var(--fog);text-decoration:none;transition:color .18s}
.ft-bot a:hover{color:var(--fog2)}
.ft-bot a span{color:var(--gold)}

/* ── SCROLL REVEAL ── */
.sr{opacity:0;transform:translateY(18px);transition:opacity .6s ease,transform .6s ease}
.sr.in{opacity:1;transform:none}

/* ── MOBILE ── */
@media(max-width:960px){
  .wrap,.nav-in,.hero-content{padding-left:24px;padding-right:24px}
  .nav-links{display:none}
  .hero-stats{grid-template-columns:repeat(2,1fr);gap:1px;background:var(--iron)}
  .hstat{background:var(--void);padding:20px 16px;border-right:none}
  .tier-header{grid-template-columns:1fr}
  .tier-label-col{position:relative;top:0;border-right:none;border-bottom:1px solid var(--iron)}
  .svc-item{grid-template-columns:1fr}
  .svc-item-arr{display:none}
  .p-step{grid-template-columns:44px 1fr;gap:20px}
  .p-meta{display:none}
  .results-grid{grid-template-columns:repeat(2,1fr)}
  .case-block,.cta-in{grid-template-columns:1fr;gap:32px}
  .pricing-grid{grid-template-columns:1fr}
  .ft{grid-template-columns:1fr 1fr;gap:36px}
}
@media(max-width:580px){
  .results-grid{grid-template-columns:1fr 1fr}
  .ft{grid-template-columns:1fr}
  .ft-bot{flex-direction:column;gap:8px;text-align:center}
  .pain-grid{grid-template-columns:1fr}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-in">
    <a href="#" class="logo"><span>AS</span><span class="logo-4">4</span></a>
    <ul class="nav-links">
      <li><a href="#services">Services</a></li>
      <li><a href="#process">Process</a></li>
      <li><a href="#results">Results</a></li>
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#contact" class="nav-cta">Talk to us</a></li>
    </ul>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg">
    <div class="hero-grid"></div>
    <div class="hero-glow"></div>
    <div class="hero-glow2"></div>
  </div>
  <div class="hero-content wrap">
    <div class="location-tag">
      <div class="location-dot"></div>
      <span>George, Western Cape — AI Systems for SA Businesses</span>
    </div>
    <h1 class="hero-title">
      Your business.<br>Running on <em>autopilot.</em>
    </h1>
    <p class="hero-sub">
      AS4 builds custom AI systems for South African businesses — from lead capture to intelligent automation. No dollar-priced software. No generic tools. Priced in rand.
    </p>
    <div class="hero-actions">
      <a href="#contact" class="btn-primary">Talk to us →</a>
      <a href="#services" class="btn-ghost">See what we build →</a>
    </div>
    <div class="hero-stats">
      <div class="hstat">
        <span class="hstat-n">60<em>%</em></span>
        <span class="hstat-l">Less manual work</span>
      </div>
      <div class="hstat">
        <span class="hstat-n">3<em>×</em></span>
        <span class="hstat-l">More output, same team</span>
      </div>
      <div class="hstat">
        <span class="hstat-n">14<em>d</em></span>
        <span class="hstat-l">First system delivered</span>
      </div>
      <div class="hstat">
        <span class="hstat-n">R<em>ZAR</em></span>
        <span class="hstat-l">Always priced in rand</span>
      </div>
    </div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-track">
    <span class="ti"><span class="d"></span>LEAD CAPTURE</span>
    <span class="ti"><span class="d"></span>REVIEW AUTOMATION</span>
    <span class="ti"><span class="d"></span>APPOINTMENT REMINDERS</span>
    <span class="ti"><span class="d"></span>QUOTE REQUESTS</span>
    <span class="ti"><span class="d"></span>CLIENT ONBOARDING</span>
    <span class="ti"><span class="d"></span>PROPOSAL AUTOMATION</span>
    <span class="ti"><span class="d"></span>AI LEAD QUALIFICATION</span>
    <span class="ti"><span class="d"></span>AI KNOWLEDGE BASE</span>
    <span class="ti"><span class="d"></span>AI CONTENT ENGINE</span>
    <span class="ti"><span class="d"></span>LEAD CAPTURE</span>
    <span class="ti"><span class="d"></span>REVIEW AUTOMATION</span>
    <span class="ti"><span class="d"></span>APPOINTMENT REMINDERS</span>
    <span class="ti"><span class="d"></span>QUOTE REQUESTS</span>
    <span class="ti"><span class="d"></span>CLIENT ONBOARDING</span>
    <span class="ti"><span class="d"></span>PROPOSAL AUTOMATION</span>
    <span class="ti"><span class="d"></span>AI LEAD QUALIFICATION</span>
    <span class="ti"><span class="d"></span>AI KNOWLEDGE BASE</span>
    <span class="ti"><span class="d"></span>AI CONTENT ENGINE</span>
  </div>
</div>

<!-- PAIN -->
<div class="pain-wrap sr">
  <div class="wrap">
    <span class="sec-label">We know the SA reality</span>
    <h2 class="sec-title">Your team is stretched.<br>The economy doesn't give more room.</h2>
    <div class="pain-grid">
      <div class="pain-card">
        <span class="pain-icon">⚡</span>
        <h3>Eskom has taken enough</h3>
        <p>Load shedding kills momentum and halts production. Our cloud-based AI systems keep running — before, during, and after every stage.</p>
        <span class="pain-fix">→ Systems that don't stop when the grid does</span>
      </div>
      <div class="pain-card">
        <span class="pain-icon">💸</span>
        <h3>Dollar software hurts more every month</h3>
        <p>Salesforce, HubSpot, Zapier — priced in dollars, getting worse as the rand weakens. We build systems priced in rand, for SA operations.</p>
        <span class="pain-fix">→ Everything invoiced in ZAR. No surprises.</span>
      </div>
      <div class="pain-card">
        <span class="pain-icon">📱</span>
        <h3>WhatsApp chaos eating your day</h3>
        <p>Quotes, follow-ups, bookings, queries — all landing on your phone. We automate the repetitive parts so you focus on actual work.</p>
        <span class="pain-fix">→ Automated follow-ups and client management</span>
      </div>
      <div class="pain-card">
        <span class="pain-icon">🏃</span>
        <h3>You're doing five jobs at once</h3>
        <p>Owner, marketer, admin, salesperson. Your time is the scarcest resource. AI takes over the repetitive tasks so you can run the business.</p>
        <span class="pain-fix">→ Automation that gives your hours back</span>
      </div>
      <div class="pain-card">
        <span class="pain-icon">📊</span>
        <h3>Month-end is a nightmare</h3>
        <p>Hours lost to spreadsheets and reports. We build systems that generate reports automatically — so you always know where you stand without the effort.</p>
        <span class="pain-fix">→ Automated reports delivered on schedule</span>
      </div>
      <div class="pain-card">
        <span class="pain-icon">🔄</span>
        <h3>You can't scale what's manual</h3>
        <p>What works for 5 clients won't hold for 50. We build infrastructure that grows with your business without adding to your payroll.</p>
        <span class="pain-fix">→ Systems that scale as you grow</span>
      </div>
    </div>
  </div>
</div>

<!-- SERVICES — TIER SYSTEM -->
<section id="services" class="services-wrap">
  <div class="wrap" style="padding-top:80px;padding-bottom:16px">
    <span class="sec-label sr">What we build</span>
    <h2 class="sec-title sr">Three tiers. Built for where<br>your business is right now.</h2>
    <p style="color:var(--fog2);font-size:15px;margin-top:16px;max-width:520px;line-height:1.65" class="sr">Start at the tier that fits. Move up as you grow. Every system is custom-built for your operation — not templated software with your logo on it.</p>
  </div>

  <!-- TIER 1 -->
  <div class="tier-band tier-1 sr" style="margin-top:48px">
    <div class="tier-header">
      <div class="tier-label-col">
        <span class="tier-num">TIER 01</span>
        <span class="tier-name">Basic<br>Systems</span>
        <span class="tier-tag">Plug the leaks. Stop losing leads, bookings, and reviews to manual gaps.</span>
        <span class="tier-badge">R2,500 SETUP · R1,500/MONTH</span>
      </div>
      <div class="tier-services-col">
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Lead Capture &amp; Notification System</h3>
            <p>Automatically captures leads from your website, social media, or ads and instantly notifies your team — so no enquiry ever goes cold while it sits in an inbox.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Review Request Automation</h3>
            <p>Sends review requests to clients at exactly the right moment after a job or purchase — automatically. More Google reviews, less asking awkwardly in person.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Appointment Reminder System</h3>
            <p>Automated reminders sent via WhatsApp, SMS, or email before every booking — reducing no-shows without your team lifting a finger for each one.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Quote Request System</h3>
            <p>A structured intake flow that captures all the information you need for a quote — then routes it to the right person instantly, every time.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
      </div>
    </div>
  </div>

  <!-- TIER 2 -->
  <div class="tier-band tier-2 sr">
    <div class="tier-header">
      <div class="tier-label-col">
        <span class="tier-num">TIER 02</span>
        <span class="tier-name">Higher<br>Value</span>
        <span class="tier-tag">Build the machine. Systems that run your operations without you in the middle.</span>
        <span class="tier-badge">R4,500 SETUP · R2,500/MONTH</span>
      </div>
      <div class="tier-services-col">
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Client Onboarding Automation</h3>
            <p>From signed contract to fully onboarded client — automated. Welcome messages, document collection, access provisioning, and kick-off scheduling handled without manual steps.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Employee Onboarding System</h3>
            <p>New hire joins — the system kicks in. Contracts sent, training materials delivered, task checklists assigned, and HR notifications triggered automatically from day one.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>Proposal &amp; Document Automation</h3>
            <p>Generate professional, branded proposals and documents from a simple input — populated with client details, pricing, and scope automatically. Send in minutes, not hours.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
      </div>
    </div>
  </div>

  <!-- TIER 3 -->
  <div class="tier-band tier-3 sr">
    <div class="tier-header">
      <div class="tier-label-col">
        <span class="tier-num">TIER 03</span>
        <span class="tier-name">Premium<br>AI</span>
        <span class="tier-tag">Intelligence on top. AI that qualifies, knows your business, and creates at scale.</span>
        <span class="tier-badge">PREMIUM</span>
      </div>
      <div class="tier-services-col">
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>AI Lead Qualification</h3>
            <p>An AI system that converses with incoming leads, asks the right questions, scores them based on your criteria, and only surfaces the ones worth your time — so your team closes, not qualifies.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>AI Knowledge Base</h3>
            <p>A custom AI that knows everything about your business — your products, processes, pricing, FAQs — and answers client or staff questions instantly, accurately, 24/7. Your best employee who never sleeps.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
        <div class="svc-item">
          <div class="svc-item-text">
            <h3>AI Content Engine</h3>
            <p>A fully trained content production system built on your brand voice. Feed it a topic or brief — it produces social posts, emails, ads, and copy ready to publish. Volume without the bottleneck.</p>
          </div>
          <span class="svc-item-arr">↗</span>
        </div>
      </div>
    </div>
  </div>

  <div style="height:80px"></div>
</section>

<!-- PROCESS -->
<section id="process" class="process-sec sec">
  <div class="wrap">
    <span class="sec-label sr">How we work</span>
    <h2 class="sec-title sr">No experiments.<br>No wasted cycles.</h2>
    <div class="process-list">
      <div class="p-step sr">
        <span class="p-num jb">01 —</span>
        <div>
          <h3>Diagnostic</h3>
          <p>We assess your operation — workflows, tools, team structure, and volume — and identify exactly where AI generates the highest return. We don't start building until we know precisely what we're solving.</p>
        </div>
        <div class="p-meta">
          <span class="p-tag">DURATION: 2–3 DAYS</span><br>
          Output: a priority map of opportunities ranked by impact. No commitment required after this stage.
        </div>
      </div>
      <div class="p-step sr">
        <span class="p-num jb">02 —</span>
        <div>
          <h3>Architect</h3>
          <p>We design the system — how it works, what it connects to, what it outputs, and how it fits your team's existing habits. You review and approve before we write a line of code.</p>
        </div>
        <div class="p-meta">
          <span class="p-tag">DURATION: 3–5 DAYS</span><br>
          Output: system architecture document, integration plan, and delivery timeline.
        </div>
      </div>
      <div class="p-step sr">
        <span class="p-num jb">03 —</span>
        <div>
          <h3>Build</h3>
          <p>We build. You receive regular progress updates and access to a staging environment throughout. First working version delivered within 14 days for most projects.</p>
        </div>
        <div class="p-meta">
          <span class="p-tag">DURATION: 7–21 DAYS</span><br>
          Output: a functional, tested, documented system. Includes onboarding session and handoff documentation.
        </div>
      </div>
      <div class="p-step sr">
        <span class="p-num jb">04 —</span>
        <div>
          <h3>Deploy &amp; Maintain</h3>
          <p>We go live, monitor performance, and refine based on real usage. Ongoing maintenance and expansion available on monthly retainer for clients that want to keep building.</p>
        </div>
        <div class="p-meta">
          <span class="p-tag">ONGOING</span><br>
          Output: live operational system with monthly performance reviews for retainer clients.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- RESULTS -->
<section id="results" class="results-sec sec" style="padding-top:80px">
  <div class="wrap">
    <span class="sec-label sr">Outcomes</span>
    <h2 class="sec-title sr">The work is measured<br>by what changes.</h2>
    <div class="results-grid sr">
      <div class="r-cell">
        <span class="r-big">60<span class="a">%</span></span>
        <span class="r-lbl">Reduction in manual work hours</span>
      </div>
      <div class="r-cell">
        <span class="r-big">3<span class="a">×</span></span>
        <span class="r-lbl">Output increase, same headcount</span>
      </div>
      <div class="r-cell">
        <span class="r-big">14<span class="a">d</span></span>
        <span class="r-lbl">Average first deployment</span>
      </div>
      <div class="r-cell">
        <span class="r-big">~80<span class="a">%</span></span>
        <span class="r-lbl">Of reporting automated</span>
      </div>
    </div>
    <div class="case-block sr">
      <div>
        <p class="case-q">We had three people handling quotes and follow-ups. After AS4 built the system, one person does it — faster. The other two are now selling full-time.</p>
        <div class="case-who">
          <strong>Owner, construction and building company</strong>
          <span>Small business, Western Cape</span>
        </div>
      </div>
      <div>
        <div class="c-num-row">
          <span class="c-n">3 → 1</span>
          <span class="c-d">People needed for the quoting process</span>
        </div>
        <div class="c-num-row">
          <span class="c-n">2×</span>
          <span class="c-d">Salespeople freed for active selling</span>
        </div>
        <div class="c-num-row">
          <span class="c-n">9 days</span>
          <span class="c-d">Diagnostic to first live system</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing" class="pricing-sec sec">
  <div class="wrap">
    <span class="sec-label sr">Investment</span>
    <h2 class="sec-title sr">Priced in rand.<br>Built for SA conditions.</h2>
    <div class="pricing-grid">
      <div class="pc sr">
        <span class="pc-tier">Tier 1 — Basic</span>
        <span class="pc-price"><span class="cur">R</span>2,500</span>
        <span class="pc-cycle">once-off setup &amp; build</span>
        <div class="pc-retainer">
          <span class="pc-retainer-price">R1,500<em>/month</em></span>
          <span class="pc-retainer-label">Monthly retainer</span>
        </div>
        <p class="pc-desc">Built once, maintained monthly. All 4 Tier 1 systems running automatically — leads, reviews, bookings, and quotes.</p>
        <span class="pc-includes">INCLUDES</span>
        <ul class="pc-feats">
          <li>Access to all 4 Tier 1 systems</li>
          <li>Initial build and setup included</li>
          <li>Integration with your existing tools</li>
          <li>Documentation &amp; onboarding session</li>
          <li>Ongoing monitoring and maintenance</li>
          <li>Monthly performance check-in</li>
        </ul>
        <a href="#contact" class="btn-tier btn-tier-ghost">Start here</a>
      </div>
      <div class="pc hot sr">
        <span class="pc-tier">Tier 2 — Higher Value</span>
        <span class="pc-price"><span class="cur">R</span>4,500</span>
        <span class="pc-cycle">once-off setup &amp; build</span>
        <div class="pc-retainer">
          <span class="pc-retainer-price">R2,500<em>/month</em></span>
          <span class="pc-retainer-label">Monthly retainer</span>
        </div>
        <p class="pc-desc">Built once, maintained monthly. Client onboarding, employee onboarding, and proposal automation — running without you in the middle.</p>
        <span class="pc-includes">INCLUDES</span>
        <ul class="pc-feats">
          <li>Access to all Tier 2 systems</li>
          <li>Includes everything in Tier 1</li>
          <li>Initial build and setup included</li>
          <li>Unlimited integrations</li>
          <li>Priority build queue</li>
          <li>Dedicated account contact</li>
          <li>Quarterly strategy session</li>
        </ul>
        <a href="#contact" class="btn-tier btn-tier-gold">Get started</a>
      </div>
      <div class="pc sr">
        <span class="pc-tier">Tier 3 — Premium AI</span>
        <span class="pc-price">Custom</span>
        <span class="pc-cycle">once-off setup &amp; build</span>
        <div class="pc-retainer">
          <span class="pc-retainer-price">TBD<em>/month</em></span>
          <span class="pc-retainer-label">Monthly retainer</span>
        </div>
        <p class="pc-desc">Scoped to your operation. AI lead qualification, a knowledge base trained on your business, or a full AI content engine — custom built.</p>
        <span class="pc-includes">INCLUDES</span>
        <ul class="pc-feats">
          <li>Full AI system design &amp; build</li>
          <li>Custom training on your business data</li>
          <li>Integration with existing workflows</li>
          <li>Ongoing refinement retainer available</li>
          <li>Direct access to build team</li>
        </ul>
        <a href="#contact" class="btn-tier btn-tier-ghost">Request a scope</a>
      </div>
    </div>
    <p class="rand-note">All pricing in <span>South African Rand (ZAR)</span>. No dollar invoices. No hidden costs.</p>
  </div>
</section>

<!-- CTA -->
<section id="contact" class="cta-sec">
  <div class="wrap">
    <div class="cta-in sr">
      <div>
        <span class="cta-chip">Ready to build</span>
        <h2>Your competitors are already automating. Be the one that's ahead.</h2>
        <p>Tell us what you're working with. We'll tell you what's possible and what it costs. No pitch. No pressure.</p>
      </div>
      <div>
        <a href="mailto:build@as4.co.za" class="btn-primary" style="font-size:15px;padding:16px 34px">Talk to us →</a>
        <p class="cta-sub">George, Western Cape · Responds within 24 hours</p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="wrap">
    <div class="ft">
      <div class="ft-brand">
        <a href="#" class="logo"><span>AS</span><span class="logo-4">4</span></a>
        <p>AI Systems For South African Businesses. Built in George. Priced in rand. Designed for how SA businesses actually operate.</p>
        <p class="ft-loc">📍 George, Western Cape, South Africa</p>
      </div>
      <div class="ft-col">
        <h4>Tier 1 — Basic</h4>
        <ul>
          <li><a href="#">Lead Capture &amp; Notification</a></li>
          <li><a href="#">Review Request Automation</a></li>
          <li><a href="#">Appointment Reminders</a></li>
          <li><a href="#">Quote Request System</a></li>
        </ul>
      </div>
      <div class="ft-col">
        <h4>Tier 2 &amp; 3</h4>
        <ul>
          <li><a href="#">Client Onboarding</a></li>
          <li><a href="#">Proposal Automation</a></li>
          <li><a href="#">AI Lead Qualification</a></li>
          <li><a href="#">AI Knowledge Base</a></li>
          <li><a href="#">AI Content Engine</a></li>
        </ul>
      </div>
      <div class="ft-col">
        <h4>Contact</h4>
        <ul>
          <li><a href="mailto:build@as4.co.za">build@as4.co.za</a></li>
          <li><a href="#">WhatsApp</a></li>
          <li><a href="#">LinkedIn</a></li>
          <li><a href="#">Instagram</a></li>
        </ul>
      </div>
    </div>
    <div class="ft-bot">
      <p>© 2026 AS4. All rights reserved.</p>
      <a href="#">A division of <span>The Large Scale Agency</span></a>
    </div>
  </div>
</footer>

<script>
// Scroll reveal
const obs = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('in'), i * 60);
      obs.unobserve(e.target);
    }
  });
}, { threshold: 0.07 });
document.querySelectorAll('.sr').forEach(el => obs.observe(el));

// Smooth scroll
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', function(e) {
    const t = document.querySelector(this.getAttribute('href'));
    if (t) { e.preventDefault(); window.scrollTo({ top: t.getBoundingClientRect().top + window.scrollY - 72, behavior: 'smooth' }); }
  });
});
</script>
</body>
</html>
