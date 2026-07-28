Bilal github profile prompt filled · MD
Bilal Nandoliya — GitHub Profile Master Prompt (Filled)
HOW TO USE THIS
Upload a clear head-and-shoulders photo of yourself (plain background, well-lit)
Copy EVERYTHING below the dashed line and paste into a new Claude session
Attach your photo to that same message
Follow the 4 phases as Claude guides you
▼ COPY FROM HERE ▼

Build my complete animated GitHub profile — banner, stats cards, contribution snake, and social badges. I've attached my photo. Work through the four phases below in order, and check in with me after each one. Don't generate five variations at once; show me one and let me react.

My Details
Name: Bilal Nandoliya GitHub username: nandoliyabilal Profile repo: nandoliyabilal/nandoliyabilal, branch main

Role: Full Stack MERN Developer Location: Gujarat, India Education: B.Sc. Information Technology — Gokul Global University Status: Building + Shipping + Open to Internships

ToolChain: VS Code, Git, Postman, Figma Languages: JavaScript, TypeScript, HTML, CSS Frontend: React.js, Responsive Design, REST API Integration Backend: Node.js, Express.js Database: MongoDB, MySQL, Supabase Infra: Netlify, Hostinger, Vercel, Razorpay API

LinkedIn: https://www.linkedin.com/in/bilalnandoliya/ Instagram: https://www.instagram.com/nandoliya_bilal/ Facebook: https://www.facebook.com/profile.php?id=61559554456980 Email: bilalnandoliya60@gmail.com Portfolio: https://bilalnandoliya.netlify.app/

Three logos to morph between: React (the blue spinning atom logo), Node.js (the green hexagon logo), MongoDB (the green leaf logo) — use official reference shapes, trace them accurately.

Palette
Portrait hue: 
#A78BFA dark / 
#7C3AED light UI chrome: 
#22D3EE / 
#0891B2 Accent: 
#10B981 Background: 
#0A101F

Palette rule: portrait must be a different hue from UI chrome so face doesn't blend into frame.

PHASE 1 — Banner (dark.svg / light.svg)
One terminal window, 1180×610, titled profile.sh --live. Left ~38% is portrait frame labelled VISUAL.MAP. Right is SYSTEM.INFO readout with dotted leaders, pulsing red LIVE badge, coloured pill with handle "nandoliyabilal".

Portrait — build in Python
Crop head + shoulders (not tight face crop)
300×340 grid, 1-bit Floyd–Steinberg dither, serpentine order
Contrast 1.3× only: autocontrast(cutoff=1) + UnsharpMask(radius=3, percent=140)
Draw dots as <path> runs with shape-rendering="crispEdges" — never font glyphs
Dark mode: segment background out (threshold colour distance, binary closing, fill holes, keep largest component) — dots draw lit subject on panel only
Light mode: keep background — dots draw dark parts of photo
Single hue — all tone from dot density
No grid lines, scanlines, glitch bars, CRT flicker
Animation
Intro (~3.2s, once): ~60 interleaved random groups fade in over ~2s. Groups scattered across whole portrait — dots appear everywhere at once and thicken together. NOT a wipe. NOT grouped by spatial region. Verify with evenness metric (~0.05 good, ~0.7 patchy). Needs duplicate portrait layer (~180KB).

Loop (~14.2s): portrait 3.0s, each logo 2.0s, 1.3s transitions. Use explicit uneven keyTimes.

Two independent layers:

Portrait — full density (~17k dots), grouped into ~94 drift bands. Each band translates ~42% toward first logo's centroid while fading, then returns. Add per-dot noise (sigma ~4) before grouping.
Travellers — ~900 dots morphing between React → Node.js → MongoDB logos via optimal transport. Opacity keyframes 0;0;0;1;1;...;0 so hidden during portrait phase.
Info Panel Rows (fill exactly as below)
Subject............ Bilal Nandoliya Role............... Full Stack MERN Developer Origin............. Gujarat, India Education.......... B.Sc. IT — Gokul Global University Status............. Building + Shipping + Open to Internships ToolChain.......... VS Code · Git · Postman · Figma Core.Lang.......... JavaScript · TypeScript · HTML · CSS Core.Frontend...... React.js · Responsive Design Core.Backend....... Node.js · Express.js Core.Database...... MongoDB · MySQL · Supabase Core.Infra......... Netlify · Hostinger · Vercel Grid.Mail.......... bilalnandoliya60@gmail.com Grid.Portfolio..... bilalnandoliya.netlify.app Grid.LinkedIn...... linkedin.com/in/bilalnandoliya Grid.GitHub........ github.com/nandoliyabilal Grid.Instagram..... instagram.com/nandoliya_bilal

