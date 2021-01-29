<p align="center">
  <a href="https://github.com/Kibibit/hass-kibibit-theme/" target="blank"><img src="https://thatkookooguy.github.io/https-assets/hassio-theme-logo.png" width="200" alt="achievibit Logo" />
  </a>
  <h2 align="center">
    @kibibit/hass-kibibit-theme
  </h2>
</p>
<p align="center">
  <a href="https://www.npmjs.com/package/@kibibit/hass-kibibit-theme"><img src="https://img.shields.io/npm/v/@kibibit/hass-kibibit-theme/latest.svg?style=for-the-badge&logo=npm&color=CB3837"></a>
</p>
<p align="center">
  <a href="https://github.com/custom-components/hacs"><img src="https://img.shields.io/badge/HACS-Default-orange.svg?style=flat-square"></a>
    <!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors-"><img src="https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square" alt="All Contributors"></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
  <a href="https://imgur.com/gallery/SQJNbWb"><img src="https://img.shields.io/badge/Screenshots-Click_Here-ff3860.svg?style=flat-square"></a>
</p>
<p align="center">
  A milky glass theme for Home Assistant
</p>
<hr>

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

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://thatkookooguy.kibibit.io/"><img src="https://avatars3.githubusercontent.com/u/10427304?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Neil Kalman</b></sub></a><br /><a href="https://github.com/kibibit/hass-kibibit-theme/commits?author=Thatkookooguy" title="Code">💻</a> <a href="https://github.com/kibibit/hass-kibibit-theme/commits?author=Thatkookooguy" title="Documentation">📖</a> <a href="#design-Thatkookooguy" title="Design">🎨</a> <a href="#infra-Thatkookooguy" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#maintenance-Thatkookooguy" title="Maintenance">🚧</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

## Credits

This theme started based on this post [Henrik](https://www.reddit.com/user/Trollet_/)'s [reddit post](https://www.reddit.com/r/homeassistant/comments/c4s28m/my_current_lovelace_ui_constructive_feedback_is/).

Learned a lot about lovelace themes from the [lovelace ios themes repo](https://github.com/basnijholt/lovelace-ios-themes)!
Check their themes out!

## Stay in touch

- Author - [Neil Kalman](https://github.com/thatkookooguy)
- Website - [https://github.com/kibibit](https://github.com/kibibit)
- StackOverflow - [thatkookooguy](https://stackoverflow.com/users/1788884/thatkookooguy)
- Twitter - [@thatkookooguy](https://twitter.com/thatkookooguy)
- Twitter - [@kibibit_opensrc](https://twitter.com/kibibit_opensrc)
