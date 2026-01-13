<!-- markdownlint-disable first-line-heading -->
<!-- markdownlint-disable no-inline-html -->

This is a fork of the [Offical Repo](https://github.com/blakeblackshear/frigate-hass-integration) with some features that I'm choosing to keep around for my own needs. 

# Frigate Home Assistant Integration Lite

Provides the following:

- Rich media browser with thumbnails and navigation
- Sensor entities (Camera FPS, Detection FPS, Process FPS, Skipped FPS, Objects detected)
- Switch entities (Recording, Detection, Snapshots, Improve Contrast)
- Services to control camera (manual events, PTZ control)
- Support for multiple Frigate instances.

It provides an option to disable the richness of sensor entities that are provided by default in the official repo, to reduce overhead and optimize the experience if you aren't using all those features, including:

- Binary Sensor entities (Object motion)
- Camera entities (Live view, Object detected snapshot)

## Installation

Easiest install is via [HACS](https://hacs.xyz/):

On the HACS tab, select Custom Repoistories and then paste this repo: `https://github.com/rgregg/frigate-hass-integration-lite`.

`HACS -> Integrations -> Explore & Add Repositories -> Frigate HASS Lite`

Notes:

- HACS does not "configure" the integration for you. You must go to `Configuration > Integrations` and add Frigate after installing via HACS.
- The `mqtt` integration must be installed and configured in order for the Frigate integration to work. As manual configuration is required for the `mqtt` setup, this cannot happen automatically.

For manual installation for advanced users, copy `custom_components/frigate` to
your `custom_components` folder in Home Assistant.

Please visit the [main Frigate
documentation](https://docs.frigate.video/integrations/home-assistant/)
for full installation instructions of this integration.

### Media Browsing

You will also need [media_source](https://www.home-assistant.io/integrations/media_source/) enabled in your Home Assistant configuration for the Media Browser to appear.

### Lovelace Card

There is also a [companion Lovelace card](https://github.com/dermotduffy/frigate-hass-card) for use with this integration.

<img src="https://raw.githubusercontent.com/blakeblackshear/frigate-hass-integration/master/images/lovelace-card.png">

## Documentation

For full usage instructions, please see the [central Frigate documentation](https://docs.frigate.video/integrations/home-assistant/).
