<svg width="1180" height="610" viewBox="0 0 1180 610" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
<title>Developer Profile Banner - Dark</title>
<desc>Animated glassmorphic developer profile hero banner</desc>
<defs>
  <clipPath id="cardClip"><rect x="0" y="0" width="1180" height="610" rx="28"/></clipPath>
  <clipPath id="leftPanelClip"><rect x="24" y="24" width="406" height="562" rx="20"/></clipPath>
  <clipPath id="rightPanelClip"><rect x="454" y="24" width="702" height="562" rx="20"/></clipPath>

  <radialGradient id="blobViolet" cx="50%" cy="50%" r="50%">
    <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.55"/>
    <stop offset="100%" stop-color="#7C3AED" stop-opacity="0"/>
  </radialGradient>
  <radialGradient id="blobCyan" cx="50%" cy="50%" r="50%">
    <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.45"/>
    <stop offset="100%" stop-color="#22D3EE" stop-opacity="0"/>
  </radialGradient>
  <radialGradient id="blobEmerald" cx="50%" cy="50%" r="50%">
    <stop offset="0%" stop-color="#10B981" stop-opacity="0.40"/>
    <stop offset="100%" stop-color="#10B981" stop-opacity="0"/>
  </radialGradient>

  <linearGradient id="accentGradient" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#7C3AED"/>
    <stop offset="50%" stop-color="#22D3EE"/>
    <stop offset="100%" stop-color="#10B981"/>
    <animate attributeName="x1" values="0%;100%;0%" dur="8s" repeatCount="indefinite"/>
    <animate attributeName="x2" values="100%;200%;100%" dur="8s" repeatCount="indefinite"/>
  </linearGradient>

  <linearGradient id="asciiGradient" x1="0%" y1="0%" x2="100%" y2="100%" spreadMethod="reflect">
    <stop offset="0%" stop-color="#7C3AED"/>
    <stop offset="50%" stop-color="#22D3EE"/>
    <stop offset="100%" stop-color="#10B981"/>
    <animateTransform attributeName="gradientTransform" type="translate" values="0 0;60 0;0 0" dur="6s" repeatCount="indefinite"/>
  </linearGradient>

  <linearGradient id="borderShimmer" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#ffffff" stop-opacity="0"/>
    <stop offset="45%" stop-color="#ffffff" stop-opacity="0"/>
    <stop offset="50%" stop-color="#ffffff" stop-opacity="0.7"/>
    <stop offset="55%" stop-color="#ffffff" stop-opacity="0"/>
    <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    <animateTransform attributeName="gradientTransform" type="translate" values="-1200 0;1200 0" dur="5s" repeatCount="indefinite"/>
  </linearGradient>

  <linearGradient id="glassSheen" x1="0%" y1="0%" x2="100%" y2="100%">
    <stop offset="0%" stop-color="#ffffff" stop-opacity="0.06"/>
    <stop offset="40%" stop-color="#ffffff" stop-opacity="0.015"/>
    <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
  </linearGradient>

  <linearGradient id="scanlineGrad" x1="0%" y1="0%" x2="0%" y2="100%">
    <stop offset="0%" stop-color="#22D3EE" stop-opacity="0"/>
    <stop offset="50%" stop-color="#22D3EE" stop-opacity="0.10"/>
    <stop offset="100%" stop-color="#22D3EE" stop-opacity="0"/>
  </linearGradient>

  <filter id="glow" x="-60%" y="-60%" width="220%" height="220%">
    <feGaussianBlur stdDeviation="4" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>
  <filter id="softGlowBig" x="-80%" y="-80%" width="260%" height="260%">
    <feGaussianBlur stdDeviation="14"/>
  </filter>
  <filter id="cardShadow" x="-20%" y="-20%" width="140%" height="140%">
    <feDropShadow dx="0" dy="18" stdDeviation="24" flood-color="#000000" flood-opacity="0.55"/>
  </filter>
  <filter id="noiseFilter" x="0" y="0" width="100%" height="100%">
    <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="2" stitchTiles="stitch" result="n"/>
    <feColorMatrix in="n" type="matrix" values="0 0 0 0 1  0 0 0 0 1  0 0 0 0 1  0 0 0 0.02 0"/>
  </filter>

  <style>
    .mono{font-family:'JetBrains Mono','Fira Code',Consolas,Menlo,monospace;}
    .sans{font-family:'Segoe UI',system-ui,-apple-system,Helvetica,Arial,sans-serif;}
    .pill{transform-box:fill-box;transform-origin:center;transition:transform .25s ease;}
    .pill:hover{transform:scale(1.08);}
    .pill:hover .pillGlowRect{opacity:1;}
    .social{transform-box:fill-box;transform-origin:center;transition:transform .25s ease;}
    .social:hover{transform:scale(1.15);}
  </style>
