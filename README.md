# Lovelace Todoist List card



## Configuration options

| Key | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `title` | `string` | `False` | - | Desired title of a card |
| `entity` | `string` | `True` | - | ID of Google Keep sensor |
| `theme` | `string` | `False` | `light` | Theme to be used for notes. Possible values: `light`, `dark`, `auto` |
| `alpha` | `float` | `False` | 1 | Level of transparency used for notes (0 - fully transparent, 1 - not transparent) |
| `show` | `list` | `True` | - | List of sections that should be displayed. Possible values: `checked`, `unchecked` |
| `hide_if_empty` | `boolean` | `False` | `false` | Enables hiding cart when there are no notes found. Possible values: `true`, `false` |
| `system_box` | `boolean` | `False` | `false` | Make each note a HA tile instead of encapsulating them into a HA tile |
| `force_background` | `boolean` | `False` | `false` | Force the background to white/black according to the theme |
| `small_title_margin` | `boolean` | `False` | `false` | Reduce the bottom margin of the title |

## Example usage:
```yaml
views:
- name: Example
  cards:
    - type: custom:google-keep-card
      entity: sensor.google_keep_12345
      theme: dark
      alpha: 0.7
      show:
        - checked
        - unchecked
```

## Installation
### Manual
1. Download [*google-keep-card.js*](https://github.com/PiotrMachowski/Lovelace-Google-Keep-card/raw/master/dist/google-keep-card.js) to `/www/custom_lovelace/google_keep_card` directory:
    ```bash
    mkdir -p www/custom_lovelace/google_keep_card
    cd www/custom_lovelace/google_keep_card/
    wget https://github.com/PiotrMachowski/Lovelace-Google-Keep-card/raw/master/dist/google-keep-card.js
    ```
2. Add card to resources:
    ```yaml
    resources:
      - url: /local/custom_lovelace/google_keep_card/google-keep-card.js
        type: module
    ```

### HACS
1. Find this card in "Frontend" section and install it 
2. Add card to resources:
    ```yaml
    resources:
      - url: /hacsfiles/google_keep_card/google-keep-card.js
        type: module
    ```

## FAQ
* **Does this card allow editing notes?**
  
  No, right now it provides read-only view of notes.

<a href="https://www.buymeacoffee.com/PiotrMachowski" target="_blank"><img src="https://bmc-cdn.nyc3.digitaloceanspaces.com/BMC-button-images/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>
