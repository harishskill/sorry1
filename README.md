<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>For Mahigill 💌</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --rose:#E8587A;--rose-d:#b8354f;--blush:#FDE8EE;--cream:#FFF7F9;
  --deep:#1a0a10;--muted:#8C5A6C;--gold:#d4a843;
}
html{scroll-behavior:smooth}
body{background:#0d0007;color:#fff;font-family:'Inter',sans-serif;overflow-x:hidden;cursor:default}

/* ═══ LOCK SCREEN ═══ */
#lock{
  position:fixed;inset:0;z-index:1000;
  background:#0d0007;
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  transition:opacity 1.2s ease;
}
#lock.fade{opacity:0;pointer-events:none}

.lock-icon{font-size:3rem;margin-bottom:1.5rem;animation:lockPulse 2s ease-in-out infinite}
@keyframes lockPulse{0%,100%{transform:scale(1);opacity:1}50%{transform:scale(1.1);opacity:0.7}}

.lock-title{
  font-family:'Playfair Display',serif;font-size:clamp(1.4rem,5vw,2.2rem);
  color:#fff;font-style:italic;text-align:center;margin-bottom:0.5rem;
  letter-spacing:0.02em;
}
.lock-sub{
  font-size:0.8rem;letter-spacing:0.22em;text-transform:uppercase;
  color:rgba(255,255,255,0.35);margin-bottom:3rem;
}
.lock-hint{
  font-size:0.78rem;color:rgba(255,255,255,0.3);letter-spacing:0.12em;
  text-transform:uppercase;animation:blink 1.8s ease-in-out infinite;
}
@keyframes blink{0%,100%{opacity:0.3}50%{opacity:1}}

.tap-btn{
  margin-top:2.5rem;
  background:none;border:1px solid rgba(232,88,122,0.5);
  color:var(--rose);font-size:0.85rem;letter-spacing:0.2em;text-transform:uppercase;
  padding:0.9rem 2.5rem;border-radius:2px;cursor:pointer;
  transition:all 0.3s ease;
}
.tap-btn:hover{background:rgba(232,88,122,0.12);border-color:var(--rose);transform:scale(1.03)}

/* ═══ BACKGROUND STARS ═══ */
#stars{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden}
.star{
  position:absolute;background:#fff;border-radius:50%;
  animation:twinkle linear infinite;
}
@keyframes twinkle{
  0%,100%{opacity:0.1;transform:scale(1)}
  50%{opacity:0.8;transform:scale(1.4)}
}

/* ═══ PETALS ═══ */
#petals{position:fixed;inset:0;pointer-events:none;z-index:1;overflow:hidden;opacity:0;transition:opacity 2s}
#petals.show{opacity:1}
.petal{position:absolute;top:-40px;animation:fallPetal linear infinite;font-size:1.1rem}
@keyframes fallPetal{to{transform:translateY(110vh) rotate(720deg)}}

/* ═══ MAIN CONTENT ═══ */
main{position:relative;z-index:2;opacity:0;transition:opacity 1.5s ease;pointer-events:none}
main.show{opacity:1;pointer-events:all}

/* ═══ CHAPTER SYSTEM ═══ */
.chapter{
  min-height:100vh;display:flex;flex-direction:column;
  align-items:center;justify-content:center;
  padding:4rem 1.5rem;text-align:center;
  opacity:0;transform:translateY(30px);
  transition:opacity 0.9s ease,transform 0.9s ease;
}
.chapter.visible{opacity:1;transform:translateY(0)}

/* ═══ CHAPTER 1 – CONFESSION ═══ */
.ch1-eyebrow{
  font-size:0.72rem;letter-spacing:0.3em;text-transform:uppercase;
  color:rgba(255,255,255,0.3);margin-bottom:2.5rem;
}
.ch1-number{
  font-family:'Playfair Display',serif;
  font-size:clamp(5rem,20vw,12rem);font-weight:700;font-style:italic;
  color:transparent;
  -webkit-text-stroke:1px rgba(232,88,122,0.4);
  line-height:1;margin-bottom:-1.5rem;
  animation:numFloat 4s ease-in-out infinite;
}
@keyframes numFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-12px)}}
.ch1-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(1.8rem,6vw,3.5rem);
  color:#fff;line-height:1.2;
  animation:revealText 0.8s ease both;
}
.ch1-title em{color:var(--rose);font-style:italic}
.ch1-divider{
  width:60px;height:1px;background:linear-gradient(90deg,transparent,var(--rose),transparent);
  margin:2rem auto;
}
.ch1-body{
  font-size:clamp(1rem,2.5vw,1.15rem);font-weight:300;color:rgba(255,255,255,0.6);
  max-width:520px;line-height:1.9;
}
.ch1-scroll{
  margin-top:3rem;font-size:0.7rem;letter-spacing:0.25em;text-transform:uppercase;
  color:rgba(255,255,255,0.2);animation:scrollBounce 2s ease-in-out infinite;
}
@keyframes scrollBounce{0%,100%{transform:translateY(0)}50%{transform:translateY(8px)}}

