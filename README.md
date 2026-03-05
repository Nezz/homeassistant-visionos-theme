# visionOS & iOS 26 Liquid Glass Theme

Theme inspired by visionOS for Home Assistant with automatic dark mode support.

### visionOS
<img width="500" alt="vision-light" src="https://github.com/user-attachments/assets/f054c59e-7198-4476-9a2e-4e0caec49df8" /><img width="500" alt="vision-dark" src="https://github.com/user-attachments/assets/61179b34-d25b-4902-9883-91156f5dc659" />

### Liquid Glass
<img width="500" alt="ios-light" src="https://github.com/user-attachments/assets/c60d760b-4531-41c2-b8b5-47404e8743d7" /><img width="500" alt="ios-dark" src="https://github.com/user-attachments/assets/273f0e86-180e-42b3-abe0-bab25c359584" />

## Installation

1. You can install the theme with [HACS](https://hacs.xyz/docs/setup/download):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Nezz&repository=homeassistant-visionos-theme&category=theme)

> [!NOTE]  
> Install the [`uix`](https://github.com/Lint-Free-Technology/uix) integration via HACS to make the sidebar transparent. It's a drop-in replacement for card-mod with backwards compatibility.

2. You should see the "Liquid Glass" and "visionos" themes appear in your list of themes.

If it's missing, try reloading your themes or adding the following code to your `configuration.yaml` file (reboot required):

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. (Optional) You can set this as the default theme with the following automation:
```
alias: Frontend - Change theme
trigger:
  - platform: homeassistant
    event: start
action:
  - service: frontend.set_theme
    data:
      name: visionos
```

## Remarks

Sample dashboard configuration from the themes is available [here](https://github.com/Nezz/homeassistant-visionos-theme/blob/sample/sample.yaml)

Based on [Bas Nijholt's iOS Themes](https://github.com/basnijholt/lovelace-ios-themes)

Dropdown fixes from [Wessam Lauf's Frosted Glass Theme](https://github.com/wessamlauf/homeassistant-frosted-glass-themes)
