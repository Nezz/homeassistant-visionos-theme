# iOS 27 & visionOS Liquid Glass Theme

Theme inspired by Apple for Home Assistant with automatic dark mode support.

### Liquid Glass
<img width="500" alt="liquid-glass-light" src="https://github.com/user-attachments/assets/d1dda7ee-d5af-48b0-aafa-054afd86e505" /><img width="500" alt="liquid-glass-dark" src="https://github.com/user-attachments/assets/94b24d47-8cac-43c0-9ded-e809016cbbca" />

### Liquid Glass Tinted
<img width="500" alt="liquid-glass-tinted-light" src="https://github.com/user-attachments/assets/40bcd9c9-1f92-47b8-a691-fcb9fd91a0ad" /><img width="500" alt="liquid-glass-tinted-dark" src="https://github.com/user-attachments/assets/e321ef1b-53be-4d18-ad8e-48b1271d3158" />

### visionOS
<img width="500" alt="visionos-light" src="https://github.com/user-attachments/assets/3e01e281-1564-4d17-9a51-be80751e019a" /><img width="500" alt="visionos-dark" src="https://github.com/user-attachments/assets/a179d0d5-4c36-4503-b9d9-96bcd50b87f2" />

## Installation

1. You can install the theme with [HACS](https://hacs.xyz/docs/use/download/download/):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Nezz&repository=homeassistant-visionos-theme&category=theme)

> [!NOTE]  
> Install the [`uix`](https://github.com/Lint-Free-Technology/uix) integration via HACS to make the sidebar transparent. It's a drop-in replacement for card-mod with backwards compatibility. After installing, don't forget to [add the integration for it](https://uix.lf.technology/quick-start/#add-ui-extension-service).

2. You should see the "Liquid Glass", "Liquid Glass Tinted" and "visionos" themes appear in your list of themes.

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
