from pathlib import Path
import textwrap, zipfile, os

root = Path("/mnt/data/richard_janas_github_profile")
assets = root / "assets"
workflow = root / ".github" / "workflows"
assets.mkdir(parents=True, exist_ok=True)
workflow.mkdir(parents=True, exist_ok=True)

readme = r'''<div align="center">

<a href="https://github.com/Ricthi">
  <img src="./assets/profile-banner.svg" alt="K. Richard Janas GitHub profile banner" width="100%">
</a>

<h1>K. RICHARD JANAS</h1>

<p><strong>AI Product Engineer · Software Engineer · Product Designer</strong></p>

<p>
  Computer Science & Engineering · Thoothukudi, Tamil Nadu, India
</p>

<p>
  <a href="mailto:dreamnasa1774@gmail.com">Email</a> ·
  <a href="https://www.linkedin.com/in/richard-k-profile/">LinkedIn</a> ·
  <a href="https://richierich.framer.website">Portfolio</a> ·
  <a href="https://github.com/Ricthi">GitHub</a>
</p>

</div>

---

## About

I build software products that connect **engineering, artificial intelligence, and product design**.

My work includes Python-based applications, responsive web experiences, AI-assisted tools, OCR and computer-vision projects, and UI/UX systems. I enjoy taking a problem from **idea → user flow → interface → implementation → refinement**.

I am currently expanding my engineering depth in AI product development, modern web applications, and practical software engineering.

---

## Technical Skills

### Engineering
`Python` · `JavaScript` · `HTML5` · `CSS3` · `FastAPI` · `Flask` · `Streamlit` · `REST APIs` · `Git` · `GitHub`

### AI & Computer Vision
`AI Product Engineering` · `Prompt Engineering` · `OCR` · `Image Processing` · `Computer Vision` · `Machine Learning Fundamentals` · `AI Workflow Design`

### Product & Design
`Figma` · `Framer` · `UI/UX Design` · `Product Design` · `Wireframing` · `Prototyping` · `Responsive Design` · `Design Systems`

### Creative Technology
`Blender` · `3D Modeling` · `3D Visualization` · `Animation` · `Photoshop` · `Adobe Firefly`

---

## Featured Work

### AI Heritage Tamil Character Recognition
**Research Project · AI / OCR / Computer Vision**

AI-assisted OCR work focused on recognizing ancient Tamil manuscript characters using image preprocessing and computer-vision techniques.

**Recognition:** Best Paper Award, International Conference on Intelligent Computing and Explainable AI (ICICEA 2026).

---

### APPLIT
**Social Networking Platform · UI/UX / Product Design**

Designed a modern social platform with profiles, messaging, community interactions, and responsive user flows.

---

### AURA SYNC
**Animated Headphones Web Experience · UI/UX / 3D**

Designed an immersive product experience combining responsive interface design with Blender-based 3D visualization, PBR materials, lighting, and animation.

---

### PIZZA CORNER
**Interactive Food Experience · UI/UX / Web Design**

Created a responsive restaurant experience using cinematic visual direction, interaction design, and cross-device UI principles.

---

## Education

**B.E. Computer Science and Engineering**  
Dr. G.U. Pope College of Engineering · Anna University  
**2022 – 2026 · CGPA: 8.45 / 10**

---

## Recognition

**Best Paper Award — ICICEA 2026**  
Awarded for the research project **AI Heritage Tamil Character Recognition** at the International Conference on Intelligent Computing and Explainable AI.

---

## Experience

**UI/UX Design Intern — Corizo**  
**October 2024 · Remote**

- Designed wireframes and high-fidelity interfaces using Figma.
- Created responsive layouts focused on usability and accessibility.
- Applied user-centered design principles to interactive prototypes.

**Founder & Creative Designer — Richie Designs**  
**2024 – Present**

- Designed brand identities, websites, and digital product experiences.
- Developed UI/UX solutions from wireframes through interactive prototypes.
- Created 3D and visual assets using Blender and Adobe tools.

---

## Current Focus

- AI-powered product development
- Product engineering
- Modern web applications
- Computer vision and OCR
- UI/UX systems
- 3D product experiences

---

<div align="center">

### Build. Design. Learn. Ship.

<a href="mailto:dreamnasa1774@gmail.com">Contact</a> ·
<a href="https://richierich.framer.website">Portfolio</a> ·
<a href="https://www.linkedin.com/in/richard-k-profile/">LinkedIn</a>

</div>
'''

