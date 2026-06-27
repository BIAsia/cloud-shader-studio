# Cloud Shader Studio

A single-file WebGL editor that recreates Figma's **Clouds** shader fill, with a
Start → End animation timeline and a configurable soft-light overlay.

No build step, no dependencies — just open `index.html` (or serve the folder).

## Features

- **Cloud shader** based on the well-known [2D Clouds by drift](https://www.shadertoy.com/view/4tdSWr)
  (simplex fBm + ridged detail), mapped to Figma's parameters:
  Cloud / Shadow color, 3-stop Sky gradient, Coverage, Density, Brightness, Detail,
  Variation, Warp, Stretch, Phase, Churn, and Transform (Scale / Offset / Angle).
- **Start / End keyframes** with linear interpolation and a scrubbable timeline.
- **Motion**: Phase drives a 45° diagonal drift; **Churn** controls the per-octave
  turbulence (0 = clean drift, higher = more morphing).
- **Seamless loop**: a crossfade loop keeps the exact motion trajectory while making
  the animation head-to-tail seamless.
- **Overlay layer** on top of the clouds — gradient or uploaded image, with a blend
  mode (default **Soft light**), angle, and opacity — mirroring Figma's layer model.
- **Light / Dark** theme toggle (light by default).

## Usage

```bash
npx serve .
# then open the printed URL
```

Toggle **Start** / **End** to edit each keyframe with the sliders; press **Play**
(or scrub) to preview the morph. Use **Copy keyframe** to export the current values
as JSON.

## License

MIT
