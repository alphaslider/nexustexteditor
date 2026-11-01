# nexustexteditor
full feature text and code editor in vanilla js and html5
NEXUS EDITOR // Monolith Code Workstation
A single-file, industrial hardware-themed code workstation. No build step, no dependencies except Google Fonts — drop it on GitHub Pages and it runs.

Nexus Editor Single File No Build

Features
Multi-tab VFS — saves workspace to localStorage, restore after reload
Collapsible Monolith — #region, braces, HTML tags → fold to /* ⊞ FOLDED */
Interactive gutter with fold buttons + outline navigator
Syntax grammars — JS, HTML, CSS, Python, JSON, Markdown, Plain
Theme Studio — 5 presets + full custom color picker, persists
Font Chassis — 10 mono fonts + custom system font, size + bold toggle
Find & Replace drawer
NEW: Character Encoding — selector in toolbar: UTF-8, UTF-8 BOM, UTF-16 LE/BE, Windows-1252, ISO-8859-1, ASCII, UTF-32 auto-detect
Auto-detects BOM on open (EF BB BF, FF FE, FE FF)
Decodes via TextDecoder, encodes on export to real bytes (not just charset label)
Per-tab encoding stored, shown in status bar ENC: UTF-8
NEW: Vertical Page Line / Ruler
Configurable columns: 80, 100, 120, 80+100, 80+120, 100+120, CUSTOM
Accurate monospace measurement via canvas measureText
Tracks horizontal scroll, font size/family/weight, window resize
Primary line glows in accent color, secondaries dashed
Toggle with GUIDE button, persists
Quick Start
Open index.html locally or enable GitHub Pages (Settings → Pages → root)
Ctrl+O open disk file, Ctrl+S save to Browser VFS, Ctrl+Shift+S export with encoding
Change ENC dropdown before opening legacy files (e.g. Windows-1252)
Set RULER to 80 for Python PEP8, 100 for modern, or 80+100 dual
File Structure
/
├── index.html          # the entire editor (110KB)
├── README.md
├── LICENSE
└── .gitignore
Browser Support
Modern Chromium / Firefox / Safari. TextDecoder required for encoding (all evergreen browsers). TextEncoder for UTF-8 export, manual encoders for others.

GitHub Pages
No action needed — it's static. Just push and enable Pages. Fonts load from Google Fonts CDN, works offline after first cache if you self-host fonts.

Limitations / Notes
Custom fonts from Google Fonts need internet on first load
UTF-32 encode is naive (no surrogate pairs beyond BMP)
ASCII/ISO exports replace >255 chars with ?
VFS uses localStorage (~5-10MB limit)
Roadmap
 Overlong line background highlight
 Minimap
 WASM tree-sitter for real tokenization
Made with the NEXUS chassis aesthetic — orange, steel, shader grid.