/* ═══ CHAPTER 2 – WHY ═══ */
.ch2-label{
  font-size:0.7rem;letter-spacing:0.3em;text-transform:uppercase;
  color:var(--rose);margin-bottom:2rem;
}
.ch2-title{
  font-family:'Playfair Display',serif;font-size:clamp(1.5rem,5vw,2.8rem);
  color:#fff;margin-bottom:3rem;line-height:1.3;
}
.ch2-title span{color:var(--rose);font-style:italic}

.reasons{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1.2rem;max-width:760px;width:100%}
.reason-card{
  background:rgba(232,88,122,0.06);border:1px solid rgba(232,88,122,0.15);
  border-radius:4px;padding:1.8rem 1.5rem;text-align:left;
  transition:all 0.3s ease;
  opacity:0;transform:translateY(20px);
}
.reason-card.pop{opacity:1;transform:translateY(0)}
.reason-card:hover{background:rgba(232,88,122,0.12);border-color:rgba(232,88,122,0.4);transform:translateY(-4px)}
.reason-icon{font-size:1.6rem;margin-bottom:0.8rem}
.reason-title{font-size:0.95rem;font-weight:500;color:#fff;margin-bottom:0.5rem}
.reason-text{font-size:0.85rem;color:rgba(255,255,255,0.45);line-height:1.7;font-weight:300}

/* ═══ CHAPTER 3 – THE LETTER (reveal) ═══ */
.ch3-label{font-size:0.7rem;letter-spacing:0.3em;text-transform:uppercase;color:var(--rose);margin-bottom:1.5rem}
.envelope-wrap{perspective:1000px;cursor:pointer;margin:2rem 0}
.envelope{
  width:320px;height:210px;position:relative;transform-style:preserve-3d;
  transition:transform 1.2s cubic-bezier(0.4,0,0.2,1);
}
.envelope.open{transform:rotateX(180deg)}
.env-face,.env-back{
  position:absolute;inset:0;border-radius:4px;
  backface-visibility:hidden;display:flex;align-items:center;justify-content:center;
}
.env-face{
  background:linear-gradient(135deg,#2a1018,#1a0810);
  border:1px solid rgba(232,88,122,0.3);flex-direction:column;
}
.env-back{
  background:var(--rose);
  transform:rotateX(180deg);flex-direction:column;
}
.env-wax{
  width:56px;height:56px;border-radius:50%;
  background:var(--rose-d);
  display:flex;align-items:center;justify-content:center;
  font-size:1.4rem;margin-bottom:0.8rem;
  box-shadow:0 0 20px rgba(232,88,122,0.4);
  animation:waxGlow 2.5s ease-in-out infinite;
}
@keyframes waxGlow{0%,100%{box-shadow:0 0 20px rgba(232,88,122,0.4)}50%{box-shadow:0 0 35px rgba(232,88,122,0.7)}}
.env-text{font-size:0.78rem;letter-spacing:0.2em;text-transform:uppercase;color:rgba(255,255,255,0.4)}
.env-hint{font-size:0.75rem;color:rgba(255,255,255,0.6);letter-spacing:0.15em;text-transform:uppercase;margin-top:0.5rem}

.letter-reveal{
  max-width:640px;width:100%;
  background:linear-gradient(145deg,#1c0a12,#150710);
  border:1px solid rgba(232,88,122,0.2);border-radius:4px;
  padding:3rem 2.5rem 3.5rem;text-align:left;
  overflow:hidden;max-height:0;transition:max-height 1.5s cubic-bezier(0.4,0,0.2,1),opacity 0.8s ease,padding 0.6s ease;
  opacity:0;padding-top:0;padding-bottom:0;
}
.letter-reveal.open{max-height:2000px;opacity:1;padding:3rem 2.5rem 3.5rem}
.letter-date{font-size:0.72rem;letter-spacing:0.18em;text-transform:uppercase;color:rgba(255,255,255,0.25);margin-bottom:2rem}
.letter-greeting{font-family:'Playfair Display',serif;font-size:1.6rem;font-style:italic;color:var(--rose);margin-bottom:1.5rem}
.letter-body p{font-size:1rem;line-height:1.95;color:rgba(255,255,255,0.65);margin-bottom:1.2rem;font-weight:300}
.letter-sign{margin-top:2.5rem;font-family:'Playfair Display',serif;font-size:1.3rem;font-style:italic;color:#fff}
.letter-sign small{display:block;font-family:'Inter',sans-serif;font-style:normal;font-size:0.72rem;letter-spacing:0.18em;text-transform:uppercase;color:rgba(255,255,255,0.3);margin-top:0.4rem}

/* ═══ CHAPTER 4 – PROMISES ═══ */
.ch4-label{font-size:0.7rem;letter-spacing:0.3em;text-transform:uppercase;color:var(--rose);margin-bottom:1.5rem}
.ch4-title{font-family:'Playfair Display',serif;font-size:clamp(1.5rem,5vw,2.8rem);color:#fff;margin-bottom:0.6rem;line-height:1.3}
.ch4-title em{color:var(--rose);font-style:italic}
.ch4-sub{font-size:0.78rem;letter-spacing:0.15em;text-transform:uppercase;color:rgba(255,255,255,0.25);margin-bottom:3rem}
.promise-list{max-width:600px;width:100%}
.promise-item{
  display:flex;align-items:flex-start;gap:1.2rem;
  padding:1.2rem 0;border-bottom:1px solid rgba(255,255,255,0.06);
  opacity:0;transform:translateX(-20px);transition:all 0.6s ease;
}
.promise-item.pop{opacity:1;transform:translateX(0)}
.promise-num{
  font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;
  color:transparent;-webkit-text-stroke:1px rgba(232,88,122,0.35);
  line-height:1;min-width:2.5rem;
}
.promise-content{}
.promise-title{font-size:1rem;font-weight:500;color:#fff;margin-bottom:0.35rem}
.promise-text{font-size:0.88rem;color:rgba(255,255,255,0.4);line-height:1.7;font-weight:300}

/* ═══ CHAPTER 5 – THE MOMENT ═══ */
.ch5-pre{font-size:0.7rem;letter-spacing:0.3em;text-transform:uppercase;color:rgba(255,255,255,0.25);margin-bottom:1.5rem}
.ch5-q{
  font-family:'Playfair Display',serif;font-size:clamp(1.8rem,6vw,3.2rem);
  color:#fff;line-height:1.25;margin-bottom:1rem;
}
.ch5-q em{color:var(--rose)}
.ch5-sub{font-size:0.9rem;color:rgba(255,255,255,0.35);margin-bottom:3.5rem;font-weight:300}

.choice-wrap{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap}
.btn-yes{
  background:var(--rose);color:#fff;
  font-family:'Inter',sans-serif;font-size:0.9rem;letter-spacing:0.18em;text-transform:uppercase;
  border:none;padding:1.1rem 3rem;border-radius:2px;cursor:pointer;
  transition:all 0.25s ease;box-shadow:0 0 30px rgba(232,88,122,0.3);
}
.btn-yes:hover{background:var(--rose-d);transform:scale(1.05);box-shadow:0 0 50px rgba(232,88,122,0.55)}
.btn-maybe{
  background:transparent;color:rgba(255,255,255,0.4);
  font-family:'Inter',sans-serif;font-size:0.9rem;letter-spacing:0.18em;text-transform:uppercase;
  border:1px solid rgba(255,255,255,0.12);padding:1.1rem 2rem;border-radius:2px;cursor:pointer;
  transition:all 0.25s ease;position:relative;
}
.btn-maybe:hover{
  border-color:rgba(255,255,255,0.3);color:rgba(255,255,255,0.7);
}
/* The "Not yet" button runs away */
.btn-maybe.running{transition:transform 0.15s ease}

/* ═══ CELEBRATION ═══ */
#celebration{
  position:fixed;inset:0;z-index:500;
  background:rgba(13,0,7,0.97);
  display:none;flex-direction:column;align-items:center;justify-content:center;text-align:center;
  padding:2rem;
}
#celebration.show{display:flex}
.celeb-hearts{font-size:4rem;margin-bottom:1.5rem;animation:heartbeat 1.2s ease-in-out infinite}
@keyframes heartbeat{0%,100%{transform:scale(1)}14%{transform:scale(1.3)}28%{transform:scale(1)}42%{transform:scale(1.2)}70%{transform:scale(1)}}
.celeb-title{font-family:'Playfair Display',serif;font-size:clamp(2rem,8vw,4.5rem);color:var(--rose);margin-bottom:1rem;animation:fadeUp 0.7s 0.2s ease both}
.celeb-body{font-size:1.05rem;color:rgba(255,255,255,0.6);max-width:420px;line-height:1.9;font-weight:300;animation:fadeUp 0.7s 0.4s ease both}
.celeb-line{width:80px;height:1px;background:linear-gradient(90deg,transparent,var(--rose),transparent);margin:1.5rem auto;animation:fadeUp 0.7s 0.6s ease both}

@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
@keyframes revealText{from{opacity:0;letter-spacing:0.3em}to{opacity:1;letter-spacing:normal}}

/* RED LINE PROGRESSION */
.progress-line{
  position:fixed;top:0;left:0;height:2px;background:var(--rose);
  width:0%;z-index:100;transition:width 0.4s ease;
  box-shadow:0 0 8px var(--rose);
}

/* chapter markers */
.chapter-markers{
  position:fixed;right:1.5rem;top:50%;transform:translateY(-50%);
  z-index:100;display:flex;flex-direction:column;gap:0.6rem;
}
.c-dot{
  width:6px;height:6px;border-radius:50%;background:rgba(255,255,255,0.15);
  transition:all 0.3s ease;cursor:pointer;
}
.c-dot.active{background:var(--rose);box-shadow:0 0 8px var(--rose)}

@media(max-width:600px){
  .envelope{width:260px;height:172px}
  .letter-reveal{padding:2rem 1.5rem 2.5rem}
  .letter-reveal.open{padding:2rem 1.5rem 2.5rem}
  .chapter-markers{display:none}
}
</style>
</head>
<body>

<!-- LOCK SCREEN -->
<div id="lock">
  <div class="lock-icon">🔒</div>
  <h1 class="lock-title">This message is for<br><em style="color:var(--rose)">Mahigill</em> only.</h1>
  <p class="lock-sub">Private &nbsp;·&nbsp; Confidential &nbsp;·&nbsp; From the heart</p>
  <p class="lock-hint">Are you her?</p>
  <button class="tap-btn" onclick="unlockSite()">Yes, I'm Mahigill 💌</button>
</div>

<!-- STARS BACKGROUND -->
<div id="stars"></div>

<!-- PETALS -->
<div id="petals"></div>

<!-- PROGRESS LINE -->
<div class="progress-line" id="progress"></div>

<!-- CHAPTER DOTS -->
<div class="chapter-markers" id="dots"></div>

<!-- MAIN -->
<main id="main">

  <!-- CH1: OPENING -->
  <section class="chapter" id="ch1" data-chapter="0">
    <p class="ch1-eyebrow">Chapter I &nbsp;·&nbsp; A confession</p>
    <div class="ch1-number">01</div>
    <h1 class="ch1-title">I did something<br><em>I deeply regret.</em></h1>
    <div class="ch1-divider"></div>
    <p class="ch1-body">Before you close this tab — give me just five minutes.<br>Not to make excuses. But to tell you the truth.</p>
    <p class="ch1-scroll">↓ &nbsp; scroll to uncover &nbsp; ↓</p>
  </section>

  <!-- CH2: WHY YOU MATTER -->
  <section class="chapter" id="ch2" data-chapter="1">
    <p class="ch2-label">Chapter II &nbsp;·&nbsp; Why this hurts so much</p>
    <h2 class="ch2-title">Because <span>Mahigill</span>,<br>you mean everything.</h2>
    <div class="reasons">
      <div class="reason-card" style="transition-delay:0.0s">
        <div class="reason-icon">🌙</div>
        <div class="reason-title">You're my calm</div>
        <div class="reason-text">In every storm, your presence is the only thing that makes sense to me.</div>
      </div>
      <div class="reason-card" style="transition-delay:0.15s">
        <div class="reason-icon">🔥</div>
        <div class="reason-title">You push me</div>
        <div class="reason-text">You make me want to be a better version of myself every single day.</div>
      </div>
      <div class="reason-card" style="transition-delay:0.3s">
        <div class="reason-icon">💎</div>
        <div class="reason-title">You're rare</div>
        <div class="reason-text">I've never met anyone who loves as fiercely and cares as deeply as you do.</div>
      </div>
    </div>
  </section>

  <!-- CH3: THE LETTER -->
  <section class="chapter" id="ch3" data-chapter="2">
    <p class="ch3-label">Chapter III &nbsp;·&nbsp; The letter I wrote for you</p>
    <p style="font-size:0.85rem;color:rgba(255,255,255,0.3);margin-bottom:2rem;font-weight:300">Tap the envelope to open it.</p>
    <div class="envelope-wrap">
      <div class="envelope" id="envelope" onclick="openEnvelope()">
        <div class="env-face">
          <div class="env-wax">💌</div>
          <div class="env-text">Sealed with love</div>
          <div class="env-hint">tap to open</div>
        </div>
        <div class="env-back">
          <div style="font-family:'Playfair Display',serif;font-size:1.3rem;font-style:italic;color:#fff">Opening…</div>
        </div>
      </div>
    </div>

    <div class="letter-reveal" id="letter">
      <p class="letter-date">June 2026 &nbsp;·&nbsp; Written with love & regret</p>
      <p class="letter-greeting">My dearest Mahigill,</p>
      <div class="letter-body">
        <p>There are moments when you realize, too late, that you've let something precious slip. This is one of those moments — and it's entirely my fault.</p>
        <p>I hurt you. And I won't dress it up with excuses, because you deserve better than that. You deserve honesty. So here it is: I was wrong. Fully. Without qualification.</p>
        <p>Every laugh we've shared, every quiet moment, every ridiculous inside joke — they replay in my head and remind me how lucky I am just to exist in your world. The idea of losing that because of my own carelessness is something I can't sit with.</p>
        <p>You didn't just make my days brighter. You made them make sense. And I took that for granted for even a second longer than I should have.</p>
        <p>This isn't just a sorry on a webpage. This is me promising — out loud, in writing, permanently — that I will earn back your trust one day at a time, starting right now.</p>
        <p>I love you more than these words can hold.</p>
      </div>
      <div class="letter-sign">
        Yours, always 🌹
        <small>with every piece of me</small>
      </div>
    </div>
  </section>

  <!-- CH4: PROMISES -->
  <section class="chapter" id="ch4" data-chapter="3">
    <p class="ch4-label">Chapter IV &nbsp;·&nbsp; What I promise you</p>
    <h2 class="ch4-title">Not words.<br><em>A commitment.</em></h2>
    <p class="ch4-sub">Written. Sealed. Non-negotiable.</p>
    <div class="promise-list">
      <div class="promise-item" style="transition-delay:0s">
        <div class="promise-num">I</div>
        <div class="promise-content">
          <div class="promise-title">I will listen before I speak</div>
          <div class="promise-text">Your feelings will always come before my reflexes. I'll breathe, then respond.</div>
        </div>
      </div>
      <div class="promise-item" style="transition-delay:0.12s">
        <div class="promise-num">II</div>
        <div class="promise-content">
          <div class="promise-title">I will choose you, every time</div>
          <div class="promise-text">No ego, no stubbornness, no pride will ever outweigh you. Not again.</div>
        </div>
      </div>
      <div class="promise-item" style="transition-delay:0.24s">
        <div class="promise-num">III</div>
        <div class="promise-content">
          <div class="promise-title">I will protect your peace</div>
          <div class="promise-text">I never want to be the reason your day is harder. I'll be your shelter, not your storm.</div>
        </div>
      </div>
      <div class="promise-item" style="transition-delay:0.36s">
        <div class="promise-num">IV</div>
        <div class="promise-content">
          <div class="promise-title">I will show up, not just say so</div>
          <div class="promise-text">Actions. Not promises. Not texts. Real, tangible proof — every single day.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- CH5: THE DECISION -->
  <section class="chapter" id="ch5" data-chapter="4">
    <p class="ch5-pre">The final chapter</p>
    <h2 class="ch5-q">So, <em>Mahigill</em>…<br>what do you say?</h2>
    <p class="ch5-sub">Only when you're truly ready. No rush. No pressure.</p>
    <div class="choice-wrap">
      <button class="btn-yes" onclick="celebrate()">I forgive you 💕</button>
      <button class="btn-maybe" id="noBtn" onmouseenter="runAway(this)" ontouchstart="runAway(this)">Not yet 😶</button>
    </div>
  </section>

</main>

<!-- CELEBRATION -->
<div id="celebration">
  <div class="celeb-hearts">💖</div>
  <h2 class="celeb-title">She said yes!!</h2>
  <div class="celeb-line"></div>
  <p class="celeb-body">Mahigill, you just made me the happiest person alive. I promise to spend every day proving you made the right choice. I love you so, so much. 🌹</p>
  <button onclick="document.getElementById('celebration').classList.remove('show')" style="margin-top:2.5rem;background:none;border:1px solid rgba(255,255,255,0.15);color:rgba(255,255,255,0.4);font-size:0.75rem;letter-spacing:0.18em;text-transform:uppercase;padding:0.7rem 1.8rem;border-radius:2px;cursor:pointer">
    Close
  </button>
</div>

<script>
// ── STARS ──
const starEl = document.getElementById('stars');
for(let i=0;i<120;i++){
  const s=document.createElement('div');
  s.classList.add('star');
  const sz=0.5+Math.random()*1.8;
  s.style.cssText=`width:${sz}px;height:${sz}px;left:${Math.random()*100}%;top:${Math.random()*100}%;animation-duration:${2+Math.random()*4}s;animation-delay:${Math.random()*5}s`;
  starEl.appendChild(s);
}

// ── PETALS ──
const petalEl=document.getElementById('petals');
const petalEmojis=['🌸','🌺','💗','✨','🌷'];
function spawnPetals(n){
  for(let i=0;i<n;i++){
    const p=document.createElement('span');
    p.classList.add('petal');
    p.textContent=petalEmojis[Math.floor(Math.random()*petalEmojis.length)];
    p.style.left=Math.random()*100+'vw';
    p.style.fontSize=(0.8+Math.random()*1)+'rem';
    p.style.animationDuration=(8+Math.random()*10)+'s';
    p.style.animationDelay=(Math.random()*10)+'s';
    petalEl.appendChild(p);
  }
}
spawnPetals(30);

// ── UNLOCK ──
function unlockSite(){
  document.getElementById('lock').classList.add('fade');
  setTimeout(()=>{
    document.getElementById('lock').style.display='none';
    document.getElementById('main').classList.add('show');
    petalEl.classList.add('show');
  },1200);
}

// ── CHAPTER DOTS ──
const chapters=document.querySelectorAll('.chapter');
const dotsWrap=document.getElementById('dots');
chapters.forEach((_,i)=>{
  const d=document.createElement('div');
  d.classList.add('c-dot');
  d.setAttribute('title','Chapter '+(i+1));
  d.onclick=()=>chapters[i].scrollIntoView({behavior:'smooth'});
  dotsWrap.appendChild(d);
});
const allDots=document.querySelectorAll('.c-dot');

// ── INTERSECTION OBSERVER ──
let currentChapter=0;
const obs=new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add('visible');
      const idx=parseInt(entry.target.dataset.chapter);
      currentChapter=idx;
      allDots.forEach((d,i)=>d.classList.toggle('active',i===idx));
      document.getElementById('progress').style.width=((idx+1)/chapters.length*100)+'%';
      // stagger children
      if(idx===1){
        document.querySelectorAll('.reason-card').forEach((c,i)=>{
          setTimeout(()=>c.classList.add('pop'),i*150+200);
        });
      }
      if(idx===3){
        document.querySelectorAll('.promise-item').forEach((p,i)=>{
          setTimeout(()=>p.classList.add('pop'),i*130+200);
        });
      }
    }
  });
},{threshold:0.35});
chapters.forEach(c=>obs.observe(c));

