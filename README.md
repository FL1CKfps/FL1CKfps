<div align="center">

<!-- ============================================================
     HERO BANNER — custom inline SVG with particle rain,
     glowing text pulse, and scanline sweep
     ============================================================ -->

<svg width="900" height="280" viewBox="0 0 900 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Background gradient -->
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%"   stop-color="#0a0a0a"/>
      <stop offset="50%"  stop-color="#1a0f00"/>
      <stop offset="100%" stop-color="#0d0d0d"/>
    </linearGradient>
    <!-- Orange glow filter -->
    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="softglow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <!-- Scanline sweep gradient -->
    <linearGradient id="sweep" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%"   stop-color="#FF8C00" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#FF8C00" stop-opacity="0.08"/>
      <stop offset="100%" stop-color="#FF8C00" stop-opacity="0"/>
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="900" height="280" fill="url(#bg)" rx="12"/>

  <!-- Grid lines horizontal -->
  <g stroke="#FF8C00" stroke-opacity="0.06" stroke-width="1">
    <line x1="0" y1="40"  x2="900" y2="40"/>
    <line x1="0" y1="80"  x2="900" y2="80"/>
    <line x1="0" y1="120" x2="900" y2="120"/>
    <line x1="0" y1="160" x2="900" y2="160"/>
    <line x1="0" y1="200" x2="900" y2="200"/>
    <line x1="0" y1="240" x2="900" y2="240"/>
  </g>
  <!-- Grid lines vertical -->
  <g stroke="#FF8C00" stroke-opacity="0.04" stroke-width="1">
    <line x1="90"  y1="0" x2="90"  y2="280"/>
    <line x1="180" y1="0" x2="180" y2="280"/>
    <line x1="270" y1="0" x2="270" y2="280"/>
    <line x1="360" y1="0" x2="360" y2="280"/>
    <line x1="450" y1="0" x2="450" y2="280"/>
    <line x1="540" y1="0" x2="540" y2="280"/>
    <line x1="630" y1="0" x2="630" y2="280"/>
    <line x1="720" y1="0" x2="720" y2="280"/>
    <line x1="810" y1="0" x2="810" y2="280"/>
  </g>

  <!-- Scanline sweep animation -->
  <rect width="900" height="280" fill="url(#sweep)" rx="12" opacity="0.8">
    <animateTransform attributeName="transform" type="translate" values="0,-280;0,280" dur="4s" repeatCount="indefinite"/>
  </rect>

  <!-- Floating particles -->
  <circle cx="60"  cy="60"  r="2" fill="#FF8C00" opacity="0.7"><animate attributeName="cy" values="60;30;60"   dur="3.2s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.7;0.1;0.7" dur="3.2s" repeatCount="indefinite"/></circle>
  <circle cx="150" cy="200" r="1.5" fill="#FFA040" opacity="0.5"><animate attributeName="cy" values="200;170;200" dur="4.1s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="4.1s" repeatCount="indefinite"/></circle>
  <circle cx="820" cy="80"  r="2" fill="#FF8C00" opacity="0.6"><animate attributeName="cy" values="80;50;80"   dur="2.8s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.6;0.1;0.6" dur="2.8s" repeatCount="indefinite"/></circle>
  <circle cx="750" cy="220" r="1.5" fill="#FFBE7A" opacity="0.5"><animate attributeName="cy" values="220;190;220" dur="3.7s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="3.7s" repeatCount="indefinite"/></circle>
  <circle cx="400" cy="30"  r="1.5" fill="#FF6B35" opacity="0.4"><animate attributeName="cy" values="30;10;30"   dur="5s"   repeatCount="indefinite"/><animate attributeName="opacity" values="0.4;0.0;0.4" dur="5s"   repeatCount="indefinite"/></circle>
  <circle cx="500" cy="260" r="2"   fill="#FF8C00" opacity="0.5"><animate attributeName="cy" values="260;230;260" dur="4.4s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="4.4s" repeatCount="indefinite"/></circle>
  <circle cx="200" cy="140" r="1"   fill="#FFA040" opacity="0.3"><animate attributeName="cx" values="200;220;200" dur="6s"   repeatCount="indefinite"/></circle>
  <circle cx="700" cy="140" r="1"   fill="#FFA040" opacity="0.3"><animate attributeName="cx" values="700;680;700" dur="5.5s" repeatCount="indefinite"/></circle>

  <!-- Corner accent brackets -->
  <g stroke="#FF8C00" stroke-width="2" fill="none" stroke-opacity="0.8">
    <polyline points="12,35 12,12 35,12"/>
    <polyline points="865,12 888,12 888,35"/>
    <polyline points="12,245 12,268 35,268"/>
    <polyline points="865,268 888,268 888,245"/>
  </g>

  <!-- Pulsing corner dots -->
  <circle cx="12" cy="12" r="3" fill="#FF8C00">
    <animate attributeName="r" values="3;6;3" dur="2s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="2s" repeatCount="indefinite"/>
  </circle>
  <circle cx="888" cy="12" r="3" fill="#FF8C00">
    <animate attributeName="r" values="3;6;3" dur="2s" begin="0.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="2s" begin="0.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="12" cy="268" r="3" fill="#FF8C00">
    <animate attributeName="r" values="3;6;3" dur="2s" begin="1s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="2s" begin="1s" repeatCount="indefinite"/>
  </circle>
  <circle cx="888" cy="268" r="3" fill="#FF8C00">
    <animate attributeName="r" values="3;6;3" dur="2s" begin="1.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="2s" begin="1.5s" repeatCount="indefinite"/>
  </circle>

  <!-- Orange underline bar that pulses -->
  <rect x="270" y="155" width="360" height="3" rx="2" fill="#FF8C00">
    <animate attributeName="opacity" values="1;0.3;1" dur="2.5s" repeatCount="indefinite"/>
    <animate attributeName="width" values="360;300;360" dur="2.5s" repeatCount="indefinite"/>
    <animate attributeName="x" values="270;300;270" dur="2.5s" repeatCount="indefinite"/>
  </rect>

  <!-- AKSHAT — main title with glow pulse -->
  <text x="450" y="138" font-family="'Courier New', monospace" font-size="78" font-weight="900"
        fill="#FF8C00" text-anchor="middle" filter="url(#glow)" letter-spacing="18">
    AKSHAT
    <animate attributeName="opacity" values="1;0.75;1" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- Subtitle -->
  <text x="450" y="185" font-family="'Courier New', monospace" font-size="14" font-weight="400"
        fill="#FFBE7A" text-anchor="middle" letter-spacing="4" opacity="0.9">
    BUILDER  ·  FOUNDER  ·  AI ENGINEER  ·  FL1CKfps
  </text>

  <!-- Bottom tagline with fade in/out -->
  <text x="450" y="230" font-family="'Courier New', monospace" font-size="12"
        fill="#888" text-anchor="middle" letter-spacing="2">
    &lt; shipping real stuff from Delhi 🇮🇳 /&gt;
    <animate attributeName="opacity" values="0.5;1;0.5" dur="4s" repeatCount="indefinite"/>
  </text>
