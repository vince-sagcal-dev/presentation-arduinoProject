<script setup lang="ts">
import { ref } from 'vue'

const demoCount = ref(0)

useHead({
  title: 'Mini Conveyor Belt Object Counter',
  meta: [
    {
      name: 'description',
      content: 'A project presentation for an Arduino-powered mini conveyor belt object counter.'
    }
  ]
})
</script>

<template>
  <main>
    <header class="site-header">
      <a class="brand" href="#top" aria-label="Mini Counter home">
        <span class="brand-mark" aria-hidden="true">
          <svg viewBox="0 0 32 32" fill="none">
            <path d="M5 10.5h22M5 21.5h22M8 10.5v11m16-11v11" />
            <circle cx="8" cy="16" r="2" />
            <circle cx="24" cy="16" r="2" />
            <path d="M12 16h7" />
          </svg>
        </span>
        <span>MINI<span class="brand-light">COUNTER</span></span>
      </a>
      <nav class="main-nav" aria-label="Main navigation">
        <a href="#system">The system</a>
        <a href="#build">The build</a>
        <a href="#testing">Testing</a>
        <a href="#next">Next steps</a>
      </nav>
      <a class="header-cta" href="#how-it-works">Explore the project <span aria-hidden="true">↘</span></a>
    </header>

    <section id="top" class="hero">
      <div class="hero-copy">
        <div class="eyebrow eyebrow-light"><span class="status-dot" /> Arduino prototype <span class="eyebrow-separator">/</span> Project presentation</div>
        <h1>A small belt.<br>A smarter count<span class="accent-period">.</span></h1>
        <p class="hero-lede">An Arduino-powered conveyor that detects passing objects and keeps a live total on an LCD.</p>
        <div class="hero-actions">
          <a class="button button-lime" href="#how-it-works">See how it works <span aria-hidden="true">↓</span></a>
          <span class="hero-note">A tabletop proof of an industrial idea.</span>
        </div>
        <div class="hero-facts">
          <div><span class="fact-number">01</span><span>Move</span></div>
          <div><span class="fact-number">02</span><span>Detect</span></div>
          <div><span class="fact-number">03</span><span>Count</span></div>
          <div><span class="fact-number">04</span><span>Display</span></div>
        </div>
      </div>
      <div class="hero-art" aria-label="Illustration of the mini conveyor prototype with an Arduino, sensor, and LCD">
        <div class="art-topline"><span>FIG. 01</span><span>THE COUNTING LOOP</span></div>
        <svg class="machine-illustration" viewBox="0 0 700 470" role="img" aria-labelledby="machine-title machine-desc">
          <title id="machine-title">Mini conveyor belt object counter</title>
          <desc id="machine-desc">A cardboard conveyor carries a sample object past an infrared sensor. An Arduino processes the detection and an LCD shows the count.</desc>
          <defs>
            <pattern id="grid" width="28" height="28" patternUnits="userSpaceOnUse">
              <path d="M28 0H0V28" fill="none" stroke="#d8e1d8" stroke-width="1" />
            </pattern>
            <linearGradient id="belt" x1="0" x2="1" y1="0" y2="1">
              <stop offset="0" stop-color="#335b50" />
              <stop offset="1" stop-color="#193b34" />
            </linearGradient>
            <linearGradient id="box" x1="0" x2="1" y1="0" y2="1">
              <stop offset="0" stop-color="#ffd17c" />
              <stop offset="1" stop-color="#f0a94e" />
            </linearGradient>
          </defs>
          <rect x="1" y="1" width="698" height="468" rx="18" fill="#eef3ed" />
          <rect x="1" y="1" width="698" height="468" rx="18" fill="url(#grid)" />
          <path d="M70 340 350 214l284 123-278 132L70 340Z" fill="#d2dacf" />
          <path d="m105 327 245-109 245 106-241 113-249-110Z" fill="url(#belt)" stroke="#17352f" stroke-width="3" />
          <path d="m137 327 216-96 211 91-212 98-215-93Z" fill="none" stroke="#789187" stroke-width="2" stroke-dasharray="7 9" />
          <path d="m130 357 4 57m72-24 2 58m317-166-3 59m-73 32-2 59" stroke="#435a52" stroke-width="8" stroke-linecap="round" />
          <path d="m91 348 16-8m488 105 27-13" stroke="#263f38" stroke-width="11" stroke-linecap="round" />
          <ellipse cx="359" cy="299" rx="40" ry="18" fill="#132f29" opacity=".22" />
          <path d="m328 261 39-19 42 19-40 20-41-20Z" fill="#ffe1a3" />
          <path d="m328 261 41 20v45l-41-20v-45Z" fill="#efb95e" />
          <path d="m369 281 40-20v45l-40 20v-45Z" fill="url(#box)" />
          <path d="m369 281 40-20" stroke="#fff1d2" stroke-width="2" />
          <g transform="translate(458 143)">
            <path d="M0 0h66v15H0z" rx="4" fill="#263e38" />
            <path d="M9 15h48v40H9z" fill="#8ea49a" />
            <path d="M16 20h34v27H16z" fill="#fbfcf4" />
            <path d="M20 33h11m6 0h8M20 39h21" stroke="#31594e" stroke-width="2" stroke-linecap="round" />
            <circle cx="33" cy="8" r="2.5" fill="#b9ee71" />
          </g>
          <path d="m490 201-39 47" stroke="#6b887b" stroke-width="1.5" stroke-dasharray="4 5" />
          <g transform="translate(208 347)">
            <path d="M0 0h101l-3 45H4L0 0Z" fill="#315da7" stroke="#21437e" stroke-width="2" />
            <path d="m11 9 2 26m12-26 2 26m12-26 2 26m12-26 2 26m12-26 2 26" stroke="#8eb2e8" stroke-width="2" />
            <rect x="66" y="13" width="19" height="13" rx="2" fill="#d8e5f7" />
            <circle cx="77" cy="31" r="3" fill="#f3bd56" />
          </g>
          <g transform="translate(444 235)">
            <path d="M0 0v42" stroke="#e78b45" stroke-width="5" />
            <path d="M-12 42h24l-4 18h-16l-4-18Z" fill="#e78b45" stroke="#bb6730" stroke-width="2" />
            <circle cx="0" cy="53" r="3" fill="#fff3dc" />
          </g>
          <path d="M443 292 423 309" stroke="#e78b45" stroke-width="2" stroke-dasharray="3 4" />
          <g class="diagram-label" transform="translate(525 116)">
            <rect width="126" height="31" rx="15.5" fill="#fff" />
            <circle cx="14" cy="15.5" r="4" fill="#e78b45" />
            <text x="26" y="20">16×2 LCD</text>
          </g>
          <g class="diagram-label" transform="translate(490 306)">
            <rect width="141" height="31" rx="15.5" fill="#fff" />
            <circle cx="14" cy="15.5" r="4" fill="#e78b45" />
            <text x="26" y="20">IR sensor</text>
          </g>
          <g class="diagram-label" transform="translate(138 404)">
            <rect width="154" height="31" rx="15.5" fill="#fff" />
            <circle cx="14" cy="15.5" r="4" fill="#315da7" />
            <text x="26" y="20">Arduino Uno</text>
          </g>
          <path d="M44 76h35m-35 9h20" stroke="#94a69a" stroke-width="2" stroke-linecap="round" />
          <text x="44" y="64" class="art-small">OBJECT IN MOTION</text>
          <path d="m75 89 17 10" stroke="#94a69a" stroke-width="1.5" />
          <path d="M548 389h74" stroke="#94a69a" stroke-width="2" stroke-linecap="round" />
          <text x="548" y="380" class="art-small">MADE TO TEST</text>
        </svg>
        <div class="art-caption"><span>01 — SYSTEM OVERVIEW</span><span>MOVE <b>→</b> SENSE <b>→</b> COUNT</span></div>
      </div>
      <div class="hero-bottom-label"><span>MECHANICAL × ELECTRONIC × LOGIC</span><span>SCROLL TO EXPLORE <span aria-hidden="true">↓</span></span></div>
    </section>

    <section id="system" class="intro section-wrap">
      <div class="section-kicker"><span>01</span> THE IDEA</div>
      <div class="intro-grid">
        <h2>One passing object.<br><span>One reliable count.</span></h2>
        <div class="intro-copy">
          <p class="body-large">This compact prototype brings a moving belt, an infrared sensor, an Arduino Uno, and an LCD together as one simple counting system.</p>
          <p>It demonstrates a principle used on production lines: detect each item at a fixed point, process the event, and make the total easy to read.</p>
        </div>
      </div>
      <div class="stats-row">
        <div class="stat"><span class="stat-symbol">↗</span><div><strong>Low-cost</strong><span>Accessible materials and parts</span></div></div>
        <div class="stat"><span class="stat-symbol">◎</span><div><strong>Non-contact</strong><span>IR sensing at a fixed point</span></div></div>
        <div class="stat"><span class="stat-symbol">▤</span><div><strong>Standalone</strong><span>Count shown directly on an LCD</span></div></div>
      </div>
    </section>

    <section id="how-it-works" class="workflow-section">
      <div class="section-wrap">
        <div class="section-kicker section-kicker-light"><span>02</span> HOW IT WORKS</div>
        <div class="section-heading-row">
          <h2>Four steps.<br><span>One complete loop.</span></h2>
          <p>Each new sensor event represents one object passing the detection point.</p>
        </div>
        <div class="workflow">
          <article class="workflow-step">
            <span class="step-index">01 / MOVE</span>
            <div class="step-icon belt-icon" aria-hidden="true"><span /><span /><span /></div>
            <h3>The belt carries</h3>
            <p>A sample object travels along the corrugated belt toward the sensor.</p>
            <div class="step-arrow" aria-hidden="true">↗</div>
          </article>
          <article class="workflow-step">
            <span class="step-index">02 / DETECT</span>
            <div class="step-icon sensor-icon" aria-hidden="true"><span /><span /><span /></div>
            <h3>The IR sensor sees</h3>
            <p>A passing object changes the sensor output inside its detection zone.</p>
            <div class="step-arrow" aria-hidden="true">↗</div>
          </article>
          <article class="workflow-step">
            <span class="step-index">03 / COUNT</span>
            <div class="step-icon chip-icon" aria-hidden="true"><span>μ</span></div>
            <h3>The Arduino counts</h3>
            <p>The controller recognizes the event and increments the running total.</p>
            <div class="step-arrow" aria-hidden="true">↗</div>
          </article>
          <article class="workflow-step">
            <span class="step-index">04 / DISPLAY</span>
            <div class="step-icon display-icon" aria-hidden="true"><span>012</span></div>
            <h3>The LCD updates</h3>
            <p>The latest count is displayed for the operator—no computer needed.</p>
          </article>
        </div>
        <div class="workflow-note"><span class="note-icon">i</span><span>For consistent detection, pass objects one at a time with a visible gap between them.</span></div>
      </div>
    </section>

    <section id="build" class="build-section section-wrap">
      <div class="section-kicker"><span>03</span> THE BUILD</div>
      <div class="build-heading">
        <h2>Built to learn.<br><span>Designed to be improved.</span></h2>
        <p>A handmade tabletop assembly keeps the mechanism visible, understandable, and easy to adjust.</p>
      </div>
      <div class="build-layout">
        <div class="build-card">
          <div class="build-card-top"><span>THE MECHANICAL SIDE</span><span>FIG. 02</span></div>
          <div class="photo-grid" aria-label="Original photos of the team prototype">
            <figure class="photo-tile photo-tile-main">
              <img src="/photos/prototype-overview.jpg" alt="Original team photo showing the mini conveyor prototype with its cardboard belt, sample objects, Arduino, and LCD" loading="lazy" decoding="async">
              <figcaption><span>01</span> FULL PROTOTYPE</figcaption>
            </figure>
            <figure class="photo-tile">
              <img src="/photos/prototype-top-view.jpg" alt="Original overhead photo of the corrugated belt and sample objects" loading="lazy" decoding="async">
              <figcaption><span>02</span> BELT &amp; OBJECTS</figcaption>
            </figure>
            <figure class="photo-tile">
              <img src="/photos/prototype-electronics.jpg" alt="Original side photo showing the Arduino, breadboard connections, motor, and underside of the belt" loading="lazy" decoding="async">
              <figcaption><span>03</span> ELECTRONICS</figcaption>
            </figure>
          </div>
          <div class="materials-list">
            <div><span>01</span><strong>Corrugated cardboard</strong><small>Moving belt surface</small></div>
            <div><span>02</span><strong>Black board / cardboard</strong><small>Track frame and panels</small></div>
            <div><span>03</span><strong>Foam blocks</strong><small>Spacers and supports</small></div>
            <div><span>04</span><strong>Small DC motor</strong><small>Drives belt movement</small></div>
          </div>
        </div>
        <div class="electronics-column">
          <div class="electronics-card">
            <div class="build-card-top"><span>THE ELECTRONIC SIDE</span><span>04 MODULES</span></div>
            <div class="component-row">
              <span class="component-mark arduino-mark">A</span>
              <div><h3>Arduino Uno</h3><p>Reads the sensor and manages the running count.</p></div>
            </div>
            <div class="component-row">
              <span class="component-mark sensor-mark">IR</span>
              <div><h3>IR sensor</h3><p>Senses an object passing at the detection point.</p></div>
            </div>
            <div class="component-row">
              <span class="component-mark lcd-mark">01</span>
              <div><h3>16×2 LCD</h3><p>Shows the current total to the operator.</p></div>
            </div>
            <div class="component-row">
              <span class="component-mark wire-mark">+</span>
              <div><h3>Breadboard &amp; wires</h3><p>Connect modules for easy inspection and adjustment.</p></div>
            </div>
          </div>
          <div class="wiring-note"><span class="wiring-icon">⌁</span><p>Modules connect through a breadboard, making the prototype easy to test and change without soldering.</p></div>
        </div>
      </div>
    </section>

    <section class="demo-section" aria-labelledby="demo-title">
      <div class="section-wrap demo-grid">
        <div>
          <div class="section-kicker section-kicker-light"><span>TRY IT</span> LIVE COUNTER DEMO</div>
          <h2 id="demo-title">See the count<br><span>update.</span></h2>
          <p>In the prototype, a new object detection updates the LCD. Simulate a pass below.</p>
        </div>
        <div class="demo-display">
          <div class="lcd-bezel">
            <div class="lcd-screen">
              <span>OBJECTS DETECTED</span>
              <strong>{{ String(demoCount).padStart(3, '0') }}</strong>
            </div>
            <div class="lcd-controls"><i /><i /><i /></div>
          </div>
          <div class="demo-controls">
            <button class="button button-lime" type="button" @click="demoCount += 1">Simulate object <span aria-hidden="true">＋</span></button>
            <button class="reset-button" type="button" @click="demoCount = 0">Reset count</button>
          </div>
          <p class="demo-status" aria-live="polite">{{ demoCount === 0 ? 'Ready for the first object.' : `${demoCount} ${demoCount === 1 ? 'object' : 'objects'} counted in this demo.` }}</p>
        </div>
      </div>
    </section>

    <section id="testing" class="testing-section section-wrap">
      <div class="section-kicker"><span>04</span> TEST &amp; EVALUATE</div>
      <div class="testing-grid">
        <div class="testing-intro">
          <h2>Make every<br><span>trial count.</span></h2>
          <p>Repeatable tests help reveal missed detections, double counts, and mechanical issues before drawing conclusions.</p>
          <div class="formula-card">
            <span class="formula-label">MEASURE ACCURACY</span>
            <div class="formula">Displayed count <span>÷</span> actual objects <span>× 100%</span></div>
            <p>Record the result for every trial. Compare repeated runs at different spacings.</p>
          </div>
        </div>
        <div class="test-list">
          <div class="test-item"><span class="test-number">01</span><div><h3>Power-on check</h3><p>Confirm the Arduino starts and the LCD is readable.</p></div><span class="test-tag">START</span></div>
          <div class="test-item"><span class="test-number">02</span><div><h3>One-object trial</h3><p>Pass one item and check that the count increases by one.</p></div><span class="test-tag">SINGLE</span></div>
          <div class="test-item"><span class="test-number">03</span><div><h3>Multiple-object trial</h3><p>Compare a known number of separated objects with the display.</p></div><span class="test-tag">REPEAT</span></div>
          <div class="test-item"><span class="test-number">04</span><div><h3>Spacing trial</h3><p>Repeat with different gaps to look for missed or double counts.</p></div><span class="test-tag">TUNE</span></div>
          <div class="test-item"><span class="test-number">05</span><div><h3>Belt trial</h3><p>Observe tracking, movement, and whether items stay on the belt.</p></div><span class="test-tag">MECHANICS</span></div>
        </div>
      </div>
      <div class="honesty-note"><span>!</span><p><strong>Results matter.</strong> Accuracy should be reported only after measurements are collected across repeatable trials.</p></div>
    </section>

    <section id="next" class="improve-section">
      <div class="section-wrap">
        <div class="section-kicker section-kicker-light"><span>05</span> LIMITATIONS → NEXT STEPS</div>
        <div class="improve-heading"><h2>Good prototypes<br><span>make the next step clear.</span></h2><p>Practical refinements can make the system more stable and reliable.</p></div>
        <div class="improvements-grid">
          <article><span class="improvement-icon">↔</span><span class="improvement-index">01</span><h3>Keep the belt aligned</h3><p>Add side guides and adjust rollers or supports to reduce drift and wrinkles.</p></article>
          <article><span class="improvement-icon">⌖</span><span class="improvement-index">02</span><h3>Fix the sensor position</h3><p>Secure the IR sensor and keep each object on the same path.</p></article>
          <article><span class="improvement-icon">⌁</span><span class="improvement-index">03</span><h3>Protect the wiring</h3><p>Route and secure jumper wires away from moving parts and the motor shaft.</p></article>
          <article><span class="improvement-icon">↻</span><span class="improvement-index">04</span><h3>Refine count reliability</h3><p>Test a suitable debounce or detection lockout at different belt speeds.</p></article>
          <article><span class="improvement-icon">▱</span><span class="improvement-index">05</span><h3>Strengthen the frame</h3><p>Reinforce flexible supports so the track stays level while operating.</p></article>
          <article><span class="improvement-icon">▤</span><span class="improvement-index">06</span><h3>Plan the next upgrade</h3><p>Consider motor speed control, a reset button, or saving and sharing counts.</p></article>
        </div>
      </div>
    </section>

    <section class="qa-section section-wrap">
      <div class="section-kicker"><span>06</span> QUESTIONS WE EXPECT</div>
      <div class="qa-heading"><h2>Ready for<br><span>the why?</span></h2><p>A few design choices worth explaining during the presentation.</p></div>
      <div class="qa-grid">
        <article class="qa-card"><span>WHY AN IR SENSOR?</span><h3>Low-cost, non-contact detection.</h3><p>It gives the Arduino a clear signal when an object passes close to the fixed sensor—well suited to this small setup.</p></article>
        <article class="qa-card"><span>WHY SPACE OBJECTS?</span><h3>Touching items can look like one.</h3><p>A visible gap helps create distinct detection events. Production systems use guides or faster sensing to handle closer spacing.</p></article>
        <article class="qa-card"><span>WHERE IS THIS USED?</span><h3>The same idea scales up.</h3><p>Factories, warehouses, and packaging lines use detect-and-count systems to track production and inventory.</p></article>
      </div>
    </section>

    <footer class="footer">
      <div class="section-wrap footer-main">
        <div class="footer-mark" aria-hidden="true">MC<span>.</span></div>
        <div class="footer-copy"><span>THE TAKEAWAY</span><h2>A practical model<br>for automatic counting.</h2><p>The belt moves each sample. The IR sensor detects it. The Arduino counts it. The LCD makes the total visible.</p></div>
        <a class="back-top" href="#top">Back to top <span aria-hidden="true">↑</span></a>
      </div>
      <div class="section-wrap footer-bottom"><span>MINI CONVEYOR BELT OBJECT COUNTER</span><span>ARDUINO PROTOTYPE PRESENTATION</span><span>MOVE <b>·</b> SENSE <b>·</b> COUNT</span></div>
    </footer>
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&display=swap');

