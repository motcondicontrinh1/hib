---
version: "alpha"
name: "Bio Signal Tracking"
description: "Bio Signal Pricing Section is designed for comparing plans and supporting conversion decisions. Key features include plan comparison blocks and conversion-oriented actions. It is suitable for subscription pricing pages and plan comparison experiences."
colors:
  primary: "#C9F365"
  secondary: "#8CCF2E"
  tertiary: "#B5DB58"
  neutral: "#D4D4D4"
  background: "#C9F365"
  surface: "#C9F365"
  text-primary: "#D4D4D4"
  text-secondary: "#FFFFFF"
  border: "#8CCF2E"
  accent: "#C9F365"
typography:
  display-lg:
    fontFamily: "Inter"
    fontSize: "48px"
    fontWeight: 400
    lineHeight: "50.400002px"
    letterSpacing: "-0.025em"
  body-md:
    fontFamily: "Inter"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: "29.25px"
  label-md:
    fontFamily: "Inter"
    fontSize: "16px"
    fontWeight: 500
    lineHeight: "24px"
rounded:
  md: "0px"
  full: "9999px"
spacing:
  base: "4px"
  sm: "4px"
  md: "8px"
  lg: "10px"
  xl: "14px"
  gap: "4px"
  card-padding: "8px"
  section-padding: "24px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#000000"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: "14px"
  button-link:
    textColor: "{colors.tertiary}"
    rounded: "{rounded.md}"
    padding: "0px"
  card:
    backgroundColor: "{colors.primary}"
    rounded: "{rounded.full}"
    padding: "23px"
---

## Overview

- **Composition cues:**
  - Layout: Flex
  - Framing: Open
  - Grid: Minimal

## Colors

The color system uses dark mode with #C9F365 as the main accent and #D4D4D4 as the neutral foundation.