</svg>

<!-- ============================================================
     TYPING SVG + BADGES
     ============================================================ -->

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=22&duration=2500&pause=700&color=FF8C00&center=true&vCenter=true&width=800&height=50&lines=Founder+%40+ELV8+Studios+%F0%9F%9A%80;AI+Agents+%7C+Voice+Bots+%7C+Automations+%F0%9F%A4%96;Flutter+%E2%80%A2+Kotlin+%E2%80%A2+React+%E2%80%A2+Next.js;Building+things+that+make+money+%F0%9F%94%A5;Shipping+from+Delhi+%E2%80%94+zero+excuses+%E2%9A%A1" alt="Typing"/>

<br/>

![Views](https://komarev.com/ghpvc/?username=FL1CKfps&color=FF8C00&style=for-the-badge&label=PROFILE+VIEWS)
[![ELV8](https://img.shields.io/badge/🔥_ELV8_Studios-elv8.codes-FF8C00?style=for-the-badge)](https://elv8.codes)
[![TrendJackr](https://img.shields.io/badge/🤖_TrendJackr_AI-LIVE-FF4500?style=for-the-badge)](https://trendjackr.elv8.codes)
[![YouTube](https://img.shields.io/badge/▶_Zenith_Synapse-FF8C00?style=for-the-badge&logo=youtube&logoColor=black)](https://youtube.com/@zenithsynapse)
[![Mail](https://img.shields.io/badge/📩_akshatdubey.business%40gmail.com-0D1117?style=for-the-badge)](mailto:akshatdubey.business@gmail.com)

</div>

---

<!-- ============================================================
     WHOAMI SECTION
     ============================================================ -->

<img align="right" width="260" src="https://media.giphy.com/media/L8K62iTDkzGX6/giphy.gif"/>

### `> whoami`

```ts
const akshat = {
  alias      : "FL1CKfps",
  age        : 18,
  roles      : ["Founder", "AI Engineer", "Full-Stack Dev"],
  companies  : ["ELV8 Studios 🔥", "Elevate Codes 🤖"],
  location   : "Delhi, India 🇮🇳",
  youtube    : "@zenithsynapse",
  email      : "akshatdubey.business@gmail.com",
  mindset    : "build → ship → scale",
  notHereFor : "learning for learning's sake"
};
```

> I don't want to be *good at coding.*
> I want to **build something big, visible, and valuable.**

- 🏗️ Founder — **[ELV8 Studios](https://elv8.codes)** (web · app · AI agency)
- 🤖 Founder — **Elevate Codes** (AI automations agency)
- 🔥 Shipped **[TrendJackr AI](https://trendjackr.elv8.codes)** — live SaaS with real users
- 📱 Production apps in **Flutter + Kotlin**
- ⚡ 18 years old. Zero excuses. Full send.

<br clear="right"/>

---

<!-- ============================================================
     AI SUPERPOWERS — animated SVG showcase
     ============================================================ -->

<div align="center">

<!-- AI SECTION BANNER SVG -->
<svg width="860" height="70" viewBox="0 0 860 70" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="aibg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#0a0a0a"/>
      <stop offset="40%"  stop-color="#1f0d00"/>
      <stop offset="100%" stop-color="#0a0a0a"/>
    </linearGradient>
    <filter id="ag">
      <feGaussianBlur stdDeviation="4" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>
  <rect width="860" height="70" fill="url(#aibg)" rx="8"/>
  <rect x="0" y="0" width="4" height="70" fill="#FF8C00" rx="2">
    <animate attributeName="opacity" values="1;0.3;1" dur="1.8s" repeatCount="indefinite"/>
  </rect>
  <rect x="856" y="0" width="4" height="70" fill="#FF8C00" rx="2">
    <animate attributeName="opacity" values="1;0.3;1" dur="1.8s" begin="0.9s" repeatCount="indefinite"/>
  </rect>
  <text x="430" y="28" font-family="'Courier New',monospace" font-size="11" fill="#FF8C00" text-anchor="middle" letter-spacing="6" opacity="0.7">sudo apt install</text>
  <text x="430" y="55" font-family="'Courier New',monospace" font-size="26" font-weight="900" fill="#FF8C00" text-anchor="middle" filter="url(#ag)" letter-spacing="8">
    AI SUPERPOWERS
    <animate attributeName="opacity" values="1;0.6;1" dur="3s" repeatCount="indefinite"/>
  </text>
</svg>

</div>

<br/>

> **AI isn't a tool I use. It's the layer everything runs on.**

<!-- ============================================================
     AI SKILLS — animated radar/orbit SVG
     ============================================================ -->

<div align="center">

<svg width="860" height="340" viewBox="0 0 860 340" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="cb" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%"  stop-color="#0d0d0d"/>
      <stop offset="100%" stop-color="#130800"/>
    </linearGradient>
    <filter id="cg">
      <feGaussianBlur stdDeviation="3" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>
  <rect width="860" height="340" fill="url(#cb)" rx="12"/>

  <!-- Central AI orb -->
  <circle cx="155" cy="170" r="55" fill="none" stroke="#FF8C00" stroke-width="1.5" stroke-opacity="0.3">
    <animate attributeName="r" values="55;65;55" dur="3s" repeatCount="indefinite"/>
    <animate attributeName="stroke-opacity" values="0.3;0.1;0.3" dur="3s" repeatCount="indefinite"/>
  </circle>
  <circle cx="155" cy="170" r="38" fill="none" stroke="#FFA040" stroke-width="1" stroke-opacity="0.5">
    <animate attributeName="r" values="38;44;38" dur="2.2s" repeatCount="indefinite"/>
  </circle>
  <circle cx="155" cy="170" r="22" fill="#1f0d00" stroke="#FF8C00" stroke-width="2">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="1.5s" repeatCount="indefinite"/>
  </circle>
  <text x="155" y="165" font-family="'Courier New',monospace" font-size="9" fill="#FF8C00" text-anchor="middle" font-weight="bold">AKSHAT</text>
  <text x="155" y="178" font-family="'Courier New',monospace" font-size="8" fill="#FFA040" text-anchor="middle">AI CORE</text>

  <!-- Orbiting dot -->
  <circle cx="155" cy="115" r="5" fill="#FF8C00" filter="url(#cg)">
    <animateTransform attributeName="transform" type="rotate" from="0 155 170" to="360 155 170" dur="4s" repeatCount="indefinite"/>
  </circle>
  <circle cx="155" cy="225" r="3" fill="#FFA040" filter="url(#cg)">
    <animateTransform attributeName="transform" type="rotate" from="180 155 170" to="540 155 170" dur="6s" repeatCount="indefinite"/>
  </circle>

  <!-- Connector lines from orb to cards -->
  <line x1="210" y1="155" x2="295" y2="80"  stroke="#FF8C00" stroke-opacity="0.25" stroke-width="1" stroke-dasharray="4 3"/>
  <line x1="210" y1="162" x2="295" y2="155" stroke="#FF8C00" stroke-opacity="0.25" stroke-width="1" stroke-dasharray="4 3"/>
  <line x1="210" y1="170" x2="295" y2="230" stroke="#FF8C00" stroke-opacity="0.25" stroke-width="1" stroke-dasharray="4 3"/>
  <line x1="210" y1="180" x2="295" y2="295" stroke="#FF8C00" stroke-opacity="0.25" stroke-width="1" stroke-dasharray="4 3"/>

  <!-- AI SKILL CARDS — left column -->
  <!-- Card 1: AI Calling Agents -->
  <rect x="295" y="18" width="250" height="72" rx="8" fill="#0f0f0f" stroke="#FF8C00" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="2.8s" repeatCount="indefinite"/>
  </rect>
  <text x="315" y="42" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FF8C00">🧠 AI Calling Agents</text>
  <text x="315" y="58" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Voice agents that call, qualify &amp; book.</text>
  <text x="315" y="72" font-family="'Courier New',monospace" font-size="10" fill="#666">No human needed. Fully automated.</text>
  <rect x="295" y="18" width="4" height="72" rx="2" fill="#FF8C00"/>

  <!-- Card 2: Workflow Automations -->
  <rect x="295" y="107" width="250" height="72" rx="8" fill="#0f0f0f" stroke="#FFA040" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="3.2s" begin="0.4s" repeatCount="indefinite"/>
  </rect>
  <text x="315" y="131" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFA040">🔄 AI Automations</text>
  <text x="315" y="147" font-family="'Courier New',monospace" font-size="10" fill="#aaa">n8n · Make · Zapier + custom LLM</text>
  <text x="315" y="161" font-family="'Courier New',monospace" font-size="10" fill="#666">Sold via Elevate Codes agency.</text>
  <rect x="295" y="107" width="4" height="72" rx="2" fill="#FFA040"/>

  <!-- Card 3: RAG + Agentic -->
  <rect x="295" y="196" width="250" height="72" rx="8" fill="#0f0f0f" stroke="#FFBE7A" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="2.5s" begin="0.8s" repeatCount="indefinite"/>
  </rect>
  <text x="315" y="220" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFBE7A">🔍 RAG + Agentic AI</text>
  <text x="315" y="236" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Multi-step agents with memory &amp; goals.</text>
  <text x="315" y="250" font-family="'Courier New',monospace" font-size="10" fill="#666">Not just chatbots — actual agents.</text>
  <rect x="295" y="196" width="4" height="72" rx="2" fill="#FFBE7A"/>

  <!-- Card 4: WhatsApp Bots -->
  <rect x="295" y="285" width="250" height="42" rx="8" fill="#0f0f0f" stroke="#FF6B35" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="3.8s" begin="1s" repeatCount="indefinite"/>
  </rect>
  <text x="315" y="309" font-family="'Courier New',monospace" font-size="12" font-weight="bold" fill="#FF6B35">💬 WhatsApp AI Bots → lead funnels</text>
  <rect x="295" y="285" width="4" height="42" rx="2" fill="#FF6B35"/>

  <!-- Connector lines right column -->
  <line x1="555" y1="100" x2="565" y2="54"  stroke="#FF8C00" stroke-opacity="0.2" stroke-width="1" stroke-dasharray="3 3"/>
  <line x1="555" y1="145" x2="565" y2="143" stroke="#FF8C00" stroke-opacity="0.2" stroke-width="1" stroke-dasharray="3 3"/>
  <line x1="555" y1="230" x2="565" y2="232" stroke="#FF8C00" stroke-opacity="0.2" stroke-width="1" stroke-dasharray="3 3"/>

  <!-- Right column cards -->
  <!-- Card 5: Voice AI -->
  <rect x="565" y="18" width="272" height="72" rx="8" fill="#0f0f0f" stroke="#FF8C00" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="2.1s" begin="0.2s" repeatCount="indefinite"/>
  </rect>
  <text x="585" y="42" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FF8C00">🗣️ Voice AI Agents</text>
  <text x="585" y="58" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Gemini Live API + ElevenLabs.</text>
  <text x="585" y="72" font-family="'Courier New',monospace" font-size="10" fill="#666">Real-time. Human-sounding. Production.</text>
  <rect x="565" y="18" width="4" height="72" rx="2" fill="#FF8C00"/>

  <!-- Card 6: SaaS / TrendJackr -->
  <rect x="565" y="107" width="272" height="72" rx="8" fill="#0f0f0f" stroke="#FFA040" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="2.9s" begin="0.6s" repeatCount="indefinite"/>
  </rect>
  <text x="585" y="131" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFA040">🌐 AI SaaS — TrendJackr</text>
  <text x="585" y="147" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Trend → viral content. Gemini + Pollinations.</text>
  <text x="585" y="161" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">→ trendjackr.elv8.codes  🟢 LIVE</text>
  <rect x="565" y="107" width="4" height="72" rx="2" fill="#FFA040"/>

  <!-- Card 7: JARVIS + local AI -->
  <rect x="565" y="196" width="272" height="72" rx="8" fill="#0f0f0f" stroke="#FFBE7A" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="3.5s" begin="1.2s" repeatCount="indefinite"/>
  </rect>
  <text x="585" y="220" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFBE7A">🏠 JARVIS — Local AI</text>
  <text x="585" y="236" font-family="'Courier New',monospace" font-size="10" fill="#aaa">FastAPI + Claude API + Flutter controller</text>
  <text x="585" y="250" font-family="'Courier New',monospace" font-size="10" fill="#666">On my own PC. On my own network.</text>
  <rect x="565" y="196" width="4" height="72" rx="2" fill="#FFBE7A"/>

  <!-- Card 8: Harit -->
  <rect x="565" y="285" width="272" height="42" rx="8" fill="#0f0f0f" stroke="#FF6B35" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.4;1" dur="4s" begin="0.3s" repeatCount="indefinite"/>
  </rect>
  <text x="585" y="309" font-family="'Courier New',monospace" font-size="12" font-weight="bold" fill="#FF6B35">🌱 Harit → AI farmer assistant, regional langs</text>
  <rect x="565" y="285" width="4" height="42" rx="2" fill="#FF6B35"/>
</svg>

</div>

<!-- AI Badge Row -->
<div align="center">

![Gemini](https://img.shields.io/badge/Gemini_2.5_Flash-FF8C00?style=for-the-badge&logo=google&logoColor=black)
![Claude](https://img.shields.io/badge/Claude_API-0D1117?style=for-the-badge&logo=anthropic&logoColor=FFA040)
![OpenAI](https://img.shields.io/badge/OpenAI_API-0D1117?style=for-the-badge&logo=openai&logoColor=FF8C00)
![LangChain](https://img.shields.io/badge/LangChain-FF8C00?style=for-the-badge)
![n8n](https://img.shields.io/badge/n8n-0D1117?style=for-the-badge&logo=n8n&logoColor=FFA040)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-FF4500?style=for-the-badge)
![Pollinations](https://img.shields.io/badge/Pollinations_AI-FFBE7A?style=for-the-badge&logoColor=black)
![WhatsApp](https://img.shields.io/badge/WhatsApp_Cloud_API-0D1117?style=for-the-badge&logo=whatsapp&logoColor=FF8C00)

</div>

---

## `> pip list && npm list` 💻

<!-- ============================================================
     TECH STACK — animated skill bars SVG
     ============================================================ -->

<div align="center">

<svg width="860" height="420" viewBox="0 0 860 420" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="sb" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#FF8C00"/>
      <stop offset="100%" stop-color="#FF4500"/>
    </linearGradient>
    <linearGradient id="sb2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#FFA040"/>
      <stop offset="100%" stop-color="#FF8C00"/>
    </linearGradient>
    <linearGradient id="sb3" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#FFBE7A"/>
      <stop offset="100%" stop-color="#FFA040"/>
    </linearGradient>
    <linearGradient id="sb4" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#FF6B35"/>
      <stop offset="100%" stop-color="#FF8C00"/>
    </linearGradient>
  </defs>
  <rect width="860" height="420" fill="#0d0d0d" rx="12"/>

  <!-- Column headers -->
  <text x="30"  y="30" font-family="'Courier New',monospace" font-size="11" fill="#FF8C00" font-weight="bold" letter-spacing="3">MOBILE</text>
  <text x="460" y="30" font-family="'Courier New',monospace" font-size="11" fill="#FFA040" font-weight="bold" letter-spacing="3">FRONTEND</text>

  <!-- LEFT COLUMN: Mobile -->
  <!-- Flutter -->
  <text x="30" y="58" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Flutter</text>
  <rect x="30" y="64" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="64" width="0"   height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="355" dur="1.5s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="74" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">93%</text>

  <!-- Kotlin -->
  <text x="30" y="96" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Kotlin</text>
  <rect x="30" y="102" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="102" width="0"  height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="323" dur="1.6s" begin="0.1s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="112" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">85%</text>

  <!-- Dart -->
  <text x="30" y="134" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Dart</text>
  <rect x="30" y="140" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="140" width="0"  height="10" rx="5" fill="url(#sb2)">
    <animate attributeName="width" from="0" to="342" dur="1.7s" begin="0.2s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="150" font-family="'Courier New',monospace" font-size="10" fill="#FFA040">90%</text>

  <!-- React Native -->
  <text x="30" y="172" font-family="'Courier New',monospace" font-size="12" fill="#ccc">React Native</text>
  <rect x="30" y="178" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="178" width="0"  height="10" rx="5" fill="url(#sb2)">
    <animate attributeName="width" from="0" to="304" dur="1.8s" begin="0.3s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="188" font-family="'Courier New',monospace" font-size="10" fill="#FFA040">80%</text>

  <!-- Divider -->
  <text x="30"  y="225" font-family="'Courier New',monospace" font-size="11" fill="#FF6B35" font-weight="bold" letter-spacing="3">BACKEND</text>

  <!-- Node.js -->
  <text x="30" y="248" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Node.js</text>
  <rect x="30" y="254" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="254" width="0"  height="10" rx="5" fill="url(#sb4)">
    <animate attributeName="width" from="0" to="342" dur="1.5s" begin="0.4s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="264" font-family="'Courier New',monospace" font-size="10" fill="#FF6B35">90%</text>

  <!-- FastAPI / Python -->
  <text x="30" y="286" font-family="'Courier New',monospace" font-size="12" fill="#ccc">FastAPI / Python</text>
  <rect x="30" y="292" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="292" width="0"  height="10" rx="5" fill="url(#sb4)">
    <animate attributeName="width" from="0" to="323" dur="1.6s" begin="0.5s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="302" font-family="'Courier New',monospace" font-size="10" fill="#FF6B35">85%</text>

  <!-- Firebase -->
  <text x="30" y="324" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Firebase</text>
  <rect x="30" y="330" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="330" width="0"  height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="361" dur="1.7s" begin="0.6s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="340" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">95%</text>

  <!-- Supabase -->
  <text x="30" y="362" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Supabase</text>
  <rect x="30" y="368" width="380" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="30" y="368" width="0"  height="10" rx="5" fill="url(#sb2)">
    <animate attributeName="width" from="0" to="304" dur="1.8s" begin="0.7s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="395" y="378" font-family="'Courier New',monospace" font-size="10" fill="#FFA040">80%</text>

  <!-- RIGHT COLUMN: Frontend -->
  <!-- React -->
  <text x="460" y="58" font-family="'Courier New',monospace" font-size="12" fill="#ccc">React</text>
  <rect x="460" y="64" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="64" width="0"   height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="352" dur="1.5s" begin="0.15s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="74" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">95%</text>

  <!-- Next.js -->
  <text x="460" y="96" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Next.js</text>
  <rect x="460" y="102" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="102" width="0"  height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="333" dur="1.6s" begin="0.25s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="112" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">90%</text>

  <!-- TypeScript -->
  <text x="460" y="134" font-family="'Courier New',monospace" font-size="12" fill="#ccc">TypeScript</text>
  <rect x="460" y="140" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="140" width="0"  height="10" rx="5" fill="url(#sb2)">
    <animate attributeName="width" from="0" to="315" dur="1.7s" begin="0.35s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="150" font-family="'Courier New',monospace" font-size="10" fill="#FFA040">85%</text>

  <!-- Tailwind -->
  <text x="460" y="172" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Tailwind CSS</text>
  <rect x="460" y="178" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="178" width="0"  height="10" rx="5" fill="url(#sb3)">
    <animate attributeName="width" from="0" to="352" dur="1.8s" begin="0.45s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="188" font-family="'Courier New',monospace" font-size="10" fill="#FFBE7A">95%</text>

  <!-- AI section right -->
  <text x="460" y="225" font-family="'Courier New',monospace" font-size="11" fill="#FFBE7A" font-weight="bold" letter-spacing="3">AI / LLM</text>

  <!-- Gemini API -->
  <text x="460" y="248" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Gemini 2.5 API</text>
  <rect x="460" y="254" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="254" width="0"  height="10" rx="5" fill="url(#sb)">
    <animate attributeName="width" from="0" to="352" dur="1.5s" begin="0.55s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="264" font-family="'Courier New',monospace" font-size="10" fill="#FF8C00">95%</text>

  <!-- Claude API -->
  <text x="460" y="286" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Claude API</text>
  <rect x="460" y="292" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="292" width="0"  height="10" rx="5" fill="url(#sb2)">
    <animate attributeName="width" from="0" to="333" dur="1.6s" begin="0.65s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="302" font-family="'Courier New',monospace" font-size="10" fill="#FFA040">90%</text>

  <!-- n8n Automations -->
  <text x="460" y="324" font-family="'Courier New',monospace" font-size="12" fill="#ccc">n8n / Make Automations</text>
  <rect x="460" y="330" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="330" width="0"  height="10" rx="5" fill="url(#sb3)">
    <animate attributeName="width" from="0" to="315" dur="1.7s" begin="0.75s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="340" font-family="'Courier New',monospace" font-size="10" fill="#FFBE7A">85%</text>

  <!-- Voice AI -->
  <text x="460" y="362" font-family="'Courier New',monospace" font-size="12" fill="#ccc">Voice AI (ElevenLabs)</text>
  <rect x="460" y="368" width="370" height="10" rx="5" fill="#1a1a1a"/>
  <rect x="460" y="368" width="0"  height="10" rx="5" fill="url(#sb4)">
    <animate attributeName="width" from="0" to="296" dur="1.8s" begin="0.85s" fill="freeze" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </rect>
  <text x="825" y="378" font-family="'Courier New',monospace" font-size="10" fill="#FF6B35">80%</text>

  <!-- Center divider -->
  <line x1="440" y1="20" x2="440" y2="400" stroke="#FF8C00" stroke-opacity="0.12" stroke-width="1" stroke-dasharray="4 4"/>
</svg>

</div>

---

## `> ls -la ./projects` 🚀

<!-- ============================================================
     PROJECTS — animated card grid SVG
     ============================================================ -->

<div align="center">

<svg width="860" height="310" viewBox="0 0 860 310" xmlns="http://www.w3.org/2000/svg">
  <rect width="860" height="310" fill="#0d0d0d" rx="12"/>

  <!-- Project Card 1: ELV8 Studios -->
  <rect x="15" y="15" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FF8C00" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <rect x="15" y="15" width="260" height="5" rx="3" fill="#FF8C00"/>
  <text x="35" y="45" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FF8C00">🔥 ELV8 Studios</text>
  <text x="35" y="63" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Web · App · AI Agency</text>
  <text x="35" y="79" font-family="'Courier New',monospace" font-size="9"  fill="#666">Next.js · React · Flutter</text>
  <rect x="35" y="110" width="50" height="18" rx="9" fill="#FF8C00"/>
  <text x="60" y="123" font-family="'Courier New',monospace" font-size="9" fill="#000" text-anchor="middle" font-weight="bold">LIVE 🟢</text>

  <!-- Project Card 2: TrendJackr AI -->
  <rect x="300" y="15" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FFA040" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="3s" begin="0.3s" repeatCount="indefinite"/>
  </rect>
  <rect x="300" y="15" width="260" height="5" rx="3" fill="#FFA040"/>
  <text x="320" y="45" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFA040">🤖 TrendJackr AI</text>
  <text x="320" y="63" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Trend → viral content SaaS</text>
  <text x="320" y="79" font-family="'Courier New',monospace" font-size="9"  fill="#666">Next.js · Gemini · Pollinations</text>
  <rect x="320" y="110" width="50" height="18" rx="9" fill="#FFA040"/>
  <text x="345" y="123" font-family="'Courier New',monospace" font-size="9" fill="#000" text-anchor="middle" font-weight="bold">LIVE 🟢</text>

  <!-- Project Card 3: CrisisOS -->
  <rect x="585" y="15" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FFBE7A" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="2.8s" begin="0.6s" repeatCount="indefinite"/>
  </rect>
  <rect x="585" y="15" width="260" height="5" rx="3" fill="#FFBE7A"/>
  <text x="605" y="45" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFBE7A">🆘 CrisisOS</text>
  <text x="605" y="63" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Offline survival — NIT Delhi</text>
  <text x="605" y="79" font-family="'Courier New',monospace" font-size="9"  fill="#666">Kotlin · BLE Mesh · AI</text>
  <rect x="605" y="110" width="80" height="18" rx="9" fill="#FFBE7A"/>
  <text x="645" y="123" font-family="'Courier New',monospace" font-size="9" fill="#000" text-anchor="middle" font-weight="bold">🏆 HACKATHON</text>

  <!-- Project Card 4: JARVIS -->
  <rect x="15" y="165" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FF6B35" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="3.5s" begin="0.9s" repeatCount="indefinite"/>
  </rect>
  <rect x="15" y="165" width="260" height="5" rx="3" fill="#FF6B35"/>
  <text x="35" y="195" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FF6B35">🏠 JARVIS</text>
  <text x="35" y="213" font-family="'Courier New',monospace" font-size="10" fill="#aaa">Local AI assistant on my PC</text>
  <text x="35" y="229" font-family="'Courier New',monospace" font-size="9"  fill="#666">FastAPI · Claude · Flutter</text>
  <rect x="35" y="260" width="70" height="18" rx="9" fill="#FF6B35"/>
  <text x="70" y="273" font-family="'Courier New',monospace" font-size="9" fill="#fff" text-anchor="middle" font-weight="bold">✅ SHIPPED</text>

  <!-- Project Card 5: Relay -->
  <rect x="300" y="165" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FF8C00" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="2.2s" begin="1.2s" repeatCount="indefinite"/>
  </rect>
  <rect x="300" y="165" width="260" height="5" rx="3" fill="#FF8C00"/>
  <text x="320" y="195" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FF8C00">📡 Relay</text>
  <text x="320" y="213" font-family="'Courier New',monospace" font-size="10" fill="#aaa">BLE mesh offline chat app</text>
  <text x="320" y="229" font-family="'Courier New',monospace" font-size="9"  fill="#666">Flutter · Dart · BLE Peripheral</text>
  <rect x="320" y="260" width="110" height="18" rx="9" fill="#FF8C00"/>
  <text x="375" y="273" font-family="'Courier New',monospace" font-size="9" fill="#000" text-anchor="middle" font-weight="bold">🏆 TOP 10 @ TRAE</text>

  <!-- Project Card 6: Harit + Voxo -->
  <rect x="585" y="165" width="260" height="130" rx="10" fill="#0f0f0f" stroke="#FFA040" stroke-width="1.5">
    <animate attributeName="stroke-opacity" values="1;0.3;1" dur="4s" begin="1.5s" repeatCount="indefinite"/>
  </rect>
  <rect x="585" y="165" width="260" height="5" rx="3" fill="#FFA040"/>
  <text x="605" y="195" font-family="'Courier New',monospace" font-size="13" font-weight="bold" fill="#FFA040">🌱 Harit  +  📱 Voxo</text>
  <text x="605" y="213" font-family="'Courier New',monospace" font-size="10" fill="#aaa">AI farmer · Sub manager</text>
  <text x="605" y="229" font-family="'Courier New',monospace" font-size="9"  fill="#666">Gemini · Voice · Flutter · Firebase</text>
  <rect x="605" y="260" width="80" height="18" rx="9" fill="#333"/>
  <text x="645" y="273" font-family="'Courier New',monospace" font-size="9" fill="#FFA040" text-anchor="middle" font-weight="bold">🔨 BUILDING</text>
</svg>

</div>

---

## `> cat ./clients.log` 🌐

> Real clients. Real delivery. Real revenue.

<div align="center">

<!-- ============================================================
     CLIENTS — animated marquee ticker SVG
     ============================================================ -->

<svg width="860" height="55" viewBox="0 0 860 55" xmlns="http://www.w3.org/2000/svg">
  <rect width="860" height="55" fill="#0d0d0d" rx="8"/>
  <rect x="0" y="0" width="4" height="55" fill="#FF8C00"/>
  <rect x="856" y="0" width="4" height="55" fill="#FF8C00"/>

  <!-- Scrolling client ticker -->
  <text font-family="'Courier New',monospace" font-size="13" fill="#FF8C00" font-weight="bold" y="33">
    <textPath href="#ticker-path">
      ☕ Mokai Cafe  ·  🧃 Juice Joint  ·  🎓 Tips Coaching  ·  🍽️ Perilicious  ·  🏢 Harmony Residences  ·  ⚡ Kryptronix  ·  🚀 Zyron  ·  🪑 Desire Furnitures (Canada)  ·  ☕ Mokai Cafe  ·  🧃 Juice Joint  ·  🎓 Tips Coaching  ·  🍽️ Perilicious  ·  🏢 Harmony Residences  ·
      <animate attributeName="startOffset" from="0%" to="-100%" dur="20s" repeatCount="indefinite"/>
    </textPath>
  </text>
  <defs>
    <path id="ticker-path" d="M 20 0 L 1800 0"/>
  </defs>
</svg>

</div>

Clients across **India 🇮🇳 + Canada 🇨🇦** — cafes, institutes, residences, tech startups & international brands.

---

## `> git log --all --stat` 📈

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=FL1CKfps&show_icons=true&theme=dark&bg_color=0D1117&title_color=FF8C00&icon_color=FFA040&text_color=ffffff&border_color=FF8C00&border_radius=12&include_all_commits=true&count_private=true"/>
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=FL1CKfps&layout=compact&theme=dark&bg_color=0D1117&title_color=FF8C00&text_color=ffffff&border_color=FF8C00&border_radius=12&langs_count=10"/>

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com?user=FL1CKfps&theme=dark&background=0D1117&ring=FF8C00&fire=FFA040&currStreakLabel=FFBE7A&sideLabels=FF8C00&border=FF8C00&stroke=FF8C00&dates=888888" width="60%"/>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=FL1CKfps&bg_color=0D1117&color=FFA040&line=FF8C00&point=FFBE7A&area=true&border_color=FF8C00" width="95%"/>

<br/>

<img src="https://github-profile-trophy.vercel.app/?username=FL1CKfps&theme=darkhub&no-frame=true&margin-w=10&column=7"/>

</div>

---

## `> echo $PHILOSOPHY` 🧠

<div align="center">

<!-- ============================================================
     PHILOSOPHY — animated terminal SVG
     ============================================================ -->

<svg width="860" height="185" viewBox="0 0 860 185" xmlns="http://www.w3.org/2000/svg">
  <rect width="860" height="185" fill="#0a0a0a" rx="12" stroke="#FF8C00" stroke-width="1.5"/>
  <!-- Terminal title bar -->
  <rect width="860" height="32" fill="#151515" rx="12"/>
  <rect width="860" height="16" y="16" fill="#151515"/>
  <circle cx="22" cy="16" r="6" fill="#FF4500"/>
  <circle cx="42" cy="16" r="6" fill="#FF8C00"/>
  <circle cx="62" cy="16" r="6" fill="#FFBE7A"/>
  <text x="430" y="21" font-family="'Courier New',monospace" font-size="11" fill="#666" text-anchor="middle">akshat@elv8 ~ zsh</text>

  <!-- Terminal lines with staggered fade-in -->
  <text x="30" y="60"  font-family="'Courier New',monospace" font-size="13" fill="#FF8C00" opacity="0"><tspan fill="#FF4500">❯</tspan>  Tech  ×  Business  ×  Design  ×  AI  =  ELV8<animate attributeName="opacity" values="0;1" dur="0.3s" begin="0.3s" fill="freeze"/></text>
  <text x="30" y="84"  font-family="'Courier New',monospace" font-size="13" fill="#aaa"     opacity="0">  Impact  &gt;  learning for learning's sake<animate attributeName="opacity" values="0;1" dur="0.3s" begin="0.8s" fill="freeze"/></text>
  <text x="30" y="106" font-family="'Courier New',monospace" font-size="13" fill="#aaa"     opacity="0">  Distribution  &gt;  just building cool things<animate attributeName="opacity" values="0;1" dur="0.3s" begin="1.2s" fill="freeze"/></text>
  <text x="30" y="128" font-family="'Courier New',monospace" font-size="13" fill="#aaa"     opacity="0">  Shipping  &gt;  perfecting in silence<animate attributeName="opacity" values="0;1" dur="0.3s" begin="1.6s" fill="freeze"/></text>
  <text x="30" y="150" font-family="'Courier New',monospace" font-size="13" fill="#FFA040"  opacity="0">  Agents  &gt;  Apps<animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.0s" fill="freeze"/></text>
  <text x="30" y="172" font-family="'Courier New',monospace" font-size="12" fill="#555"     opacity="0">  "build something big, visible, and valuable." — akshat<animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.4s" fill="freeze"/></text>

  <!-- Blinking cursor -->
  <rect x="30" y="158" width="9" height="16" fill="#FF8C00" rx="1">
    <animate attributeName="opacity" values="1;0;1" dur="1s" begin="2.7s" repeatCount="indefinite"/>
  </rect>
</svg>

</div>

---

## `> top -pid akshat` ⚡

```
🔨  Building  →  Harit AI + Voxo + new agency clients
📹  Creating  →  Zenith Synapse (Indian tech market)
🤖  Shipping  →  AI automations via Elevate Codes
📚  Teaching  →  Class 12 CS + Class 8 Science
🚀  Exploring →  IoT · Robotics · Radio Astronomy · Home Servers
```

---

<div align="center">

*If you're building something bold — let's talk.*

[![Email](https://img.shields.io/badge/📩_akshatdubey.business%40gmail.com-FF8C00?style=for-the-badge)](mailto:akshatdubey.business@gmail.com)
[![ELV8](https://img.shields.io/badge/🔥_elv8.codes-0D1117?style=for-the-badge)](https://elv8.codes)
[![TrendJackr](https://img.shields.io/badge/🤖_trendjackr.elv8.codes-0D1117?style=for-the-badge)](https://trendjackr.elv8.codes)

<br/>

<!-- FOOTER WAVE -->
<svg width="860" height="80" viewBox="0 0 860 80" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#FF4500"/>
      <stop offset="50%"  stop-color="#FF8C00"/>
      <stop offset="100%" stop-color="#FFBE7A"/>
    </linearGradient>
  </defs>
  <path d="M0,40 Q107,10 215,40 Q322,70 430,40 Q537,10 645,40 Q752,70 860,40 L860,80 L0,80 Z" fill="url(#wg)" opacity="0.15">
    <animate attributeName="d" values="M0,40 Q107,10 215,40 Q322,70 430,40 Q537,10 645,40 Q752,70 860,40 L860,80 L0,80 Z;M0,50 Q107,20 215,50 Q322,80 430,50 Q537,20 645,50 Q752,80 860,50 L860,80 L0,80 Z;M0,40 Q107,10 215,40 Q322,70 430,40 Q537,10 645,40 Q752,70 860,40 L860,80 L0,80 Z" dur="4s" repeatCount="indefinite"/>
  </path>
  <path d="M0,50 Q107,20 215,50 Q322,80 430,50 Q537,20 645,50 Q752,80 860,50 L860,80 L0,80 Z" fill="url(#wg)" opacity="0.25">
    <animate attributeName="d" values="M0,50 Q107,20 215,50 Q322,80 430,50 Q537,20 645,50 Q752,80 860,50 L860,80 L0,80 Z;M0,40 Q107,10 215,40 Q322,70 430,40 Q537,10 645,40 Q752,70 860,40 L860,80 L0,80 Z;M0,50 Q107,20 215,50 Q322,80 430,50 Q537,20 645,50 Q752,80 860,50 L860,80 L0,80 Z" dur="4s" repeatCount="indefinite"/>
  </path>
  <text x="430" y="68" font-family="'Courier New',monospace" font-size="11" fill="#FF8C00" text-anchor="middle" opacity="0.7" letter-spacing="3">BUILT DIFFERENT. SHIPPED REAL.</text>
</svg>

</div>
