# Architecting Intelligence: TPU Innovation Keynote

This is a cinematic, Apple-style Keynote presentation built with **Reveal.js**. It tells the story of Google's Tensor Processing Unit (TPU) innovation, from the initial compute crisis in 2006 to the cutting-edge TPU v8 architecture of 2026.

## 🚀 Presentation Features

- **Minimalist Aesthetics:** High-impact imagery with massive, clean typography (Inter, Jost, and Barlow).
- **Cinematic Pacing:** Smooth cross-fades and auto-animate transitions.
- **Ken Burns Effect:** Subtle, slow-panning background parallax for all hardware and data center imagery.
- **Dynamic Timeline:** A kinetic year-ticker on Slide 5 that fast-forwards through a decade of evolution with a custom starburst finish.
- **Interactive "Aha!" Moment:** A seamless visual bifurcation of the "Monolith" architecture into specialized "Throughput" (Training) and "Latency" (Inference) branches.
- **Speaker View:** Built-in speaker notes accessible via a secondary window.

## 📁 Project Structure

```text
slides/
├── index.html          # Main presentation file
├── spec.md             # The original storyline and talk track
├── README.md           # This file
└── assets/
    ├── images/         # High-res hardware, chip, and lifestyle photos
    └── media/          # Cinematic background video loops (AlphaChip, Ironwood)
```

## 🛠️ Installation & Setup

Since this presentation uses modern web features like CSS transitions and local video assets, it must be served via a local web server to avoid browser security (CORS) restrictions.

### 1. Requirements
You only need a terminal and a web browser. No complex installation is required.

### 2. Running the Presentation
Navigate to the project directory in your terminal and start a local server using Python (pre-installed on most systems):

```bash
# Navigate to the folder
cd /path/to/your/folder/slides

# Start the server
python3 -m http.server 8000
```

### 3. Viewing the Slides
Open your browser and navigate to:
**[http://localhost:8000](http://localhost:8000)**

## ⌨️ Presentation Controls

- **Advance Slide:** Spacebar, Right Arrow, or Mouse Click.
- **Previous Slide:** Left Arrow.
- **Full Screen:** Press `F`.
- **Speaker Notes:** Press `S` to open the Speaker View (notes, timer, and next-slide preview).
- **Overview Mode:** Press `O` or `Esc` to see all slides at once.

## 📝 Customization

- **Fonts:** The presentation uses Google Fonts (Inter, Jost, Barlow).
- **Styling:** Keynote-style adjustments (drop shadows, overlays, and animations) are defined in the `<style>` block of `index.html`.
- **Media:** Images can be swapped by replacing the files in `assets/images/`.

---
*Created for the APAC Google TPU Innovation Keynote.*
