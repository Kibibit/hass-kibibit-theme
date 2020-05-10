<p align="center">
  <a href="https://github.com/Kibibit/hass-kibibit-theme/" target="blank"><img src="hassio-theme-logo.png" width="200" alt="achievibit Logo" />
  </a>
  <h2 align="center">
    @kibibit/hass-kibibit-theme
  </h2>
</p>
<p align="center">
  <a href="https://github.com/custom-components/hacs"><img src="https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge"></a>
</p>
<p align="center">
  A milky glass theme for Home Assistant
</p>
<hr>

This is based on [Henrik](https://www.reddit.com/user/Trollet_/)'s [reddit post](https://www.reddit.com/r/homeassistant/comments/c4s28m/my_current_lovelace_ui_constructive_feedback_is/) with a few additions of mine


## Installation

### Prerequisites

Add the following code to your `configuration.yaml` file (reboot required).

```yaml
frontend:
  ... # your configuration.
  themes: !include_dir_merge_named themes
  ... # your configuration.
```

### Add the font
Right now, this theme requires you to add the `Comfortaa` font as a resource to your lovelace configuration:
```yaml
resources:
  - url: https://fonts.googleapis.com/css?family=Comfortaa&display=swap
  type: css
```

### HACS

1. Go to the Community Store.
2. Search for `kibibit`.
3. Navigate to `kibibit` theme.
4. Press `Install`.
6. Go to services and trigger the `frontend.reload_themes` service.

### Manual

Clone this repository in your existing (or create it) `themes/` folder.

```bash
cd themes/
git clone https://github.com/Kibibit/hass-kibibit-theme.git
```

Or using submodules:

```bash
cd themes/
git submodule add https://github.com/Kibibit/hass-kibibit-theme.git
```

## Screenshots
![Theme - Overview](/screenshots/dashboard-example.png)

## Stay in touch

- Author - [Neil Kalman](https://github.com/thatkookooguy)
- Website - [https://github.com/kibibit](https://github.com/kibibit)
- StackOverflow - [thatkookooguy](https://stackoverflow.com/users/1788884/thatkookooguy)
- Twitter - [@thatkookooguy](https://twitter.com/thatkookooguy)
- Twitter - [@kibibit_opensrc](https://twitter.com/kibibit_opensrc)