:root {
  --ink: #17231f;
  --green: #193d34;
  --green-deep: #102b25;
  --green-mid: #31574b;
  --paper: #f5f6ef;
  --paper-dark: #e9eee6;
  --lime: #c8f17b;
  --orange: #e7954c;
  --muted: #68756e;
  --line: #dce2d8;
  --mono: 'DM Mono', 'Courier New', monospace;
  --sans: 'DM Sans', 'Segoe UI', sans-serif;
  --display: 'Manrope', 'Segoe UI', sans-serif;
  scroll-behavior: smooth;
  scroll-padding-top: 85px;
}

* { box-sizing: border-box; }
body { margin: 0; background: var(--paper); color: var(--ink); font-family: var(--sans); -webkit-font-smoothing: antialiased; }
button, a { font: inherit; }
a { color: inherit; text-decoration: none; }
button:focus-visible, a:focus-visible { outline: 3px solid var(--orange); outline-offset: 4px; }
.section-wrap { width: min(1190px, calc(100% - 80px)); margin-inline: auto; }

.site-header { height: 76px; padding: 0 max(40px, calc((100% - 1190px) / 2)); display: flex; align-items: center; justify-content: space-between; background: var(--green-deep); color: #f5f6ef; }
.brand { display: flex; align-items: center; gap: 10px; font-size: 13px; font-weight: 700; letter-spacing: .07em; }
.brand-light { font-weight: 400; opacity: .7; }
.brand-mark { width: 30px; height: 30px; display: grid; place-items: center; border: 1px solid #799283; border-radius: 50%; }
.brand-mark svg { width: 20px; stroke: var(--lime); stroke-width: 1.5; stroke-linecap: round; }
.main-nav { display: flex; gap: 34px; margin-left: 52px; }
.main-nav a, .header-cta { font-size: 12px; color: #d4dfd6; transition: color .2s ease; }
.main-nav a:hover, .header-cta:hover { color: var(--lime); }
.header-cta { display: flex; align-items: center; gap: 11px; }
.header-cta span { color: var(--lime); font-size: 17px; }

.hero { position: relative; min-height: 640px; padding: 72px max(40px, calc((100% - 1190px) / 2)) 83px; background: var(--green-deep); color: #f5f6ef; display: grid; grid-template-columns: .91fr 1.09fr; align-items: center; gap: 42px; overflow: hidden; }
.hero::before { content: ''; position: absolute; width: 680px; height: 680px; left: -260px; top: -350px; border: 1px solid rgba(205, 235, 206, .08); border-radius: 50%; box-shadow: 0 0 0 60px rgba(205, 235, 206, .025), 0 0 0 120px rgba(205, 235, 206, .018); pointer-events: none; }
.hero-copy { position: relative; z-index: 1; padding-bottom: 12px; }
.eyebrow, .section-kicker { font-family: var(--mono); font-size: 10px; letter-spacing: .09em; text-transform: uppercase; }
.eyebrow-light { color: #aabdb0; display: flex; align-items: center; gap: 9px; }
.status-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--lime); box-shadow: 0 0 12px rgba(200, 241, 123, .6); }
.eyebrow-separator { color: #688073; }
h1, h2, h3, p { margin-top: 0; }
.hero h1 { margin: 25px 0 18px; font-family: var(--display); font-size: clamp(51px, 5.3vw, 76px); line-height: .99; letter-spacing: -.065em; font-weight: 600; }
.accent-period { color: var(--lime); }
.hero-lede { max-width: 430px; margin-bottom: 28px; color: #b8c7bb; font-size: 16px; line-height: 1.7; }
.hero-actions { display: flex; align-items: center; gap: 20px; }
.button { border: 0; border-radius: 3px; padding: 14px 18px; font-size: 12px; font-weight: 700; display: inline-flex; gap: 22px; align-items: center; cursor: pointer; transition: transform .18s ease, background .18s ease; }
.button:hover { transform: translateY(-2px); }
.button-lime { background: var(--lime); color: #183229; }
.button-lime:hover { background: #d6f89a; }
.hero-note { font-size: 11px; color: #8fa398; }
.hero-facts { margin-top: 54px; padding-top: 16px; max-width: 440px; border-top: 1px solid rgba(217, 231, 217, .2); display: flex; justify-content: space-between; }
.hero-facts div { display: flex; flex-direction: column; gap: 7px; font-size: 11px; color: #d2ded2; }
.fact-number { color: #789184; font: 9px var(--mono); }
.hero-art { position: relative; padding: 11px; border: 1px solid rgba(227, 239, 225, .16); border-radius: 21px; background: rgba(235, 243, 231, .04); }
.art-topline, .art-caption { color: #9aafa0; font: 9px var(--mono); letter-spacing: .07em; display: flex; justify-content: space-between; padding: 8px 11px 10px; }
.art-topline span:first-child { color: var(--lime); }
.machine-illustration { display: block; width: 100%; height: auto; border-radius: 13px; }
.diagram-label text { fill: #31483d; font: 10px var(--mono); letter-spacing: .04em; }
.art-small { fill: #71897b; font: 8px var(--mono); letter-spacing: .06em; }
.art-caption { padding-top: 11px; padding-bottom: 3px; }
.art-caption b { color: var(--lime); padding-inline: 3px; }
.hero-bottom-label { position: absolute; bottom: 0; left: max(40px, calc((100% - 1190px) / 2)); right: max(40px, calc((100% - 1190px) / 2)); padding: 16px 0; border-top: 1px solid rgba(217, 231, 217, .15); display: flex; justify-content: space-between; color: #82988b; font: 9px var(--mono); letter-spacing: .08em; }
.hero-bottom-label span:last-child span { color: var(--lime); padding-left: 5px; }

.intro { padding-top: 108px; padding-bottom: 95px; }
.section-kicker { color: #77877e; display: flex; align-items: center; gap: 12px; }
.section-kicker span { color: #bd8050; }
.intro-grid { margin-top: 35px; display: grid; grid-template-columns: 1fr .75fr; gap: 90px; align-items: start; }
h2 { font-family: var(--display); font-size: clamp(38px, 4vw, 54px); line-height: 1.08; letter-spacing: -.055em; font-weight: 600; }
.intro h2, .build-heading h2, .testing-intro h2, .qa-heading h2 { margin: 0; }
.intro h2 span, .build-heading h2 span, .testing-intro h2 span, .qa-heading h2 span { color: #8b9b8e; }
.intro-copy { padding-top: 3px; }
.body-large { margin-bottom: 16px; font-family: var(--display); font-size: 18px; line-height: 1.55; font-weight: 500; }
.intro-copy p:last-child { color: var(--muted); font-size: 13px; line-height: 1.8; }
.stats-row { margin-top: 60px; padding: 24px 0; border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); display: grid; grid-template-columns: repeat(3, 1fr); }
.stat { display: flex; align-items: center; gap: 14px; padding-left: 28px; border-left: 1px solid var(--line); }
.stat:first-child { padding-left: 0; border-left: 0; }
.stat-symbol { width: 38px; height: 38px; display: grid; place-items: center; color: #31594b; background: #e5ecdf; border-radius: 50%; font-size: 18px; }
.stat strong, .stat span:last-child { display: block; }
.stat strong { font-family: var(--display); font-size: 13px; margin-bottom: 4px; }
.stat div span { color: var(--muted); font-size: 11px; }

.workflow-section { padding: 88px 0 92px; background: #e9eee6; }
.section-kicker-light { color: #a8b8aa; }
.section-kicker-light span { color: var(--lime); }
.section-heading-row { margin: 30px 0 43px; display: flex; justify-content: space-between; align-items: end; }
.section-heading-row h2 { margin: 0; }
.section-heading-row h2 span { color: #899a8d; }
.section-heading-row p { max-width: 285px; margin: 0 0 5px; color: #65756a; font-size: 13px; line-height: 1.7; }
.workflow { display: grid; grid-template-columns: repeat(4, 1fr); border: 1px solid #d5ded3; background: rgba(255,255,255,.28); }
.workflow-step { min-height: 245px; position: relative; padding: 23px 22px; border-right: 1px solid #d5ded3; }
.workflow-step:last-child { border-right: 0; }
.step-index { color: #87988d; font: 9px var(--mono); letter-spacing: .06em; }
.step-icon { height: 68px; margin: 20px 0 17px; display: flex; align-items: center; justify-content: center; color: #345b4d; }
.belt-icon { gap: 4px; position: relative; }
.belt-icon::before { content: ''; position: absolute; width: 66px; height: 16px; border: 2px solid #527464; border-radius: 50%; transform: rotate(-12deg); }
.belt-icon span { z-index: 1; width: 9px; height: 9px; border-radius: 2px; background: #dda15d; transform: translateY(-4px) rotate(15deg); }
.sensor-icon { gap: 5px; }
.sensor-icon span:first-child { width: 15px; height: 24px; background: #e7954c; border-radius: 3px; }
.sensor-icon span:nth-child(2), .sensor-icon span:nth-child(3) { width: 18px; height: 1px; background: #d29056; transform: rotate(-14deg); }
.sensor-icon span:nth-child(3) { width: 25px; }
.chip-icon span { width: 43px; height: 43px; border: 2px solid #527464; display: grid; place-items: center; font: 21px var(--mono); border-radius: 7px; }
.display-icon span { padding: 8px 11px; border: 2px solid #527464; border-radius: 4px; color: #345b4d; background: #d8e5d7; font: 14px var(--mono); }
.workflow-step h3 { margin: 0 0 8px; font-family: var(--display); font-size: 15px; letter-spacing: -.02em; }
.workflow-step p { max-width: 220px; margin: 0; color: #6b796e; font-size: 11px; line-height: 1.65; }
.step-arrow { position: absolute; top: 21px; right: 19px; color: #a8b5a9; }
.workflow-note { margin-top: 17px; display: flex; align-items: center; gap: 10px; color: #718077; font-size: 11px; }
.note-icon { width: 17px; height: 17px; border: 1px solid #9aab9e; border-radius: 50%; display: grid; place-items: center; font: 10px var(--mono); }

.build-section { padding-top: 104px; padding-bottom: 108px; }
.build-heading { margin: 30px 0 43px; display: flex; align-items: end; justify-content: space-between; gap: 35px; }
.build-heading > p { max-width: 300px; margin: 0 0 6px; color: var(--muted); font-size: 13px; line-height: 1.7; }
.build-layout { display: grid; grid-template-columns: 1.07fr .93fr; gap: 22px; }
.build-card, .electronics-card { border: 1px solid var(--line); background: #fbfcf8; }
.build-card-top { padding: 17px 19px; display: flex; justify-content: space-between; border-bottom: 1px solid var(--line); color: #68796e; font: 9px var(--mono); letter-spacing: .06em; }
.build-card-top span:last-child { color: #a3afa5; }
.photo-grid { height: 270px; margin: 0 12px; padding: 10px; display: grid; grid-template-columns: 1.25fr 1fr; grid-template-rows: 1fr 1fr; gap: 8px; background: #edf0e9; }
.photo-tile { min-width: 0; min-height: 0; position: relative; margin: 0; overflow: hidden; background: #d7ddd4; }
.photo-tile::after { content: ''; position: absolute; inset: 30% 0 0; background: linear-gradient(transparent, rgba(10, 25, 20, .68)); pointer-events: none; }
.photo-tile img { width: 100%; height: 100%; display: block; object-fit: cover; transition: transform .45s ease; }
.photo-tile:hover img { transform: scale(1.035); }
.photo-tile-main { grid-row: span 2; }
.photo-tile-main img { object-position: 54% center; }
.photo-tile:nth-child(2) img { object-position: center 48%; }
.photo-tile figcaption { position: absolute; z-index: 1; bottom: 10px; left: 10px; right: 8px; color: #fff; font: 8px var(--mono); letter-spacing: .05em; }
.photo-tile figcaption span { color: var(--lime); margin-right: 5px; }
.materials-list { padding: 0 20px 19px; display: grid; grid-template-columns: 1fr 1fr; gap: 15px 20px; }
.materials-list > div { display: grid; grid-template-columns: 24px 1fr; align-items: baseline; }
.materials-list span { grid-row: span 2; color: #bc8554; font: 9px var(--mono); }
.materials-list strong { font-size: 10px; font-weight: 600; }
.materials-list small { margin-top: 3px; color: #839087; font-size: 9px; }
.electronics-column { display: flex; flex-direction: column; gap: 14px; }
.electronics-card { flex: 1; }
.component-row { min-height: 83px; margin: 0 19px; display: flex; align-items: center; gap: 14px; border-bottom: 1px solid #e8ece5; }
.component-row:last-child { border-bottom: 0; }
.component-mark { width: 37px; height: 37px; flex: 0 0 auto; display: grid; place-items: center; border-radius: 9px; font: 11px var(--mono); }
.arduino-mark { color: #315da7; background: #e8eef8; }
.sensor-mark { color: #bd7136; background: #f7eee3; }
.lcd-mark { color: #3a6954; background: #e8efe7; }
.wire-mark { color: #80668c; background: #f1ebf3; font-size: 19px; }
.component-row h3 { margin: 0 0 5px; font-family: var(--display); font-size: 12px; }
.component-row p { margin: 0; color: #77847a; font-size: 10px; line-height: 1.5; }
.wiring-note { padding: 17px 20px; display: flex; align-items: center; gap: 13px; background: #e8eee5; }
.wiring-icon { color: #48755d; font-size: 25px; }
.wiring-note p { margin: 0; color: #596a5e; font-size: 10px; line-height: 1.6; }

.demo-section { padding: 80px 0; background: var(--green); color: #f5f6ef; }
.demo-grid { display: grid; grid-template-columns: 1fr 1fr; align-items: center; gap: 80px; }
.demo-grid h2 { margin: 24px 0 14px; }
.demo-grid h2 span { color: var(--lime); }
.demo-grid > div:first-child > p { max-width: 360px; color: #b6c8b9; font-size: 13px; line-height: 1.7; }
.demo-display { padding: 28px; background: rgba(8, 30, 25, .26); border: 1px solid rgba(226, 242, 222, .13); border-radius: 8px; }
.lcd-bezel { padding: 15px; background: #263d33; border-radius: 6px; box-shadow: inset 0 2px 4px rgba(0,0,0,.25); }
.lcd-screen { min-height: 144px; padding: 16px 19px; display: flex; flex-direction: column; justify-content: space-between; background: #c8d8ae; color: #294631; border: 5px solid #9db28a; font-family: var(--mono); }
.lcd-screen span { font-size: 10px; letter-spacing: .08em; }
.lcd-screen strong { font-size: 62px; line-height: .9; font-weight: 400; letter-spacing: .08em; }
.lcd-controls { padding: 11px 3px 1px; display: flex; justify-content: flex-end; gap: 7px; }
.lcd-controls i { width: 6px; height: 6px; border-radius: 50%; background: #859687; }
.demo-controls { margin-top: 21px; display: flex; align-items: center; justify-content: space-between; gap: 12px; }
.reset-button { border: 0; padding: 10px 0; background: transparent; color: #c3d0c4; font-size: 11px; cursor: pointer; }
.reset-button:hover { color: var(--lime); }
.demo-status { margin: 13px 0 0; color: #9db3a3; font: 10px var(--mono); }

.testing-section { padding-top: 104px; padding-bottom: 100px; }
.testing-grid { margin-top: 34px; display: grid; grid-template-columns: .78fr 1.22fr; gap: 80px; }
.testing-intro > p { max-width: 325px; margin: 18px 0 27px; color: var(--muted); font-size: 12px; line-height: 1.75; }
.formula-card { padding: 17px 18px; background: #e9eee6; border-left: 3px solid #749277; }
.formula-label { color: #77887b; font: 8px var(--mono); letter-spacing: .08em; }
.formula { margin: 11px 0; font-family: var(--display); font-size: 14px; font-weight: 700; letter-spacing: -.02em; }
.formula span { color: #719076; padding: 0 3px; }
.formula-card p { margin: 0; color: #7b887e; font-size: 9px; line-height: 1.6; }
.test-list { border-top: 1px solid var(--line); }
.test-item { min-height: 76px; display: grid; grid-template-columns: 35px 1fr auto; align-items: center; gap: 15px; border-bottom: 1px solid var(--line); }
.test-number { color: #bd8556; font: 10px var(--mono); }
.test-item h3 { margin: 0 0 5px; font-family: var(--display); font-size: 12px; }
.test-item p { margin: 0; color: #7b877e; font-size: 10px; }
.test-tag { color: #819086; font: 8px var(--mono); letter-spacing: .05em; }
.honesty-note { margin-top: 24px; padding: 15px 18px; display: flex; align-items: center; gap: 12px; background: #f0eade; }
.honesty-note > span { width: 18px; height: 18px; display: grid; place-items: center; color: #a76539; border: 1px solid #d6a177; border-radius: 50%; font: 10px var(--mono); }
.honesty-note p { margin: 0; color: #6f6c60; font-size: 10px; }
.honesty-note strong { color: #4b5148; }

.improve-section { padding: 89px 0 94px; background: var(--green-deep); color: #f2f5ee; }
.improve-heading { margin: 29px 0 43px; display: flex; align-items: end; justify-content: space-between; }
.improve-heading h2 { margin: 0; }
.improve-heading h2 span { color: #9eb29f; }
.improve-heading > p { max-width: 270px; margin: 0 0 5px; color: #a9bbb0; font-size: 12px; line-height: 1.7; }
.improvements-grid { display: grid; grid-template-columns: repeat(3, 1fr); border-top: 1px solid rgba(220,237,221,.19); border-left: 1px solid rgba(220,237,221,.19); }
.improvements-grid article { min-height: 180px; position: relative; padding: 22px 21px; border-right: 1px solid rgba(220,237,221,.19); border-bottom: 1px solid rgba(220,237,221,.19); }
.improvement-icon { color: var(--lime); font-size: 21px; }
.improvement-index { position: absolute; top: 24px; right: 20px; color: #718a7c; font: 9px var(--mono); }
.improvements-grid h3 { margin: 20px 0 8px; font-family: var(--display); font-size: 13px; }
.improvements-grid p { max-width: 260px; margin: 0; color: #9aafa1; font-size: 10px; line-height: 1.7; }

.qa-section { padding-top: 96px; padding-bottom: 101px; }
.qa-heading { margin: 30px 0 34px; display: flex; justify-content: space-between; align-items: end; }
.qa-heading h2 { margin: 0; }
.qa-heading h2 span { color: #899b8d; }
.qa-heading p { max-width: 250px; margin: 0 0 4px; color: var(--muted); font-size: 12px; line-height: 1.7; }
.qa-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; }
.qa-card { min-height: 197px; padding: 21px 21px 24px; border: 1px solid var(--line); background: #fafbf7; }
.qa-card > span { color: #b47c4c; font: 8px var(--mono); letter-spacing: .08em; }
.qa-card h3 { margin: 24px 0 10px; font-family: var(--display); font-size: 16px; line-height: 1.3; letter-spacing: -.03em; }
.qa-card p { margin: 0; color: #748077; font-size: 10px; line-height: 1.7; }

.footer { padding-top: 55px; background: #e7ece4; }
.footer-main { min-height: 245px; display: grid; grid-template-columns: 1fr 2fr auto; align-items: center; gap: 45px; }
.footer-mark { color: #315647; font: 700 38px var(--display); letter-spacing: -.09em; }
.footer-mark span { color: #c18351; }
.footer-copy > span { color: #7a897e; font: 9px var(--mono); letter-spacing: .08em; }
.footer-copy h2 { margin: 15px 0 10px; font-size: 34px; }
.footer-copy p { max-width: 430px; margin: 0; color: #6b796f; font-size: 11px; line-height: 1.7; }
.back-top { display: flex; gap: 12px; align-items: center; padding-bottom: 5px; border-bottom: 1px solid #9cac9d; font-size: 11px; }
.back-top span { color: #6c896f; font-size: 16px; }
.footer-bottom { min-height: 51px; border-top: 1px solid #d0d9ce; display: flex; align-items: center; justify-content: space-between; color: #87958a; font: 8px var(--mono); letter-spacing: .06em; }
.footer-bottom b { color: #b78152; }

@media (min-width: 1500px) {
  .hero { min-height: 710px; }
}
@media (max-width: 900px) {
  .site-header { padding-inline: 28px; }
  .main-nav { gap: 18px; margin-left: 12px; }
  .header-cta { display: none; }
  .section-wrap { width: min(100% - 56px, 700px); }
  .hero { padding-inline: 28px; grid-template-columns: 1fr 1fr; gap: 24px; min-height: 570px; }
  .hero-bottom-label { left: 28px; right: 28px; }
  .hero h1 { font-size: clamp(47px, 6vw, 65px); }
  .hero-lede { font-size: 14px; }
  .hero-note { display: none; }
  .intro-grid { gap: 36px; }
  .workflow-step { padding-inline: 14px; }
  .workflow-step h3 { font-size: 13px; }
  .build-layout { grid-template-columns: 1fr 1fr; gap: 14px; }
  .materials-list { padding-inline: 12px; gap: 15px 8px; }
  .testing-grid { gap: 35px; }
}
@media (max-width: 650px) {
  :root { scroll-padding-top: 65px; }
  .section-wrap { width: calc(100% - 40px); }
  .site-header { height: 63px; padding-inline: 20px; }
  .brand { font-size: 11px; }
  .brand-mark { width: 27px; height: 27px; }
  .main-nav { display: none; }
  .hero { padding: 54px 20px 75px; display: flex; flex-direction: column; align-items: stretch; gap: 37px; }
  .hero h1 { margin-top: 22px; font-size: clamp(48px, 13vw, 68px); }
  .hero-lede { max-width: 370px; }
  .hero-facts { margin-top: 37px; }
  .hero-art { padding: 7px; border-radius: 14px; }
  .art-topline, .art-caption { font-size: 7px; padding-inline: 7px; }
  .hero-bottom-label { left: 20px; right: 20px; font-size: 7px; }
  .intro, .build-section, .testing-section, .qa-section { padding-top: 72px; padding-bottom: 70px; }
  .intro-grid { grid-template-columns: 1fr; gap: 20px; margin-top: 26px; }
  h2 { font-size: clamp(37px, 10vw, 49px); }
  .body-large { font-size: 16px; }
  .stats-row { margin-top: 35px; grid-template-columns: 1fr; padding: 10px 0; }
  .stat, .stat:first-child { min-height: 68px; padding: 10px 0; border-left: 0; border-bottom: 1px solid var(--line); }
  .stat:last-child { border-bottom: 0; }
  .workflow-section, .improve-section { padding: 69px 0; }
  .section-heading-row, .build-heading, .improve-heading, .qa-heading { align-items: start; flex-direction: column; gap: 16px; margin-top: 26px; margin-bottom: 30px; }
  .section-heading-row p, .build-heading > p, .improve-heading > p, .qa-heading p { max-width: 350px; }
  .workflow { grid-template-columns: 1fr 1fr; }
  .workflow-step { min-height: 223px; padding: 17px 14px; border-bottom: 1px solid #d5ded3; }
  .workflow-step:nth-child(2) { border-right: 0; }
  .workflow-step:nth-child(3), .workflow-step:nth-child(4) { border-bottom: 0; }
  .workflow-step p { font-size: 10px; }
  .step-icon { margin: 12px 0; }
  .workflow-note { align-items: start; line-height: 1.6; }
  .build-layout { grid-template-columns: 1fr; }
  .photo-grid { height: 245px; margin-inline: 7px; padding: 7px; gap: 6px; }
  .photo-tile figcaption { bottom: 7px; left: 7px; font-size: 7px; }
  .materials-list strong { font-size: 9px; }
  .demo-section { padding: 64px 0; }
  .demo-grid { grid-template-columns: 1fr; gap: 28px; }
  .demo-display { padding: 18px; }
  .lcd-screen { min-height: 130px; }
  .testing-grid { grid-template-columns: 1fr; gap: 28px; margin-top: 27px; }
  .testing-intro > p { max-width: 420px; }
  .test-item { grid-template-columns: 27px 1fr; gap: 10px; min-height: 82px; }
  .test-tag { display: none; }
  .test-item p { line-height: 1.5; }
  .honesty-note { align-items: start; line-height: 1.6; }
  .improvements-grid { grid-template-columns: 1fr 1fr; }
  .improvements-grid article { min-height: 177px; padding: 17px 14px; }
  .improvements-grid h3 { font-size: 12px; }
  .improvements-grid p { font-size: 9px; }
  .improvement-index { right: 12px; }
  .qa-grid { grid-template-columns: 1fr; }
  .qa-card { min-height: auto; }
  .qa-card h3 { margin-top: 16px; }
  .footer { padding-top: 36px; }
  .footer-main { padding-bottom: 30px; grid-template-columns: 1fr auto; gap: 16px; }
  .footer-mark { grid-column: 1 / -1; font-size: 29px; }
  .footer-copy h2 { font-size: 28px; }
  .footer-copy p { max-width: 330px; }
  .back-top { align-self: end; font-size: 10px; }
  .footer-bottom { min-height: 58px; gap: 8px; font-size: 7px; }
  .footer-bottom span:nth-child(2) { display: none; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { scroll-behavior: auto !important; transition-duration: .01ms !important; animation-duration: .01ms !important; }
}
</style>
