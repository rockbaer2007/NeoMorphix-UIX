# NeuMorphix

[![Open your Home Assistant instance and add this repository to HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=rockbaer2007&repository=NeumorphixHome&category=theme)

A neumorphic theme for [Home Assistant](https://www.home-assistant.io/) that brings soft shadows, rounded surfaces, and a tactile 3D feel to your dashboards.

NeuMorphix ships with **12 theme variants** across two styles and two styling engines:

| Style | card-mod Light | card-mod Dark | card-mod Claude | UIX Light | UIX Dark | UIX Claude |
|-------|----------------|---------------|-----------------|-----------|----------|------------|
| **Raised** | `neumorphix-light` | `neumorphix-dark` | `neumorphix-claude` | `neumorphix-light-uix` | `neumorphix-dark-uix` | `neumorphix-claude-uix` |
| **Inset** | `neumorphix-light-inset` | `neumorphix-dark-inset` | `neumorphix-claude-inset` | `neumorphix-light-uix-inset` | `neumorphix-dark-uix-inset` | `neumorphix-claude-uix-inset` |

- **Raised** variants give cards and elements a soft, extruded look — the classic neumorphic style.
- **Inset** variants flip the effect so elements appear pressed into the surface.

> [!NOTE]
> **Inset themes and the Settings page**
>
> The inset theme variants do not apply to the main Settings page. The Settings page is part of Home Assistant's core UI and is rendered differently from dashboard views, which means theme tools like card-mod or UIX may not reach it. Every other page — including all dashboard views and all Settings sub-pages — themes correctly.

## Prerequisites

- **Home Assistant** 2023.9.0 or newer
- **[card-mod](https://github.com/thomasloven/lovelace-card-mod)** or **[UIX](https://github.com/Lint-Free-Technology/uix)** — install your preferred styling engine through HACS before installing NeuMorphix

## Installation

### HACS (recommended)

1. Open HACS in your Home Assistant instance.
2. Go to **Frontend** (the three-dot menu in the top right).
3. Select **Custom repositories**.
4. Add the URL of this repository and choose **Theme** as the category.
5. Search for **NeuMorphix** in HACS and install it.
6. Restart Home Assistant.

### Manual

1. Download the `themes/` folder from this repository.
2. Copy the theme files you want to use into your Home Assistant `config/themes/` directory.
3. Restart Home Assistant.

## Configuration

Make sure your `configuration.yaml` includes the frontend integration with the required resource.

For card-mod themes:

```yaml
frontend:
  themes: !include_dir_merge_named themes
  extra_module_url:
    - /hacsfiles/lovelace-card-mod/card-mod.js
```

For UIX themes, install UIX and add the UIX resource according to the UIX documentation.

After restarting, go to **Settings → General** and pick a NeuMorphix variant from the **Theme** dropdown — or set it per-dashboard in the dashboard settings.

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
- `neumorphix-light-uix` — light raised neumorphic for UIX
- `neumorphix-dark-uix` — dark raised neumorphic for UIX
- `neumorphix-claude-uix` — claude-inspired raised neumorphic for UIX
- `neumorphix-light-uix-inset` — light inset neumorphic for UIX
- `neumorphix-dark-uix-inset` — dark inset neumorphic for UIX
- `neumorphix-claude-uix-inset` — claude-inspired inset neumorphic for UIX

## License

MIT