- **Primary (#C9F365):** Main accent and emphasis color.
- **Secondary (#8CCF2E):** Supporting accent for secondary emphasis.
- **Tertiary (#B5DB58):** Reserved accent for supporting contrast moments.
- **Neutral (#D4D4D4):** Neutral foundation for backgrounds, surfaces, and supporting chrome.

- **Usage:** Background: #C9F365; Surface: #C9F365; Text Primary: #D4D4D4; Text Secondary: #FFFFFF; Border: #8CCF2E; Accent: #C9F365

## Typography

Typography relies on Inter across display, body, and utility text.

- **Display (`display-lg`):** Inter, 48px, weight 400, line-height 50.400002px, letter-spacing -0.025em.
- **Body (`body-md`):** Inter, 18px, weight 400, line-height 29.25px.
- **Labels (`label-md`):** Inter, 16px, weight 500, line-height 24px.

## Layout

Layout follows a flex composition with reusable spacing tokens. Preserve the flex structural frame before changing ornament or component styling. Use 4px as the base rhythm and let larger gaps step up from that cadence instead of introducing unrelated spacing values.

Treat the page as a flex composition, and keep that framing stable when adding or remixing sections.

- **Layout type:** Flex
- **Base unit:** 4px
- **Scale:** 4px, 8px, 10px, 14px, 24px, 32px, 40px, 48px
- **Section padding:** 24px, 68px
- **Card padding:** 8px, 24px
- **Gaps:** 4px, 8px, 12px, 32px

## Elevation & Depth

Depth is communicated through elevated, border contrast, and reusable shadow or blur treatments. Keep those recipes consistent across hero panels, cards, and controls so the page reads as one material system.

Surfaces should read as elevated first, with borders, shadows, and blur only reinforcing that material choice.

- **Surface style:** Elevated
- **Borders:** 1px #8CCF2E
- **Shadows:** rgba(201, 243, 101, 0.6) 0px 0px 45px -10px

## Shapes

Shapes rely on a tight radius system anchored by 9999px and scaled across cards, buttons, and supporting surfaces. Icon geometry should stay compatible with that soft-to-controlled silhouette.

Use the radius family intentionally: larger surfaces can open up, but controls and badges should stay within the same rounded DNA instead of inventing sharper or pill-only exceptions.

- **Corner radii:** 9999px
- **Icon treatment:** Linear
- **Icon sets:** Solar

## Components

Anchor interactions to the detected button styles. Reuse the existing card surface recipe for content blocks.

### Buttons
- **Primary:** background #C9F365, text #000000, radius 9999px, padding 14px, border 0px solid rgb(229, 231, 235).
- **Links:** text #B5DB58, radius 0px, padding 0px, border 0px solid rgb(229, 231, 235).

### Cards and Surfaces
- **Card surface:** background #C9F365, border 0px solid rgb(229, 231, 235), radius 9999px, padding 23px, shadow rgba(201, 243, 101, 0.6) 0px 0px 45px -10px.

### Iconography
- **Treatment:** Linear.
- **Sets:** Solar.

## Do's and Don'ts

Use these constraints to keep future generations aligned with the current system instead of drifting into adjacent styles.

### Do
- Do use the primary palette as the main accent for emphasis and action states.
- Do keep spacing aligned to the detected 4px rhythm.
- Do reuse the Elevated surface treatment consistently across cards and controls.
- Do keep corner radii within the detected 9999px family.

### Don't
- Don't introduce extra accent colors outside the core palette roles unless the page needs a new semantic state.
- Don't mix unrelated shadow or blur recipes that break the current depth system.
- Don't exceed the detected moderate motion intensity without a deliberate reason.

## Motion

Motion feels controlled and interface-led across text, layout, and section transitions. Timing clusters around 150ms. Easing favors ease and cubic-bezier(0.4. Hover behavior focuses on text and color changes. Scroll choreography uses GSAP ScrollTrigger and Parallax for section reveals and pacing.

**Motion Level:** moderate

**Durations:** 150ms

**Easings:** ease, cubic-bezier(0.4, 0, 0.2, 1)

**Hover Patterns:** text, color, transform

**Scroll Patterns:** gsap-scrolltrigger, parallax

## WebGL

Reconstruct the graphics as a ambient background using webgl, custom shaders. The effect should read as technical, meditative, and atmospheric: perspective grid field with black and sparse spacing. Build it from grid lines + depth fade so the effect reads clearly. Animate it as slow breathing pulse. Interaction can react to the pointer, but only as a subtle drift. Preserve dom fallback.

**Id:** webgl

**Label:** WebGL

**Stack:** WebGL

**Insights:**
  - **Scene:**
    - **Value:** Ambient background
  - **Effect:**
    - **Value:** Perspective grid field
  - **Primitives:**
    - **Value:** Grid lines + depth fade
  - **Motion:**
    - **Value:** Slow breathing pulse
  - **Interaction:**
    - **Value:** Pointer-reactive drift
  - **Render:**
    - **Value:** WebGL, custom shaders

**Techniques:** Perspective grid, Breathing pulse, Pointer parallax, Shader gradients, Noise fields

**Code Evidence:**
  - **HTML reference:**
    - **Language:** html
    - **Snippet:**
      ```html
      <!-- WebGL Background Canvas -->
      <canvas id="webgl-bg" class="fixed top-0 left-0 w-full h-full pointer-events-none z-0"></canvas>

      <div class="relative z-10 flex flex-col min-h-screen">
      ```
  - **JS reference:**
    - **Language:** js
    - **Snippet:**
      ```
      // --- WebGL Background Animation ---
      const canvas = document.getElementById('webgl-bg');
      const gl = canvas.getContext('webgl');

      if (gl) {
          // Resize canvas to fill window
          const resize = () => {
              canvas.width = window.innerWidth;
      ```
  - **Renderer setup:**
    - **Language:** js
    - **Snippet:**
      ```
      // --- WebGL Background Animation ---
      const canvas = document.getElementById('webgl-bg');
      const gl = canvas.getContext('webgl');

      if (gl) {
          // Resize canvas to fill window
          const resize = () => {
      ```