// ── ENVELOPE ──
let envelopeOpen=false;
function openEnvelope(){
  if(envelopeOpen)return;
  envelopeOpen=true;
  document.getElementById('envelope').classList.add('open');
  setTimeout(()=>{
    document.getElementById('letter').classList.add('open');
  },800);
}

// ── RUNAWAY BUTTON ──
let runCount=0;
function runAway(btn){
  runCount++;
  if(runCount>5){
    btn.textContent='Fine… okay 💕';
    btn.onclick=celebrate;
    btn.style.color='var(--rose)';
    btn.style.borderColor='var(--rose)';
    return;
  }
  const rect=btn.getBoundingClientRect();
  const maxX=window.innerWidth-rect.width-20;
  const maxY=window.innerHeight-rect.height-20;
  const nx=Math.max(10,Math.random()*maxX);
  const ny=Math.max(10,Math.random()*maxY);
  btn.style.position='fixed';
  btn.style.left=nx+'px';
  btn.style.top=ny+'px';
  btn.style.zIndex='200';
  btn.style.margin='0';
}

// ── CELEBRATE ──
function celebrate(){
  const cel=document.getElementById('celebration');
  cel.classList.add('show');
  spawnPetals(20);
  setTimeout(()=>spawnPetals(20),1000);
}
</script>
</body>
</html>