Font-size 14, header 13, LIVE 12, pill 14, spacing 23px. Lock every row with textLength + lengthAdjust="spacingAndGlyphs".

PHASE 2 — Stats Cards (Self-Hosted)
Walk me through self-hosting github-readme-stats step by step:

Create GitHub classic token: Settings → Developer settings → Tokens (classic) → Generate new (classic) → repo scope → No expiration. Warn me to copy immediately, never share it.
Fork anuraghazra/github-readme-stats
Vercel → sign up with GitHub → Hobby (free) → Add New Project → import fork
Add environment variable PAT_1 = my token → Deploy
Give me my instance URL → generate themed block
Then produce:

Streak card (streak-stats.demolab.com) at width="100%"
Stats card and top-langs side by side at width="49%" each
Theme: background 
#0A101F, title 
#22D3EE, icons 
#A78BFA, text 
#94A3B8
Include hide_rank=true — explain that rank is stars-weighted and misleading for newer accounts
Username for all cards: nandoliyabilal

PHASE 3 — Contribution Snake
Write .github/workflows/snake.yml using Platane/snk/svg-only@v3:

Schedule: 12-hour cron + workflow_dispatch + push to main
Push to output branch via crazy-max/ghaction-github-pages@v3.1.0
Include permissions: contents: write
Tell me to set: repo Settings → Actions → General → Workflow permissions → Read and write (this is REPO settings, not account settings). URL: github.com/nandoliyabilal/nandoliyabilal/settings/actions

Two SVGs themed to my palette:

Light snake: color_snake=0891B2 color_dots=
#ebedf0,
#a5b4fc,
#818cf8,
#6366f1,
#0891B2

Dark snake: color_snake=10B981 color_dots=
#2d3343,
#4b5563,
#7C3AED,
#A78BFA,
#22D3EE

(First dot colour 
#2d3343 — must be visible slate against GitHub dark 
#0d1117, not near-black)

Display via theme-aware <picture> — tell me to add ONLY after Action runs green (output branch won't exist before).

PHASE 4 — Social Badges
shields.io badges, for-the-badge style, background 
#0A101F,    between each, all clickable.

LinkedIn: https://www.linkedin.com/in/bilalnandoliya/ → MUST use brand blue 
#0A66C2 (Shields.io bug: LinkedIn logo silently vanishes on any other colour)

Instagram: https://www.instagram.com/nandoliya_bilal/ → logo colour 
#A78BFA (recolours fine)

Email: bilalnandoliya60@gmail.com → logo colour 
#10B981 (recolours fine)

Portfolio: https://bilalnandoliya.netlify.app/ → use "netlify" logo or globe icon, logo colour 
#22D3EE

Skip GitHub badge — circular on own profile.

FINALLY — Assemble
Give me the complete README.md in one block with:

Banner <picture> (dark.svg + light.svg)
Stats cards (streak + stats + top-langs)
Snake <picture> (dark + light)
Social badges row
Fill in nandoliyabilal everywhere. Then give me a short checklist of what I do by hand (upload SVGs, create token, deploy Vercel, enable Actions permissions).

How to work with me
Verify by measurement, not by eye. cairosvg mishandles SMIL. Use correlation vs approved render, band distributions, ink coverage — then tell me to check in browser.
When something "didn't change": check raw.githubusercontent.com/.../file.svg?v=999 — almost always CDN cache not a bug.
Flag file size honestly. Banner lands ~900KB–1MB.
Tell me when I'm wrong.
If I reject something twice, stop and ask.
Keep generator script and .npy data — they're source of truth, not the SVG.
▲ END OF PROMPT ▲

QUICK REFERENCE — Your Links
Field	Value
GitHub	github.com/nandoliyabilal
Portfolio	bilalnandoliya.netlify.app
LinkedIn	linkedin.com/in/bilalnandoliya
Instagram	instagram.com/nandoliya_bilal
Email	bilalnandoliya60@gmail.com
Profile Repo	github.com/nandoliyabilal/nandoliyabilal
PHOTO TIPS (Read Before Starting)
For best banner result, your photo needs: ✅ Plain, flat background (white wall / studio backdrop) ✅ Head + shoulders framing (NOT just face — reads aggressive) ✅ Even lighting on face (no harsh shadows — they survive dithering) ✅ Clear separation from background (don't wear same colour as wall) ✅ Sharp, minimum 1000px on short edge ✅ Well-lit — the dithering amplifies bad lighting

❌ Busy background (biggest cause of poor result) ❌ Dark/moody lighting ❌ Tight face crop ❌ Blurry or low-res photo
