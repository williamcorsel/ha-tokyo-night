# Tokyo Night for Home Assistant

[![Open your Home Assistant instance and open this repository in HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=williamcorsel&repository=ha-tokyo-night&category=theme)

The [Tokyo Night](https://github.com/tokyo-night/tokyo-night-vscode-theme) colour scheme as Home Assistant themes. The colours come from the [tokyonight.nvim](https://github.com/folke/tokyonight.nvim) palette, which also has the Moon and Day styles.

The repository contains three themes. Each one has a dark and a light mode:

| Theme | Dark mode | Light mode |
|---|---|---|
| Tokyo Night | Night | Day |
| Tokyo Night Storm | Storm | Day |
| Tokyo Night Moon | Moon | Day |

## Screenshots

**Tokyo Night** (dark mode)

![Tokyo Night](images/night.png)

**Tokyo Night Storm** (dark mode)

![Tokyo Night Storm](images/storm.png)

**Tokyo Night Moon** (dark mode)

![Tokyo Night Moon](images/moon.png)

**Day** (light mode of all three themes)

![Tokyo Night Day](images/day.png)

## Installation

### HACS (recommended)

1. Click the **Open your Home Assistant instance** button above. If the button does not work, open HACS, select **⋮ → Custom repositories**, and add `https://github.com/williamcorsel/ha-tokyo-night` with the type **Theme**.
2. Download **Tokyo Night** in HACS.
3. Go to **Tools → Actions** and run `frontend.reload_themes`, or restart Home Assistant. Before Home Assistant 2026.8, **Tools** is called **Developer tools**.

### Manual

1. Copy `themes/tokyo-night.yaml` to the `themes` folder in your Home Assistant configuration folder.
2. Reload the themes as in step 3 of the HACS steps.

### Theme folder setup

Home Assistant only loads themes from the `themes` folder if your `configuration.yaml` contains:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

If you add this line, restart Home Assistant once.

## Usage

1. Select your name at the bottom of the sidebar to open your profile.
2. Under **Theme**, select **Tokyo Night**, **Tokyo Night Storm**, or **Tokyo Night Moon**.
3. Select **Auto**, **Light**, or **Dark**. **Auto** follows the setting of your device.

To use a theme for all users, run the `frontend.set_theme` action:

```yaml
action: frontend.set_theme
data:
  name: Tokyo Night
  mode: dark
```

## Credits

- Enkia made the original [Tokyo Night](https://github.com/tokyo-night/tokyo-night-vscode-theme) theme for Visual Studio Code (MIT License).
- [tokyonight.nvim](https://github.com/folke/tokyonight.nvim) by Folke Lemaitre is the Neovim port that added the Moon and Day styles. The colour values in this repository come from its palette (Apache License 2.0).
