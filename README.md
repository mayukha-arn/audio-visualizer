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