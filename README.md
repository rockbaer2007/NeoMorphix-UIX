# NeoMorphix UIX

[![Open your Home Assistant instance and add this repository to HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=rockbaer2007&repository=NeoMorphix-UIX&category=theme)

A neumorphic theme for [Home Assistant](https://www.home-assistant.io/) that brings soft shadows, rounded surfaces, and a tactile 3D feel to your dashboards.

NeuMorphix ships with **6 original card-mod variants**. This branch additionally adds **6 NeoMorphix UIX variants**:

| Style | card-mod Light | card-mod Dark | card-mod Claude | UIX Light | UIX Dark | UIX Claude |
|-------|----------------|---------------|-----------------|-----------|----------|------------|
| **Raised** | `neumorphix-light` | `neumorphix-dark` | `neumorphix-claude` | `NeoMorphix UIX Light` | `NeoMorphix UIX Dark` | `NeoMorphix UIX Claude` |
| **Inset** | `neumorphix-light-inset` | `neumorphix-dark-inset` | `neumorphix-claude-inset` | `NeoMorphix UIX Light Inset` | `NeoMorphix UIX Dark Inset` | `NeoMorphix UIX Claude Inset` |

- **Raised** variants give cards and elements a soft, extruded look — the classic neumorphic style.
- **Inset** variants flip the effect so elements appear pressed into the surface.

> [!NOTE]
> **Inset themes and the Settings page**
>
> The inset theme variants do not apply to the main Settings page. The Settings page is part of Home Assistant's core UI and is rendered differently from dashboard views, which means theme tools like card-mod or UIX may not reach it. Every other page — including all dashboard views and all Settings sub-pages — themes correctly.

## Prerequisites

- **Home Assistant** 2023.9.0 or newer
- **[UIX](https://github.com/Lint-Free-Technology/uix)** — install UIX through HACS before installing NeoMorphix UIX

## Installation

### HACS (recommended)

1. Open HACS in your Home Assistant instance.
2. Go to **Frontend** (the three-dot menu in the top right).
3. Select **Custom repositories**.
4. Add the URL of this repository and choose **Theme** as the category.
5. Search for **NeoMorphix UIX** in HACS and install it.
6. Restart Home Assistant.

### Manual

1. Download the `themes/` folder from this repository.
2. Copy the theme files you want to use into your Home Assistant `config/themes/` directory.
3. Restart Home Assistant.

## Configuration

Make sure your `configuration.yaml` includes the frontend integration and the UIX resource according to the UIX documentation.

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

The original NeuMorphix theme files still target card-mod. NeoMorphix UIX uses the additional `NeoMorphix UIX ...` theme variants.

After restarting, go to **Settings → General** and pick a NeoMorphix UIX variant from the **Theme** dropdown — or set it per-dashboard in the dashboard settings.

## Screenshots

### Light
![neumorphix-light](screenshots/NeuMorphix%20Light.png)
![neumorphix-light-inset](screenshots/NeuMorphix%20Light%20Inset.png)

### Dark
![neumorphix-dark](screenshots/NeuMorphix%20Dark.png)
![neumorphix-dark-inset](screenshots/NeuMorphix%20Dark%20Inset.png)

### Claude
![neumorphix-claude](screenshots/NeuMorphix%20Claude.png)
![neumorphix-claude-inset](screenshots/NeuMorphix%20Claude%20Inset.png)

## Theme variants

- `neumorphix-light` — light raised neumorphic
- `neumorphix-dark` — dark raised neumorphic
- `neumorphix-claude` — claude-inspired raised neumorphic
- `neumorphix-light-inset` — light inset neumorphic
- `neumorphix-dark-inset` — dark inset neumorphic
- `neumorphix-claude-inset` — claude-inspired inset neumorphic
- `NeoMorphix UIX Light` — light raised neumorphic for UIX
- `NeoMorphix UIX Dark` — dark raised neumorphic for UIX
- `NeoMorphix UIX Claude` — claude-inspired raised neumorphic for UIX
- `NeoMorphix UIX Light Inset` — light inset neumorphic for UIX
- `NeoMorphix UIX Dark Inset` — dark inset neumorphic for UIX
- `NeoMorphix UIX Claude Inset` — claude-inspired inset neumorphic for UIX

## License

MIT
