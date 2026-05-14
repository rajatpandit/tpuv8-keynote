# Style Guide: Architecting Intelligence Keynote

This document outlines the design philosophy, visual standards, and technical specifications for the "Architecting Intelligence" TPU Innovation Keynote.

## 🎨 Design Philosophy: "Luminescent Monolith"
The visual style is inspired by Apple's high-end hardware keynotes: **Ruthless Minimalism**, **Dramatic Contrast**, and **Cinematic Pacing**.

- **Atmosphere:** Dark, premium, and futuristic.
- **Mood:** Immersive and professional.
- **Focus:** One idea per slide. The speaker is the hero; the slides are the atmosphere.

---

## 🏛️ Layout & Grid
- **Aspect Ratio:** 16:9 (1920x1080).
- **Centering:** All primary content (Hero Numbers, Headings) is strictly centered horizontally and vertically to anchor the audience's focus.
- **Negative Space:** Deliberate use of empty "black" areas to allow the imagery and text to breathe and to prevent visual fatigue.

---

## 🔡 Typography
The presentation uses a tiered typography system to distinguish between technical precision and geometric beauty.

| Element | Font | Weight | Character |
| :--- | :--- | :--- | :--- |
| **Hero Numbers** | **Barlow** | 700 (Bold) | Technical, condensed, high-precision. |
| **Major Headings** | **Jost** | 700 (Bold) | Geometric, modern, impactful. |
| **Subtitles / Body** | **Inter** | 400 (Regular) | Clean, readable, Swiss-style. |

### Typography Specs
- **Hero Numbers:** `15vw` (Viewport Width). Tighter tracking (`-0.05em`) for a premium look.
- **Main Headings:** `10vw`.
- **Subtitles:** `3vw`.
- **Color:** Primary text is Pure White (`#FFFFFF`). Subtitles use Google Gray (`#E8EAED`).

---

## 🎨 Color Palette
- **Canvas:** Pure Black (`#000000`).
- **Dimming:** All background images are dimmed using a `0.55` brightness filter to ensure white text remains legible.
- **Google Accents:**
  - **Google Blue:** `#4285F4` (Primary accent for AlphaChip and Throughput).
  - **Google Red:** `#EA4335` (Accent for Latency).
  - **Google Yellow:** `#FBBC05`.
  - **Google Green:** `#34A853`.

---

## 🖼️ Visual Language
- **Imagery:** High-resolution macro photography of silicon chips, deep perspective shots of data centers, and abstract network visualizations.
- **Parallax effect:** Background images use a subtle 40-second `scale` and `translate` animation to give a "Ken Burns" breathing effect.
- **Text Shadows:** Multi-layered black drop shadows (`0 0 20px`, `0 0 40px`, `0 10px 60px`) ensure legibility against complex image backgrounds.

---

## 🎞️ Animation & Interaction
- **Transitions:** Smooth `fade` transitions between all slides.
- **Timeline Ticker:** A kinetic 6-second vertical scroll that fast-forwards through a decade, ending in a glowing **2026** with a blue starburst bloom.
- **Bifurcation:** An auto-animate morph where "The Monolith" physically splits into two columns: **Throughput** and **Latency**.
- **Sparkle Shine:** A one-time, slow-moving light sweep across the final hero text to signify "completion" and "polish."

---

## 🛠️ Technical Implementation
- **Framework:** Reveal.js 5.0.4.
- **Styling:** Custom CSS overrides within the `<style>` block of `index.html`.
- **Media:** Locally served `.mp4` and `.jpg/.webp` assets.
- **Plugins:** `RevealNotes` for speaker view.

---
*Last Updated: May 13, 2026*
