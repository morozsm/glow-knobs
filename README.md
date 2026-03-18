# 🎛 glow-knobs

Instrument panel controls for **Svelte 5** — knobs with arc glow, LED indicator buttons, gradient bars, drag-to-adjust values. Zero dependencies.

> **Status: In Development** — Components are being built inside [icom-lan](https://github.com/morozsm/icom-lan) (a web-based radio transceiver control app) and will be extracted here when stable.

## Components (planned)

### ValueControl — One core, many renderers

| Renderer | Description | Use case |
|----------|-------------|----------|
| **HBar** | Horizontal bar with fill + gradient | AF gain, RF gain, levels |
| **Bipolar** | Centered ± bar | PBT, IF shift, RIT offset |
| **Knob** | SVG rotary with arc glow ✨ | Any rotary parameter |
| **VBar** | Vertical bar | Equalizer, level meters |

All renderers share the same interaction model:
- 🖱 **Drag** to adjust (horizontal or vertical)
- 🔄 **Scroll wheel** for fine control
- ⌨️ **Arrow keys** when focused
- ⇧ **Shift** = fine adjust (÷10)
- 🔘 **Double-click** = reset to default
- 📱 **Touch** with pointer capture

### Knob Features

- **Arc glow** — filled sector glows proportionally to value
- **Gradient fill** — multi-stop color gradients along the arc
- **Configurable glow** — blur radius, spread, opacity, intensity scaling
- **Tick marks** with optional labels
- **Sweep angle** — 270° default, configurable

### ControlButton — LED indicator styles

| Style | Visual |
|-------|--------|
| `ring` | Border glow (default) |
| `dot` | LED indicator dot (like hardware) |
| `edge-bottom` | Bottom edge glow |
| `edge-left` | Left edge glow |
| `edge-sides` | Left + right edge glow |
| `fill` | Background fill glow |

**6 color tokens:** cyan, green, amber, red, orange, white — plus custom via CSS variable.

### Also included

- **SegmentedButton** — radio-group selector
- **TuningWheel** — horizontal jog dial with momentum

## Design goals

- 🎨 **Instrument-panel aesthetics** — dark theme, glow effects, professional look
- 🧩 **Svelte 5** runes (`$props`, `$derived`, `$effect`)
- 📦 **Zero dependencies** — pure Svelte + SVG + CSS
- 🎯 **Channel theming** — CSS variables for multi-channel color coding
- ♿ **Accessible** — ARIA slider attributes, keyboard navigation
- 📱 **Mobile-first** — touch, haptics, pointer capture

## Target audience

- 📻 Ham radio / SDR control panels
- 🎵 Audio / DAW — mixer controls, synth knobs
- 🌡 IoT dashboards — sensor displays, actuator controls
- 🔬 Lab equipment — instrument panels
- ✈️ Simulators — cockpit instruments

## License

MIT © 2026 Sergey Morozik
