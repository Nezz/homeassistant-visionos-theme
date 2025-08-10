# visionOS & iOS 26 Liquid Glass Theme

Theme inspired by visionOS for Home Assistant with automatic dark mode support.

### visionOS
<img width="500" alt="vision light" src="https://github.com/user-attachments/assets/37b0c69a-c876-4d13-ac05-e48ccc178785" /><img width="500" alt="vision dark" src="https://github.com/user-attachments/assets/908e3338-6573-4a9c-b483-90e352e9977c" />

### Liquid Glass
<img width="500" alt="ios light" src="https://github.com/user-attachments/assets/dde7aa13-2dad-42f6-8239-3ffa7fe2477b" /><img width="500" alt="ios dark" src="https://github.com/user-attachments/assets/13e3f550-5935-4cc6-825f-ae1bf90d1070" />

## Installation

1. You can install the theme with [HACS](https://hacs.xyz/docs/setup/download):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Nezz&repository=homeassistant-visionos-theme&category=theme)

> [!NOTE]  
> Install the [`card-mod`](https://github.com/thomasloven/lovelace-card-mod) integration via HACS to fix issues with dropdowns.

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

Based on [Bas Nijholt's iOS Themes](https://github.com/basnijholt/lovelace-ios-themes)
Dropdown fixes from [Wessam Lauf's Frosted Glass Theme](https://github.com/wessamlauf/homeassistant-frosted-glass-themes)