banner = r'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 620" role="img" aria-labelledby="title desc">
  <title id="title">K. Richard Janas animated GitHub profile banner</title>
  <desc id="desc">Premium black and gold technical profile banner for an AI Product Engineer, Software Engineer and Product Designer.</desc>

  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#050505"/>
      <stop offset="0.55" stop-color="#0B0B0B"/>
      <stop offset="1" stop-color="#15110A"/>
    </linearGradient>

    <linearGradient id="gold" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#8F6B1F"/>
      <stop offset="0.45" stop-color="#F4D27A"/>
      <stop offset="0.7" stop-color="#C89B3C"/>
      <stop offset="1" stop-color="#FFF0B5"/>
    </linearGradient>

    <radialGradient id="glow">
      <stop offset="0" stop-color="#D4AF37" stop-opacity=".24"/>
      <stop offset="1" stop-color="#D4AF37" stop-opacity="0"/>
    </radialGradient>

    <filter id="blur">
      <feGaussianBlur stdDeviation="22"/>
    </filter>

    <filter id="shadow">
      <feDropShadow dx="0" dy="12" stdDeviation="18" flood-opacity=".55"/>
    </filter>

    <pattern id="grid" width="42" height="42" patternUnits="userSpaceOnUse">
      <path d="M42 0H0V42" fill="none" stroke="#D4AF37" stroke-opacity=".07"/>
    </pattern>
  </defs>

  <rect width="1600" height="620" rx="34" fill="url(#bg)"/>
  <rect width="1600" height="620" rx="34" fill="url(#grid)"/>

  <ellipse cx="1270" cy="170" rx="360" ry="250" fill="url(#glow)" filter="url(#blur)">
    <animate attributeName="opacity" values=".35;.65;.35" dur="5s" repeatCount="indefinite"/>
  </ellipse>

  <!-- Perspective frame -->
  <g transform="translate(1040 70) skewY(-4)" opacity=".9">
    <rect x="0" y="0" width="430" height="410" rx="24" fill="#080808" stroke="#D4AF37" stroke-opacity=".42"/>
    <rect x="24" y="24" width="382" height="362" rx="18" fill="none" stroke="#D4AF37" stroke-opacity=".12"/>
    <path d="M35 325 L385 55" stroke="#D4AF37" stroke-opacity=".12" stroke-width="2"/>
    <path d="M55 360 L405 90" stroke="#D4AF37" stroke-opacity=".08" stroke-width="2"/>
    <circle cx="214" cy="205" r="118" fill="none" stroke="url(#gold)" stroke-width="2" stroke-dasharray="5 12">
      <animateTransform attributeName="transform" type="rotate" from="0 214 205" to="360 214 205" dur="18s" repeatCount="indefinite"/>
    </circle>
    <circle cx="214" cy="205" r="86" fill="none" stroke="#D4AF37" stroke-opacity=".2" stroke-width="1"/>
    <text x="214" y="198" text-anchor="middle" fill="#F4D27A" font-family="Inter,Arial,sans-serif" font-size="22" letter-spacing="4">AI</text>
    <text x="214" y="232" text-anchor="middle" fill="#8F8F8F" font-family="Inter,Arial,sans-serif" font-size="12" letter-spacing="3">PRODUCT ENGINEERING</text>
  </g>

  <!-- Text -->
  <g filter="url(#shadow)">
    <text x="88" y="126" fill="#A98A3A" font-family="Inter,Arial,sans-serif" font-size="15" letter-spacing="6">PROFILE // 2026</text>
    <text x="88" y="215" fill="url(#gold)" font-family="Inter,Arial,sans-serif" font-size="62" font-weight="700" letter-spacing="2">K. RICHARD JANAS</text>
    <text x="92" y="265" fill="#F3F3F3" font-family="Inter,Arial,sans-serif" font-size="24" letter-spacing="1">AI PRODUCT ENGINEER  ·  SOFTWARE ENGINEER</text>
    <text x="92" y="304" fill="#B7B7B7" font-family="Inter,Arial,sans-serif" font-size="19">PRODUCT DESIGNER  ·  CREATIVE TECHNOLOGIST</text>

    <line x1="92" y1="350" x2="760" y2="350" stroke="url(#gold)" stroke-width="2">
      <animate attributeName="x2" values="400;760;400" dur="4.5s" repeatCount="indefinite"/>
    </line>

    <text x="92" y="396" fill="#E0E0E0" font-family="Inter,Arial,sans-serif" font-size="16">Python · JavaScript · FastAPI · Flask · Streamlit · Figma · Framer · Blender</text>
    <text x="92" y="430" fill="#8D8D8D" font-family="Inter,Arial,sans-serif" font-size="15">AI · OCR · Computer Vision · UI/UX · 3D Visualization</text>
  </g>

  <!-- Animated signal particles -->
  <g fill="#D4AF37">
    <circle cx="90" cy="520" r="2"><animate attributeName="cy" values="520;485;520" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="160" cy="548" r="1.5"><animate attributeName="cy" values="548;500;548" dur="3.1s" repeatCount="indefinite"/></circle>
    <circle cx="250" cy="520" r="2"><animate attributeName="cy" values="520;475;520" dur="2.8s" repeatCount="indefinite"/></circle>
    <circle cx="780" cy="540" r="1.7"><animate attributeName="cy" values="540;495;540" dur="3.5s" repeatCount="indefinite"/></circle>
    <circle cx="900" cy="500" r="2"><animate attributeName="cy" values="500;460;500" dur="2.2s" repeatCount="indefinite"/></circle>
  </g>

  <text x="92" y="565" fill="#6D6D6D" font-family="Inter,Arial,sans-serif" font-size="12" letter-spacing="3">BUILD · DESIGN · LEARN · SHIP</text>
</svg>
'''

snake = r'''name: Generate contribution snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches: ["main"]

permissions:
  contents: write

jobs:
  snake:
    runs-on: ubuntu-latest
    steps:
      - name: Generate contribution snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: Ricthi
          outputs: |
            dist/github-contribution-snake.svg?palette=github-dark
            dist/github-contribution-snake-dark.svg?palette=github-dark
      - name: Publish generated SVG
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
'''

(root / "README.md").write_text(readme, encoding="utf-8")
(assets / "profile-banner.svg").write_text(banner, encoding="utf-8")
(workflow / "snake.yml").write_text(snake, encoding="utf-8")

zip_path = Path("/mnt/data/Richard_Janas_GitHub_Profile_Premium.zip")
with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:
    for p in root.rglob("*"):
        if p.is_file():
            z.write(p, p.relative_to(root))

print(f"Created package: {zip_path}")
print("Files:")
for p in sorted(root.rglob("*")):
    if p.is_file():
        print(" -", p.relative_to(root))