</defs>

<g filter="url(#cardShadow)">
<g clip-path="url(#cardClip)">
  <rect width="1180" height="610" fill="#030712"/>

  <!-- floating background glows -->
  <g>
    <circle cx="180" cy="120" r="260" fill="url(#blobViolet)">
      <animateTransform attributeName="transform" type="translate" values="0 0;40 30;-20 10;0 0" dur="14s" repeatCount="indefinite"/>
    </circle>
    <circle cx="950" cy="480" r="300" fill="url(#blobCyan)">
      <animateTransform attributeName="transform" type="translate" values="0 0;-30 -20;20 15;0 0" dur="16s" repeatCount="indefinite"/>
    </circle>
    <circle cx="700" cy="60" r="220" fill="url(#blobEmerald)">
      <animateTransform attributeName="transform" type="translate" values="0 0;25 20;-15 -10;0 0" dur="18s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- noise texture -->
  <rect width="1180" height="610" filter="url(#noiseFilter)"/>

  <!-- moving scanline sweep across whole card -->
  <rect x="0" y="-120" width="1180" height="120" fill="url(#scanlineGrad)">
    <animateTransform attributeName="transform" type="translate" values="0 0;0 730" dur="7s" repeatCount="indefinite"/>
  </rect>

  <!-- tiny floating particles -->
  <g fill="#22D3EE">
    <circle cx="120" cy="500" r="1.6" opacity="0.6">
      <animateMotion path="M0,0 C 20,-40 -10,-80 10,-140" dur="9s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.8;0" dur="9s" repeatCount="indefinite"/>
    </circle>
    <circle cx="380" cy="560" r="1.2" fill="#7C3AED" opacity="0.6">
      <animateMotion path="M0,0 C -15,-50 25,-90 5,-160" dur="11s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.7;0" dur="11s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1050" cy="120" r="1.4" fill="#10B981" opacity="0.6">
      <animateMotion path="M0,0 C 10,40 -20,70 -5,130" dur="10s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.7;0" dur="10s" repeatCount="indefinite"/>
    </circle>
    <circle cx="900" cy="550" r="1.3" opacity="0.5">
      <animateMotion path="M0,0 C -25,-30 15,-70 -10,-120" dur="12.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.6;0" dur="12.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="600" cy="80" r="1.2" fill="#7C3AED" opacity="0.5">
      <animateMotion path="M0,0 C 15,30 -15,60 5,110" dur="13s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.6;0" dur="13s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- outer border with shimmer -->
  <rect x="1" y="1" width="1178" height="608" rx="27" fill="none" stroke="rgba(255,255,255,.08)" stroke-width="1.5"/>
  <rect x="1" y="1" width="1178" height="608" rx="27" fill="none" stroke="url(#borderShimmer)" stroke-width="1.5"/>

  <!-- =============== LEFT PANEL =============== -->
  <g>
    <rect x="24" y="24" width="406" height="562" rx="20" fill="#0F172A" fill-opacity="0.55"/>
    <rect x="24" y="24" width="406" height="562" rx="20" fill="url(#glassSheen)"/>
    <rect x="24.5" y="24.5" width="405" height="561" rx="19.5" fill="none" stroke="rgba(255,255,255,.08)" stroke-width="1"/>

    <g clip-path="url(#leftPanelClip)">
      <!-- floating ascii portrait -->
      <g transform="translate(227,120)">
        <animateTransform attributeName="transform" type="translate" additive="sum" values="227,120;227,112;227,120" dur="5s" repeatCount="indefinite"/>
        <text text-anchor="middle" class="mono" font-size="12.5" fill="url(#asciiGradient)" style="letter-spacing:1px;">
          <tspan x="0" dy="0">      .:^!!!^:.</tspan>
          <tspan x="0" dy="16">   :~7?JJJJJJ?7~:</tspan>
          <tspan x="0" dy="16">  ~?JJYY55555YYJJ?~</tspan>
          <tspan x="0" dy="16"> ^?JY5PGB##BGP5YJ?^</tspan>
          <tspan x="0" dy="16"> 7JY5B@@@@@@@@B5YJ7</tspan>
          <tspan x="0" dy="16"> 7JY5#@@●@@●@@#5YJ7</tspan>
          <tspan x="0" dy="16"> 7JY5B@@@@@@@@B5YJ7</tspan>
          <tspan x="0" dy="16"> ^?JYPB@@▽@@BPYJ?^</tspan>
          <tspan x="0" dy="16">  ~?JJY5PGBBGP5YJJ?~</tspan>
          <tspan x="0" dy="16">   :~7?JJJJJJ?7~:</tspan>
          <tspan x="0" dy="16">      .:^!!!^:.</tspan>
        </text>
        <!-- reveal masks: 11 lines, staggered fade-in/hold/out cycle -->
        <rect x="-120" y="-14" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.03;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="2" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.06;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="18" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.09;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="34" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.12;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="50" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.15;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="66" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.18;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="82" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.21;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="98" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.24;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="114" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.27;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="130" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.30;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
        <rect x="-120" y="146" width="240" height="16" fill="#030712">
          <animate attributeName="opacity" values="1;0;0;1;1" keyTimes="0;0.33;0.85;0.92;1" dur="9s" begin="0s" repeatCount="indefinite"/>
        </rect>
      </g>

      <!-- mini terminal readout under ascii -->
      <g class="mono" font-size="12.5" fill="#94A3B8">
        <text x="48" y="320">$ whoami<tspan fill="#22D3EE"> _</tspan>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="9s" begin="0.2s" repeatCount="indefinite"/>
        </text>
        <text x="48" y="342" fill="#10B981">&gt; creative_developer
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="9s" begin="0.5s" repeatCount="indefinite"/>
        </text>
        <text x="48" y="368">$ status --check
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="9s" begin="0.8s" repeatCount="indefinite"/>
        </text>
        <text x="48" y="390" fill="#10B981">&gt; [ONLINE] available for hire
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="9s" begin="1.1s" repeatCount="indefinite"/>
        </text>
      </g>

      <!-- blinking cursor -->
      <rect x="48" y="396" width="8" height="14" fill="#22D3EE">
        <animate attributeName="opacity" values="1;1;0;0" keyTimes="0;0.5;0.5;1" dur="1s" repeatCount="indefinite"/>
      </rect>

      <!-- status dot -->
      <g transform="translate(48,450)">
        <circle r="4" fill="#10B981">
          <animate attributeName="opacity" values="1;0.3;1" dur="1.6s" repeatCount="indefinite"/>
        </circle>
        <text x="14" y="4" class="mono" font-size="11" fill="#94A3B8" style="letter-spacing:1.5px;">SYSTEM ONLINE</text>
      </g>

      <!-- decorative code fragment near bottom -->
      <g class="mono" font-size="11" fill="#475569" opacity="0.55">
        <text x="48" y="510">const dev = {</text>
        <text x="60" y="528">focus: "ship fast",</text>
        <text x="60" y="546">craft: "obsessive",</text>
        <text x="60" y="564">coffee: true</text>
        <text x="48" y="582">};</text>
      </g>
    </g>
  </g>

  <!-- =============== RIGHT PANEL (terminal) =============== -->
  <g>
    <rect x="454" y="24" width="702" height="562" rx="20" fill="#0F172A" fill-opacity="0.55"/>
    <rect x="454" y="24" width="702" height="562" rx="20" fill="url(#glassSheen)"/>
    <rect x="454.5" y="24.5" width="701" height="561" rx="19.5" fill="none" stroke="rgba(255,255,255,.08)" stroke-width="1"/>

    <g clip-path="url(#rightPanelClip)">
      <!-- header bar -->
      <rect x="454" y="24" width="702" height="42" rx="20" fill="#0B1220" fill-opacity="0.6"/>
      <rect x="454" y="46" width="702" height="20" fill="#0B1220" fill-opacity="0.6"/>
      <circle cx="480" cy="45" r="6" fill="#FF5F56"/>
      <circle cx="502" cy="45" r="6" fill="#FFBD2E"/>
      <circle cx="524" cy="45" r="6" fill="#27C93F"/>
      <text x="805" y="49" text-anchor="middle" class="mono" font-size="12.5" fill="#64748B">visitor@devfolio: ~</text>
      <line x1="454" y1="66" x2="1156" y2="66" stroke="rgba(255,255,255,.06)" stroke-width="1"/>

      <!-- greeting -->
      <text x="486" y="112" class="sans" font-size="22" font-weight="600" fill="#F8FAFC">
        Hi <tspan>👋</tspan>
      </text>
      <text x="486" y="150" class="sans" font-size="34" font-weight="700" fill="url(#accentGradient)">
        I'm Mayank Jha
      </text>

      <!-- typing role line -->
      <g class="mono" font-size="20" fill="#94A3B8">
        <g>
          <clipPath id="clipRole0"><rect x="486" y="176" height="26">
            <animate attributeName="width" values="0;0;204;204;0;0" keyTimes="0;0;0.0533;0.1667;0.2;1" dur="15s" begin="0s" repeatCount="indefinite"/>
          </rect></clipPath>
          <text x="486" y="194" clip-path="url(#clipRole0)">Frontend Engineer</text>
        </g>
        <g>
          <clipPath id="clipRole1"><rect x="486" y="176" height="26">
            <animate attributeName="width" values="0;0;252;252;0;0" keyTimes="0;0.2;0.2533;0.3667;0.4;1" dur="15s" begin="0s" repeatCount="indefinite"/>
          </rect></clipPath>
          <text x="486" y="194" clip-path="url(#clipRole1)">Full Stack Developer</text>
        </g>
        <g>
          <clipPath id="clipRole2"><rect x="486" y="176" height="26">
            <animate attributeName="width" values="0;0;288;288;0;0" keyTimes="0;0.4;0.4533;0.5667;0.6;1" dur="15s" begin="0s" repeatCount="indefinite"/>
          </rect></clipPath>
          <text x="486" y="194" clip-path="url(#clipRole2)">Open Source Contributor</text>
        </g>
        <g>
          <clipPath id="clipRole3"><rect x="486" y="176" height="26">
            <animate attributeName="width" values="0;0;132;132;0;0" keyTimes="0;0.6;0.6533;0.7667;0.8;1" dur="15s" begin="0s" repeatCount="indefinite"/>
          </rect></clipPath>
          <text x="486" y="194" clip-path="url(#clipRole3)">UI Engineer</text>
        </g>
        <g>
          <clipPath id="clipRole4"><rect x="486" y="176" height="26">
            <animate attributeName="width" values="0;0;156;156;0" keyTimes="0;0.8;0.8533;0.9667;1" dur="15s" begin="0s" repeatCount="indefinite"/>
          </rect></clipPath>
          <text x="486" y="194" clip-path="url(#clipRole4)">AI Enthusiast</text>
        </g>
      </g>
      <!-- tracking + blinking cursor for role line -->
      <rect y="178" width="2.5" height="20" fill="#22D3EE">
        <animate attributeName="x" dur="15s" repeatCount="indefinite"
          keyTimes="0;0.0533;0.1667;0.2;0.2533;0.3667;0.4;0.4533;0.5667;0.6;0.6533;0.7667;0.8;0.8533;0.9667;1"
          values="486;690;690;486;738;738;486;774;774;486;618;618;486;642;642;486"/>
        <animate attributeName="opacity" values="1;1;0;0" keyTimes="0;0.5;0.5;1" dur="0.9s" repeatCount="indefinite"/>
      </rect>

      <line x1="486" y1="214" x2="1124" y2="214" stroke="rgba(255,255,255,.07)" stroke-width="1"/>

      <!-- info rows -->
      <g class="sans" font-size="14.5" fill="#94A3B8">
        <g transform="translate(486,246)">
          <path d="M0,-9 C4,-9 8,-6 8,-1 C8,5 0,12 0,12 C0,12 -8,5 -8,-1 C-8,-6 -4,-9 0,-9 Z" fill="url(#accentGradient)"/>
          <circle r="2.6" fill="#0F172A"/>
          <text x="22" y="4" fill="#F8FAFC" font-weight="600">Location <tspan fill="#94A3B8" font-weight="400">— Mumbai, Maharashtra</tspan></text>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="10s" begin="0s" repeatCount="indefinite"/>
        </g>
        <g transform="translate(486,280)">
          <path d="M-10,-3 L0,-8 L10,-3 L0,2 Z" fill="url(#accentGradient)"/>
          <path d="M-6,-1 L-6,5 C-6,8 6,8 6,5 L6,-1" fill="none" stroke="url(#accentGradient)" stroke-width="1.4"/>
          <text x="22" y="4" fill="#F8FAFC" font-weight="600">Education <tspan fill="#94A3B8" font-weight="400">— B.Tech AI &amp; ML</tspan></text>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="10s" begin="0.3s" repeatCount="indefinite"/>
        </g>
        <g transform="translate(486,314)">
          <circle r="9" fill="none" stroke="url(#accentGradient)" stroke-width="1.4"/>
          <circle r="5" fill="none" stroke="url(#accentGradient)" stroke-width="1.4"/>
          <circle r="1.6" fill="url(#accentGradient)"/>
          <text x="22" y="4" fill="#F8FAFC" font-weight="600">Current Focus <tspan fill="#94A3B8" font-weight="400">— Building Applications &amp; Websites</tspan></text>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="10s" begin="0.6s" repeatCount="indefinite"/>
        </g>
        <g transform="translate(486,348)">
          <circle r="9" fill="none" stroke="url(#accentGradient)" stroke-width="1.4"/>
          <ellipse cx="0" cy="0" rx="4" ry="9" fill="none" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <line x1="-9" y1="0" x2="9" y2="0" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="22" y="4" fill="#F8FAFC" font-weight="600">Portfolio <tspan fill="#94A3B8" font-weight="400">— porfolio21.netlify.app</tspan></text>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="10s" begin="0.9s" repeatCount="indefinite"/>
        </g>
        <g transform="translate(486,382)">
          <rect x="-10" y="-7" width="20" height="14" rx="2" fill="none" stroke="url(#accentGradient)" stroke-width="1.4"/>
          <path d="M-10,-6 L0,2 L10,-6" fill="none" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="22" y="4" fill="#F8FAFC" font-weight="600">Email <tspan fill="#94A3B8" font-weight="400">— mayankbuilds21@gmail.com</tspan></text>
          <animate attributeName="opacity" values="0;1;1;1;1" keyTimes="0;0.02;0.9;0.95;1" dur="10s" begin="1.2s" repeatCount="indefinite"/>
        </g>
      </g>

      <line x1="486" y1="408" x2="1124" y2="408" stroke="rgba(255,255,255,.07)" stroke-width="1"/>

      <text x="486" y="432" class="sans" font-size="13" font-weight="700" fill="#64748B" style="letter-spacing:2px;">SKILLS</text>

      <!-- skill pills row 1 -->
      <g class="sans" font-size="13" font-weight="600">
        <!-- React -->
        <g class="pill" transform="translate(486,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="78" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="4s" repeatCount="indefinite"/></rect>
          <rect width="70" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="35" y="21" text-anchor="middle" fill="#F8FAFC">React</text>
        </g>
        <!-- Next.js -->
        <g class="pill" transform="translate(566,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="86" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="4.4s" repeatCount="indefinite"/></rect>
          <rect width="78" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="39" y="21" text-anchor="middle" fill="#F8FAFC">Next.js</text>
        </g>
        <!-- Node.js -->
        <g class="pill" transform="translate(654,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="86" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="4.8s" repeatCount="indefinite"/></rect>
          <rect width="78" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="39" y="21" text-anchor="middle" fill="#F8FAFC">Node.js</text>
        </g>
        <!-- TypeScript -->
        <g class="pill" transform="translate(742,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="104" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="5.2s" repeatCount="indefinite"/></rect>
          <rect width="96" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="48" y="21" text-anchor="middle" fill="#F8FAFC">TypeScript</text>
        </g>
        <!-- Tailwind -->
        <g class="pill" transform="translate(848,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="96" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="5.6s" repeatCount="indefinite"/></rect>
          <rect width="88" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="44" y="21" text-anchor="middle" fill="#F8FAFC">Tailwind</text>
        </g>
        <!-- Python -->
        <g class="pill" transform="translate(944,446)">
          <rect class="pillGlowRect" x="-4" y="-4" width="84" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="6s" repeatCount="indefinite"/></rect>
          <rect width="76" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="38" y="21" text-anchor="middle" fill="#F8FAFC">Python</text>
        </g>
      </g>

      <!-- skill pills row 2 -->
      <g class="sans" font-size="13" font-weight="600">
        <!-- Docker -->
        <g class="pill" transform="translate(486,490)">
          <rect class="pillGlowRect" x="-4" y="-4" width="90" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="4.2s" repeatCount="indefinite"/></rect>
          <rect width="82" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="41" y="21" text-anchor="middle" fill="#F8FAFC">Docker</text>
        </g>
        <!-- Postgres -->
        <g class="pill" transform="translate(582,490)">
          <rect class="pillGlowRect" x="-4" y="-4" width="100" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="4.6s" repeatCount="indefinite"/></rect>
          <rect width="92" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="46" y="21" text-anchor="middle" fill="#F8FAFC">Postgres</text>
        </g>
        <!-- AWS -->
        <g class="pill" transform="translate(688,490)">
          <rect class="pillGlowRect" x="-4" y="-4" width="74" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="5s" repeatCount="indefinite"/></rect>
          <rect width="66" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="33" y="21" text-anchor="middle" fill="#F8FAFC">AWS</text>
        </g>
        <!-- Git -->
        <g class="pill" transform="translate(768,490)">
          <rect class="pillGlowRect" x="-4" y="-4" width="62" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="5.4s" repeatCount="indefinite"/></rect>
          <rect width="54" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="27" y="21" text-anchor="middle" fill="#F8FAFC">Git</text>
        </g>
        <!-- Figma -->
        <g class="pill" transform="translate(834,490)">
          <rect class="pillGlowRect" x="-4" y="-4" width="82" height="40" rx="20" fill="url(#accentGradient)" opacity="0" filter="url(#softGlowBig)"><animate attributeName="opacity" values="0.25;0.55;0.25" dur="5.8s" repeatCount="indefinite"/></rect>
          <rect width="74" height="32" rx="16" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.2"/>
          <text x="37" y="21" text-anchor="middle" fill="#F8FAFC">Figma</text>
        </g>
      </g>

      <line x1="486" y1="536" x2="1124" y2="536" stroke="rgba(255,255,255,.07)" stroke-width="1"/>

      <!-- social icons -->
      <g class="sans" font-size="12" font-weight="700" fill="#F8FAFC">
        <g class="social" transform="translate(510,564)">
          <circle r="19" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.3" filter="url(#glow)"/>
          <text text-anchor="middle" dy="4">GH</text>
        </g>
        <g class="social" transform="translate(566,564)">
          <circle r="19" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.3" filter="url(#glow)"/>
          <text text-anchor="middle" dy="4">in</text>
        </g>
        <g class="social" transform="translate(622,564)">
          <circle r="19" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.3" filter="url(#glow)"/>
          <text text-anchor="middle" dy="4">X</text>
        </g>
        <g class="social" transform="translate(678,564)">
          <circle r="19" fill="#111827" stroke="url(#accentGradient)" stroke-width="1.3" filter="url(#glow)"/>
          <text text-anchor="middle" dy="4">🌐</text>
        </g>
      </g>
    </g>
  </g>
</g>
</g>
</svg>
