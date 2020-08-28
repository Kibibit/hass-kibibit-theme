<p align="center">
  <a href="https://github.com/Kibibit/hass-kibibit-theme/" target="blank"><img src="https://thatkookooguy.github.io/https-assets/hassio-theme-logo.png" width="200" alt="achievibit Logo" />
  </a>
  <h2 align="center">
    @kibibit/hass-kibibit-theme
  </h2>
</p>
<p align="center">
  <a href="https://github.com/custom-components/hacs"><img src="https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge"></a>
  <a href="https://imgur.com/gallery/SQJNbWb"><img src="https://img.shields.io/badge/Screenshots-Click_Here-ff3860.svg?style=for-the-badge"></a>
</p>
<p align="center">
  A milky glass theme for Home Assistant
</p>
<hr>

This is based on [Henrik](https://www.reddit.com/user/Trollet_/)'s [reddit post](https://www.reddit.com/r/homeassistant/comments/c4s28m/my_current_lovelace_ui_constructive_feedback_is/) with a few additions of mine

## Screenshots
![Theme - Overview](https://thatkookooguy.github.io/https-assets/dashboard-example.png)
![Theme - mobile](https://thatkookooguy.github.io/https-assets/mobile.png)

[more screenshots](https://imgur.com/gallery/SQJNbWb)

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

### Change the background

This theme comes with a background by default, but you can change it to whatever you like.

You can use either a url or a local file.

1. Find a background you like (You can fetch the original one from [HERE](https://thatkookooguy.github.io/https-assets/bg-kibibit-theme.png))
2. If it's a local image, put the background image inside `/config/www` to make it a public asset accessible from the frontend (`/config/www/bg-kibibit-theme.png`).

access the theme file `kibibit.yaml` and change the following line:

```yaml
background-image: "center / cover no-repeat fixed url('https://thatkookooguy.github.io/https-assets/bg-kibibit-theme.png')"
```

to include your url, or a local asset by mapping `/config/www/` to `/local/` (`/local/bg-kibibit-theme.png`)

Refresh home assistant after that.

### Setting the default `backend-selected` theme
In order to have this theme set automatically as the backend selected default, add the following automation to your home assistant:
```yaml
- alias: Set Default Theme
  description: ''
  trigger:
  - event: start
    platform: homeassistant
  condition: []
  action:
  - data:
      name: kibibit
    service: frontend.set_theme
```

## Stay in touch

- Author - [Neil Kalman](https://github.com/thatkookooguy)
- Website - [https://github.com/kibibit](https://github.com/kibibit)
- StackOverflow - [thatkookooguy](https://stackoverflow.com/users/1788884/thatkookooguy)
- Twitter - [@thatkookooguy](https://twitter.com/thatkookooguy)
- Twitter - [@kibibit_opensrc](https://twitter.com/kibibit_opensrc)
