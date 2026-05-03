<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 300" width="100%" height="100%">
  <defs>
    <!-- Background -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0A1110"/>
      <stop offset="100%" stop-color="#111B16"/>
    </linearGradient>
    
    <!-- Mint gradients -->
    <linearGradient id="mintMain" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#00FF9D"/>
      <stop offset="100%" stop-color="#00B4D8"/>
    </linearGradient>
    <linearGradient id="mintDark" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#00C853"/>
      <stop offset="100%" stop-color="#0091EA"/>
    </linearGradient>
    
    <!-- Gloss -->
    <linearGradient id="gloss" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#FFFFFF" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#FFFFFF" stop-opacity="0"/>
    </linearGradient>
    
    <!-- Filters -->
    <filter id="softShadow" x="-20%" y="-20%" width="140%" height="140%">
      <feDropShadow dx="0" dy="4" stdDeviation="6" flood-color="#000000" flood-opacity="0.4"/>
    </filter>
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <rect width="800" height="300" fill="url(#bgGrad)" rx="20"/>

  <!-- Icon: SwiftOSC‑style network node + waveform -->
  <g transform="translate(110, 150)" filter="url(#softShadow)">
    <!-- Outer hexagon (SDK common shape) -->
    <polygon points="0,-55 48,-27 48,27 0,55 -48,27 -48,-27" fill="none" stroke="url(#mintMain)" stroke-width="2" opacity="0.4"/>
    
    <!-- Central circle (OSC message target) -->
    <circle cx="0" cy="0" r="22" fill="none" stroke="url(#mintMain)" stroke-width="2.5"/>
    <circle cx="0" cy="0" r="8" fill="#00FF9D" filter="url(#glow)"/>
    
    <!-- OSC wave / signal lines -->
    <path d="M -40,-15 Q -30,-25 -20,-15 T 0,-15 T 20,-15 T 40,-15" fill="none" stroke="url(#mintMain)" stroke-width="2" opacity="0.7"/>
    <path d="M -45,0 Q -35,-10 -20,0 T 0,0 T 20,0 T 45,0" fill="none" stroke="url(#mintDark)" stroke-width="2" opacity="0.5"/>
    <path d="M -40,15 Q -30,5 -20,15 T 0,15 T 20,15 T 40,15" fill="none" stroke="url(#mintMain)" stroke-width="2" opacity="0.7"/>
    
    <!-- Small data nodes -->
    <circle cx="-30" cy="-25" r="3" fill="#00FF9D" opacity="0.8"/>
    <circle cx="30" cy="-25" r="3" fill="#00FF9D" opacity="0.8"/>
    <circle cx="-35" cy="25" r="3" fill="#00FF9D" opacity="0.8"/>
    <circle cx="35" cy="25" r="3" fill="#00FF9D" opacity="0.8"/>
    
    <!-- "osc" label inside hexagon bottom -->
    <text x="0" y="70" font-family="'SF Mono', 'Segoe UI Mono', monospace" font-size="12" font-weight="700" fill="#00FF9D" text-anchor="middle" opacity="0.8" letter-spacing="2">OSC</text>
  </g>

  <!-- Typography: "thinmintai" left‑aligned, no spaces -->
  <g transform="translate(250, 120)">
    <text x="0" y="0" font-family="'Segoe UI', -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif" font-size="52" font-weight="300" fill="#FFFFFF" letter-spacing="0">
      <tspan font-weight="300" fill="#FFFFFF">thin</tspan>
      <tspan font-weight="600" fill="url(#mintMain)">mint</tspan>
      <tspan font-weight="300" fill="#FFFFFF">ai</tspan>
    </text>
    
    <!-- Divider -->
    <line x1="0" y1="20" x2="300" y2="20" stroke="#00FF9D" stroke-width="1.5" opacity="0.4"/>
    
    <!-- "clone" badge (clickable link) -->
    <a href="#" target="_blank">
      <rect x="0" y="32" width="70" height="26" rx="13" fill="none" stroke="#00FF9D" stroke-width="1.5" opacity="0.9"/>
      <text x="35" y="49" font-family="'Segoe UI', -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif" font-size="13" font-weight="600" fill="#00FF9D" text-anchor="middle" text-decoration="underline">clone</text>
    </a>
    
    <!-- Tagline with "SDK" hint -->
    <text x="80" y="49" font-family="'Segoe UI', -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif" font-size="14" font-weight="500" fill="#00B4D8" opacity="0.8" letter-spacing="2">SWIFT OSC SDK AGENT</text>
  </g>
</svg>