<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="300" viewBox="0 0 1200 300">
  <defs>
    <!-- Deep navy background gradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#050d1f"/>
      <stop offset="50%" stop-color="#081528"/>
      <stop offset="100%" stop-color="#0f1c38"/>
    </linearGradient>

    <!-- Ambient glow left (blue) -->
    <radialGradient id="ambLeft" cx="20%" cy="55%" r="45%">
      <stop offset="0%" stop-color="#0e6ba8" stop-opacity="0.45"/>
      <stop offset="100%" stop-color="#050d1f" stop-opacity="0"/>
    </radialGradient>

    <!-- Ambient glow right (cyan) -->
    <radialGradient id="ambRight" cx="80%" cy="40%" r="40%">
      <stop offset="0%" stop-color="#00b4d8" stop-opacity="0.22"/>
      <stop offset="100%" stop-color="#050d1f" stop-opacity="0"/>
    </radialGradient>

    <!-- Orb center glow -->
    <radialGradient id="orbGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.3"/>
      <stop offset="100%" stop-color="#0e6ba8" stop-opacity="0"/>
    </radialGradient>

    <!-- Card inner glow -->
    <radialGradient id="cardGlow" cx="0%" cy="0%" r="100%">
      <stop offset="0%" stop-color="#0e6ba8" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#050d1f" stop-opacity="0"/>
    </radialGradient>

    <!-- Text glow filter -->
    <filter id="textGlow" x="-20%" y="-40%" width="140%" height="180%">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feFlood flood-color="#00d4ff" flood-opacity="0.6" result="col"/>
      <feComposite in="col" in2="blur" operator="in" result="shadow"/>
      <feMerge>
        <feMergeNode in="shadow"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Soft blur filter for glass depth -->
    <filter id="softBlur">
      <feGaussianBlur stdDeviation="2.5"/>
    </filter>

    <!-- Outer glow for orbs -->
    <filter id="orbFilter" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="5" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <style>
    @keyframes pulse {
      0%,100%{opacity:.65}
      50%{opacity:1}
    }
    @keyframes pulse2 {
      0%,100%{opacity:.4}
      50%{opacity:.85}
    }
    @keyframes spin-slow {
      from{transform-origin:950px 148px; transform:rotate(0deg)}
      to{transform-origin:950px 148px; transform:rotate(360deg)}
    }
    @keyframes spin-rev {
      from{transform-origin:950px 148px; transform:rotate(0deg)}
      to{transform-origin:950px 148px; transform:rotate(-360deg)}
    }
    @keyframes float-orb {
      0%,100%{transform:translateY(0)}
      50%{transform:translateY(-6px)}
    }
    @keyframes shimmer {
      0%,100%{opacity:.25}
      50%{opacity:.7}
    }
    @keyframes tag-fade {
      0%,100%{opacity:.7}
      50%{opacity:1}
    }
    .p1{animation:pulse 3s ease-in-out infinite}
    .p2{animation:pulse2 4s ease-in-out infinite}
    .s1{animation:spin-slow 18s linear infinite}
    .s2{animation:spin-rev 12s linear infinite}
    .s3{animation:spin-slow 25s linear infinite}
    .shim{animation:shimmer 3.5s ease-in-out infinite}
    .tag{animation:tag-fade 4s ease-in-out infinite}
  </style>

  <!-- ═══ BACKGROUND ═══ -->
  <rect width="1200" height="300" fill="url(#bgGrad)"/>
  <rect width="1200" height="300" fill="url(#ambLeft)"/>
  <rect width="1200" height="300" fill="url(#ambRight)"/>

  <!-- ═══ TECH GRID ═══ -->
  <g opacity="0.055" stroke="#4fc3f7" stroke-width="0.6">
    <line x1="0" y1="0" x2="1200" y2="0"/>
    <line x1="0" y1="40" x2="1200" y2="40"/>
    <line x1="0" y1="80" x2="1200" y2="80"/>
    <line x1="0" y1="120" x2="1200" y2="120"/>
    <line x1="0" y1="160" x2="1200" y2="160"/>
    <line x1="0" y1="200" x2="1200" y2="200"/>
    <line x1="0" y1="240" x2="1200" y2="240"/>
    <line x1="0" y1="280" x2="1200" y2="280"/>
    <line x1="0" y1="0" x2="0" y2="300"/>
    <line x1="80" y1="0" x2="80" y2="300"/>
    <line x1="160" y1="0" x2="160" y2="300"/>
    <line x1="240" y1="0" x2="240" y2="300"/>
    <line x1="320" y1="0" x2="320" y2="300"/>
    <line x1="400" y1="0" x2="400" y2="300"/>
    <line x1="480" y1="0" x2="480" y2="300"/>
    <line x1="560" y1="0" x2="560" y2="300"/>
    <line x1="640" y1="0" x2="640" y2="300"/>
    <line x1="720" y1="0" x2="720" y2="300"/>
    <line x1="800" y1="0" x2="800" y2="300"/>
    <line x1="880" y1="0" x2="880" y2="300"/>
    <line x1="960" y1="0" x2="960" y2="300"/>
    <line x1="1040" y1="0" x2="1040" y2="300"/>
    <line x1="1120" y1="0" x2="1120" y2="300"/>
    <line x1="1200" y1="0" x2="1200" y2="300"/>
  </g>

  <!-- ═══ DOT PARTICLES (right area) ═══ -->
  <g fill="#4fc3f7">
    <circle cx="780" cy="30" r="1.5" opacity="0.35" class="shim"/>
    <circle cx="820" cy="55" r="1" opacity="0.25"/>
    <circle cx="760" cy="80" r="1.5" opacity="0.3" class="shim"/>
    <circle cx="850" cy="15" r="1" opacity="0.2"/>
    <circle cx="1160" cy="40" r="2" opacity="0.3" class="shim"/>
    <circle cx="1180" cy="90" r="1.5" opacity="0.25"/>
    <circle cx="1140" cy="260" r="2" opacity="0.3" class="shim"/>
    <circle cx="1180" cy="240" r="1" opacity="0.2"/>
    <circle cx="800" cy="270" r="1.5" opacity="0.25" class="shim"/>
    <circle cx="750" cy="250" r="1" opacity="0.2"/>
  </g>

  <!-- ═══ TECH ORB (right side) ═══ -->
  <!-- Outer ring 1 -->
  <circle cx="950" cy="148" r="108" fill="none" stroke="#0e6ba8" stroke-width="0.6" opacity="0.18" class="s1"/>
  <!-- Outer ring 2 (dashed) -->
  <circle cx="950" cy="148" r="88" fill="none" stroke="#00d4ff" stroke-width="0.5" opacity="0.12" stroke-dasharray="6,12" class="s2"/>
  <!-- Mid ring -->
  <circle cx="950" cy="148" r="65" fill="none" stroke="#4fc3f7" stroke-width="0.8" opacity="0.2" class="s3"/>
  <!-- Inner ring -->
  <circle cx="950" cy="148" r="44" fill="none" stroke="#00d4ff" stroke-width="1" opacity="0.25"/>
  <!-- Core glow -->
  <circle cx="950" cy="148" r="24" fill="url(#orbGlow)" class="p1"/>
  <circle cx="950" cy="148" r="12" fill="#0e6ba8" opacity="0.35" class="p2" filter="url(#orbFilter)"/>
  <circle cx="950" cy="148" r="5" fill="#00d4ff" opacity="0.7" class="p1"/>

  <!-- Orbit dots on rings -->
  <circle cx="950" cy="40" r="3" fill="#00d4ff" opacity="0.5" filter="url(#orbFilter)" class="s1"/>
  <circle cx="1058" cy="148" r="2.5" fill="#4fc3f7" opacity="0.4" class="s2"/>
  <circle cx="862" cy="220" r="2" fill="#00d4ff" opacity="0.35" class="s3"/>

  <!-- Connection lines from card to orb -->
  <line x1="730" y1="148" x2="842" y2="148" stroke="#00d4ff" stroke-width="0.4" opacity="0.2" stroke-dasharray="4,8"/>

  <!-- ═══ GLASS CARD ═══ -->
  <!-- Shadow layer -->
  <rect x="55" y="33" width="700" height="225" rx="24" fill="#000" opacity="0.35" filter="url(#softBlur)"/>
  <!-- Glass background -->
  <rect x="52" y="30" width="700" height="225" rx="24"
        fill="rgba(14,107,168,0.06)"
        stroke="rgba(0,212,255,0.18)"
        stroke-width="1"/>
  <!-- Top glass highlight -->
  <rect x="53" y="31" width="698" height="1.5" rx="20" fill="rgba(255,255,255,0.22)"/>
  <!-- Left glass highlight -->
  <rect x="53" y="31" width="1.5" height="223" rx="2" fill="rgba(255,255,255,0.12)"/>
  <!-- Inner card glow -->
  <rect x="52" y="30" width="700" height="225" rx="24" fill="url(#cardGlow)"/>

  <!-- ═══ CARD CONTENT ═══ -->
  <!-- Name -->
  <text x="105" y="115"
    font-family="-apple-system,BlinkMacSystemFont,'SF Pro Display','Segoe UI',system-ui,sans-serif"
    font-size="60" font-weight="700" letter-spacing="-1"
    fill="#00d4ff"
    filter="url(#textGlow)"
    class="p1">Sarathkumar</text>

  <!-- Divider line -->
  <rect x="105" y="128" width="580" height="1" rx="1"
        fill="rgba(0,212,255,0.2)"/>

  <!-- Subtitle -->
  <text x="108" y="158"
    font-family="-apple-system,BlinkMacSystemFont,'SF Pro Text','Segoe UI',system-ui,sans-serif"
    font-size="16" font-weight="400" letter-spacing="0.3"
    fill="#90caf9" opacity="0.88">
    Full-Stack Developer  ·  AI &amp; ML Enthusiast  ·  Colombo, Sri Lanka
  </text>

  <!-- ═══ TECH PILL BADGES ═══ -->
  <!-- React -->
  <rect x="105" y="180" width="62" height="24" rx="12"
        fill="rgba(97,218,251,0.1)" stroke="rgba(97,218,251,0.35)" stroke-width="0.8" class="tag"/>
  <text x="136" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#61dafb" class="tag">React</text>

  <!-- Node.js -->
  <rect x="176" y="180" width="66" height="24" rx="12"
        fill="rgba(104,193,52,0.1)" stroke="rgba(104,193,52,0.3)" stroke-width="0.8" class="tag"/>
  <text x="209" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#7ec850" class="tag">Node.js</text>

  <!-- Python -->
  <rect x="251" y="180" width="62" height="24" rx="12"
        fill="rgba(77,171,247,0.1)" stroke="rgba(77,171,247,0.3)" stroke-width="0.8" class="tag"/>
  <text x="282" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#4dabf7" class="tag">Python</text>

  <!-- Django -->
  <rect x="322" y="180" width="62" height="24" rx="12"
        fill="rgba(9,110,66,0.15)" stroke="rgba(9,110,66,0.4)" stroke-width="0.8" class="tag"/>
  <text x="353" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#44b78b" class="tag">Django</text>

  <!-- ML/AI -->
  <rect x="393" y="180" width="58" height="24" rx="12"
        fill="rgba(255,120,80,0.1)" stroke="rgba(255,120,80,0.25)" stroke-width="0.8" class="tag"/>
  <text x="422" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#ff9a7b" class="tag">ML / AI</text>

  <!-- Docker -->
  <rect x="460" y="180" width="58" height="24" rx="12"
        fill="rgba(13,183,237,0.1)" stroke="rgba(13,183,237,0.25)" stroke-width="0.8" class="tag"/>
  <text x="489" y="196" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11.5" font-weight="500"
    fill="#0db7ed" class="tag">Docker</text>

  <!-- Location badge -->
  <rect x="105" y="215" width="130" height="22" rx="11"
        fill="rgba(0,212,255,0.08)" stroke="rgba(0,212,255,0.2)" stroke-width="0.7"/>
  <text x="170" y="230" text-anchor="middle"
    font-family="-apple-system,sans-serif" font-size="11" font-weight="400"
    fill="#90caf9" opacity="0.8">Sri Lanka  ·  Open to Work</text>

  <!-- ═══ BOTTOM WAVE ═══ -->
  <path d="M0 260 Q300 240 600 258 Q900 276 1200 255 L1200 300 L0 300 Z"
        fill="rgba(14,107,168,0.08)"/>
  <path d="M0 275 Q400 260 800 272 Q1000 278 1200 265 L1200 300 L0 300 Z"
        fill="rgba(0,212,255,0.05)"/>
</svg>
