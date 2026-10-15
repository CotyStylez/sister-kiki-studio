# Sister Kiki Creator Studio 🎀 — Insider Photo Editor Suite

Adds a dedicated, insider-grade **Photo Editor (`📸 Photos`)** as the fifth tool in Sister Kiki Creator Studio. It gives Kiki access to the exact styling secrets top celebrity creative directors and editorial retouchers use—distilled into simple, one-tap controls.

> [!IMPORTANT]
> **Confirmed Choices from Clarification**:
> - **The 5-Tool Bottom Navigation Bar**:
>   `🎬 Video` · `📸 Photos` · `🎙️ Voice` · `📜 Prompter` · `🎨 Covers`
> - **Insider Competitiveness (What the Best in the Business Use)**:
>   1. **Pro-Mist Diffusion Glow**: The signature Hollywood/fashion lens filter effect that diffuses specular highlights into a dreamy, glowing aura while keeping details crisp.
>   2. **Top Agency Color Emulsions (Pro Color Grading)**:
>      - *Portra 400 Warmth* (golden skin tones, creamy pastels)
>      - *Parisian Desat* (muted architectural chic, understated luxury)
>      - *Studio Flash Pop* (hard-edge flash, razor sharpness, deep contrast)
>      - *Copenhagen Clean* (clear blues, glass skin daylight clarity)
>      - *90s Amber Film* (warm analog nostalgic tones)
>      - *Noir Velvet* (editorial high-contrast monochrome)
>   3. **Organic Film Grain & Halation**: Natural 35mm textural grain slider that eliminates digital flatness.
>   4. **Golden Hour Warmth & Studio Flash**: Quick-tap lighting adjustments that mimic $5,000 studio lighting setups with one thumb.
> - **Seamless Workflow Integration**: Any photo edited in the Photo Studio can be downloaded directly to her Camera Roll in high resolution, or sent with one tap into the **Video Maker** or **Cover Designer**.

---

## 1. Overview & Core Concept

### What It Does
The new **Photo Editor** tool provides a professional darkroom and retouching studio right on Kiki's phone:
- **Upload / Snap**: Pick any photo from her device (or load one of the built-in sample looks).
- **Insider Lighting Levers**: Toggle Pro-Mist glow, adjust golden hour radiance, or add studio flash pop.
- **Agency Emulsion Filters**: 6 curated fashion agency color grades.
- **Film Grain & Texture**: Dial in natural 35mm film grain for an authentic editorial look.
- **Aspect Ratio Cropping**: Fast 1-tap framing for 9:16 (TikTok), 4:5 (Portrait Feed), and 1:1 (Square).
- **One-Tap Actions**: "Save to Camera Roll (High Res)" and "Send to Video Maker 🎬".

### Target Persona
- Kiki: An ambitious creator who wants her photos and stills to look like they were graded by a premier fashion house or top creative agency, without needing complex desktop software like Lightroom or Photoshop.

---

## 2. User Experience & Visual Design

### The 5 Modular Tool Stations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                      SISTER KIKI CREATOR SUITE 🎀                           │
│                                                                             │
│  [🎬 Video]      [📸 Photos]      [🎙️ Voice]      [📜 Prompter]  [🎨 Covers] │
│   Montage Maker   Insider Retouch  Sound Booth     Teleprompter   Thumbnails│
└─────────────────────────────────────────────────────────────────────────────┘
```

### The Photo Editor Layout (`📸 Photos`)
1. **Photo Canvas & Live Before/After Preview**:
   - High-definition canvas showing real-time filter, glow, and grain adjustments.
   - Long-press or tap "Compare" button to instantly view the unedited original photo vs. her styled edit.
2. **Insider Emulsion Carousel**:
   - 6 Tap-to-Apply Presets:
     - 🌸 *Portra Warmth*: Creamy skin glow & soft highlights.
     - 📸 *Studio Flash*: Punchy high-contrast flash aesthetic.
     - 🌹 *Parisian Chic*: Muted cool greens & effortless neutral tones.
     - ✨ *Copenhagen Clean*: Glass skin, airy daylight, crisp sharpness.
     - 🎞️ *90s Film*: Sepia film grain & nostalgic tones.
     - 🖤 *Noir Velvet*: Rich high-fashion black and white.
3. **Insider Light & Texture Levers (Simple Sliders)**:
   - **Pro-Mist Glow** (0–100%): Diffuses highlights into a dreamy soft glow.
   - **Golden Warmth** (-50% to +50%): Warms up or cools down skin tones.
   - **Film Grain** (0–100%): Adds authentic analog 35mm grain.
   - **Studio Contrast** (0–100%): Dials in runway punch.
4. **Fast Export & Sharing**:
   - **"Download Photo (Camera Roll) 🎀"**: High-resolution PNG.
   - **"Send to Video Maker 🎬"**: Injects her freshly edited photo directly into her current video project!

---

## 3. Technical Architecture & Component Mapping

### Canvas 2D Shader Engine
- Multi-pass canvas rendering:
  1. Base photo draw with scaling and aspect ratio framing.
  2. Color matrix adjustment (saturation, brightness, warmth balance).
  3. Pro-Mist bloom pass: draws an offscreen blurred copy using `screen` or `lighten` blend mode to bloom the specular highlights.
  4. Procedural film grain pass: generates randomized micro-noise using pixel manipulation for authentic film grain.
- Performance: Instant 60 FPS slider responsiveness entirely in the client-side browser.
