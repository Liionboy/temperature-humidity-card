# Living Temperature Card

A decorative, read-only Home Assistant Lovelace card for indoor temperature and humidity sensors. Warm coral and amber accents distinguish temperature; teal and blue accents highlight humidity, including a circular humidity gauge.

## Features

- Large, easy-to-scan temperature and humidity readings in separate colorful panels.
- Circular humidity gauge with a percentage ring.
- Configurable temperature sensor, humidity sensor, and card title.
- Uses each sensor's live state and unit; unavailable values are shown gracefully.
- Responsive, theme-aware surface, accessible labels, and reduced-motion support.
- Read-only: it does not call Home Assistant services or change devices.
- No external assets, libraries, analytics, credentials, or backend integration.

## Install with HACS

1. In Home Assistant, open **HACS → ⋮ → Custom repositories**.
2. Add `https://github.com/Liionboy/lovelace-living-temperature-card` with category **Dashboard**.
3. Install **Living Temperature Card**, then refresh the browser.
4. Add the card from the dashboard card picker and select the temperature and humidity entities.

This is a frontend Dashboard plugin, not a backend integration.

## Configuration

The visual editor is recommended. The default entities are the Living Temperature sensors; you can change them in the card editor.

```yaml
type: custom:living-temperature-card
temperature_entity: sensor.living_temperature_temperature
humidity_entity: sensor.living_temperature_humidity
title: Living Temperature
```

`humidity_entity` and `title` are optional. Units are read from the entities.

## Manual resource install

Copy `dist/living-temperature-card.js` to `/config/www/living-temperature-card.js`, add `/local/living-temperature-card.js` as a JavaScript module under **Settings → Dashboards → Resources**, refresh the browser, and use `type: custom:living-temperature-card`.

## Development

Dependency-free ES module. Run `npm run check` to check JavaScript syntax.

## License

MIT. See [LICENSE](LICENSE).
