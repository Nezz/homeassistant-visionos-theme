# iOS 27 & visionOS Liquid Glass Theme

Theme inspired by Apple for Home Assistant with automatic dark mode support.

### Liquid Glass
<img width="500" alt="liquid-glass-light" src="https://github.com/user-attachments/assets/83e3e2c9-f010-4480-a1a2-b8eea7d53f05" /><img width="500" alt="liquid-glass-dark" src="https://github.com/user-attachments/assets/741a5ec0-3863-4e6d-a0a4-0311b61166de" />

### Liquid Glass Tinted
<img width="500" alt="liquid-glass-tinted-light" src="https://github.com/user-attachments/assets/8fe13210-44ea-4250-8c30-24ce139b2e8d" /><img width="500" alt="liquid-glass-tinted-dark" src="https://github.com/user-attachments/assets/0c69a322-3b7e-42d9-a342-cc5a25d5c706" />

### visionOS
<img width="500" alt="visionos-light" src="https://github.com/user-attachments/assets/67cb1dbb-e433-44e1-bce4-249cd606ecb5" /><img width="500" alt="visionos-dark" src="https://github.com/user-attachments/assets/49527a0a-9353-46eb-b2a3-6d421b993386" />

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
