# AmanMap ♿🌍

**A community-powered accessibility map.** Help people discover places and report obstacles that affect mobility.

AmanMap is a lightweight, country-aware web app built with vanilla JavaScript, Leaflet and OpenStreetMap. The current interface offers six languages: Arabic, French, English, Spanish, German and Tamazight (Tifinagh); it is not yet translated into every language in the world.

## Features

- Country selection before entering the map, with a suggested language and a country-change control inside the app. Country selection recenters the map for a curated set of countries; other countries open at a world view.
- Add places, parking, accessible parking, roads and paths, sidewalks, crossings, ramps, elevators, public transport, medical services, entrances, public facilities, barriers, tactile paving, shelters, benches and adapted toilets.
- Record accessibility details and notes.
- Search and filter contributions; view summary counts.
- Use device geolocation and click the map to select coordinates.
- Import/export contributions as JSON.
- Arabic RTL plus French, English, Spanish, German and Tamazight (Tifinagh) interfaces.
- Load nearby public places and mapped pedestrian infrastructure from OpenStreetMap around the current map center (up to 120 results per request).
- Accessibility status is inferred only from explicit OpenStreetMap `wheelchair` tags; otherwise it remains unknown.
- Responsive layout and local-first storage.
- Remember the selected interface language on the current device.
- Validate imported JSON files (size, record count, field types and coordinates), support generic places with unknown accessibility, and skip duplicate IDs.
- Limit Overpass requests to one per minute per browser, use POST requests, and stop requests after a 30-second timeout.

## Run locally

No build step is required. Open `index.html` in a browser, or serve the folder with any static HTTP server.

## Deploy with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment → Source**, select **GitHub Actions**.
3. Push changes to `main` or run the deployment workflow manually.
4. Open `https://zakaria027-tech.github.io/amanmap/` after the workflow succeeds.

## Current limitations

- The map displays nearby road/path and pedestrian-infrastructure features as mapped records; it does not yet calculate turn-by-turn accessible pedestrian routes or verify curb cuts, surface quality, slope, width, crossing signals, or temporary closures.
- Country selection changes the starting region for a curated set of countries and suggests a language. It does not yet load country-specific laws, services, or authoritative accessibility datasets.
- Six interface languages are available today. Comprehensive support for every world language requires additional reviewed translations.

## Important data and privacy note

This release stores contributions in the visitor's browser using localStorage. Data is **not** uploaded to a server and is **not automatically shared** between visitors. Use JSON export/import to exchange contributions manually. The service worker caches the application shell for repeat/offline opening; map tiles and OpenStreetMap place discovery require an internet connection. Nearby place discovery queries the public Overpass API and adds results to the visitor's local list. The interface enforces a one-minute per-browser cooldown and a 30-second request timeout, but this is not a substitute for the provider's usage policies. Please respect OpenStreetMap/Overpass usage policies and avoid repeated rapid requests. Do not enter personal or sensitive information. Geolocation is requested only after the visitor presses the location button.

Map tiles and map data are provided by OpenStreetMap. See https://www.openstreetmap.org/copyright. Leaflet is loaded from unpkg CDN. An internet connection is required for the map and its tiles.

## Data quality and safety

Contributions are community reports, not verified accessibility certifications. Check conditions with the venue before travelling. AmanMap does not guarantee that a route or place is accessible.

## Contributing

Issues and pull requests are welcome. Please report bugs, suggest features, and help translate the interface. Keep reports respectful, factual, and free of personal data.

## License

MIT — see [LICENSE](LICENSE).


## Experimental pedestrian route planner

A beta route planner lets visitors select start and destination points on the map and requests a pedestrian route from the public Valhalla demo service using OpenStreetMap data. The route is a pedestrian suggestion only; it is **not certified as wheelchair-accessible**. Stair, sidewalk, curb, ramp, surface and temporary-obstacle data may be incomplete or absent. Users must verify conditions on site. The routing service is external and may be unavailable or rate-limited. Country selection centers the map on a country where a preset exists; it does not provide a complete, independently curated national accessibility database. The current interface's fully authored translations remain Arabic, French, English, Spanish, German and Tamazight; other languages are not yet fully translated.
