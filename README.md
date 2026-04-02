# Bloom — Voice Flower Visualizer

A real-time audio-reactive web app that translates your voice into animated, parametric flowers. Speak, sing, or hum into your microphone and watch the visuals respond directly to your pitch, volume, and tone.

Built with plain HTML, CSS, and JavaScript using the Web Audio API. No libraries, no dependencies, no install required.

---

## What It Does

Bloom listens to your microphone and breaks your voice down into five frequency bands. Each band controls a different visual parameter, creating a near-simultaneous exchange between your sound and the shapes on screen.

| Frequency Band | Visual Effect |
|---|---|
| Bass (20–250 Hz) | Flower size, petal width, spiral spread |
| Low Mid (250–500 Hz) | Secondary petal shaping |
| Mid (500–2000 Hz) | Petal count, spiral density |
| High Mid (2000–4000 Hz) | Edge wobble, distortion, petal stretch |
| Treble (4000–20000 Hz) | Outline glow, particle brightness, line weight |
| Overall Volume | Rotation speed, opacity, particle burst rate |

The background shifts hue dynamically with bass and volume. Particles burst off the center flower when your voice crosses a volume threshold. When the mic is off or silent, a soft ghost flower animates on its own.

---

## Flower Types

Select a mode from the panel at the bottom of the screen.

**Rose** — A rhodonea (mathematical rose) curve. Petal count follows mid frequencies. Treble introduces edge warping across the curve.

**Daisy** — Elliptical petals arranged radially around a central disk. The disk pulses with bass; petal length stretches with mids.

**Lotus** — Three concentric layers of pointed petals, each layer driven by a different frequency band. Creates depth and complexity with sustained tones.

**Spiral** — Archimedean spiral arms that wobble with high-frequency content. Works especially well with sharp consonants or sibilant sounds.

**Auto** — Cycles through all four types continuously.

---

## How to Deploy on GitHub Pages

GitHub Pages serves the file over HTTPS, which is required for microphone access in modern browsers. This is the recommended way to run the project.

### Step 1 — Rename the file

Before uploading, rename `voice_flower_visualizer.html` to `index.html`. GitHub Pages will serve this as the root page automatically.

### Step 2 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon in the top right and select **New repository**
3. Give it a name (e.g. `bloom-visualizer`)
4. Set visibility to **Public**
5. Click **Create repository**

### Step 3 — Upload the file

On the new repository page:

1. Click **uploading an existing file**
2. Drag and drop `index.html` into the upload area
3. Scroll down and click **Commit changes**

### Step 4 — Enable GitHub Pages

1. Go to the repository's **Settings** tab
2. In the left sidebar, click **Pages**
3. Under **Branch**, select `main` and leave the folder as `/ (root)`
4. Click **Save**

### Step 5 — Open the live site

After about 30–60 seconds, GitHub Pages will publish the site. Your URL will be:

```
https://your-username.github.io/your-repo-name/
```

GitHub shows the exact URL at the top of the Pages settings page once it is live. Open it in Chrome or Firefox, click the mic button, and allow microphone access when prompted.

---

## Browser Requirements

- **Chrome** (recommended) or **Firefox**
- Microphone access must be allowed when prompted
- JavaScript must be enabled
- Works on desktop only — mobile mic support varies by browser

---

## Controls

| Control | Function |
|---|---|
| Mic button (circle) | Toggle microphone on/off |
| Rose / Daisy / Lotus / Spiral | Switch flower type |
| Auto | Cycle through all types automatically |
| Frequency bars | Real-time display of bass, low mid, mid, high mid, and treble levels |
| Volume / Pitch readout | Live display of overall volume and estimated pitch |

---

## Color Scheme

| Hex | Name | Usage |
|---|---|---|
| `#E5D9F2` | Lavender | Primary petal fill, text |
| `#A594F9` | Violet | Secondary petal fill, UI accents |
| `#7371FC` | Indigo | Deep petal tones, bass-driven elements |
| `#595758` | Charcoal | Background base |
| `#E8F8C1` | Mint | Outlines, particles, stamen glow, active states |

---

## Project Context

This was built for a media assignment exploring parametric and cybernetic models of interaction — specifically how a human voice can drive visual form in real time, rather than through sliders or manual input. The goal was a near-simultaneous feedback loop between sound and shape, where the human has agency through their voice alone.

Inspired by examples at [aklobucar.github.io/voice_patterning](https://aklobucar.github.io/voice_patterning/) and [aklobucar.github.io/advanced_cybernetic_audio](https://aklobucar.github.io/advanced_cybernetic_audio/).