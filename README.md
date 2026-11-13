# AmanMap ♿🌍

**A community-powered accessibility map.** Help people discover places and report obstacles that affect mobility.

AmanMap is a lightweight, bilingual (Arabic/French) progressive-friendly web app built with vanilla JavaScript, Leaflet and OpenStreetMap.

## Features

- Interactive OpenStreetMap centered on Agadir, Morocco (change the map location anytime).
- Add accessible places, limited-access places, obstacles and adapted toilets.
- Record accessibility details and notes.
- Search and filter contributions; view summary counts.
- Use device geolocation and click the map to select coordinates.
- Import/export contributions as JSON.
- Arabic RTL and French LTR interface.
- Responsive layout and local-first storage.

## Run locally

No build step is required. Open `index.html` in a browser, or serve the folder with any static HTTP server.

## Deploy with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select **main** and **/ (root)**, then Save.
4. Wait for the deployment and open the URL shown by GitHub Pages.

A workflow in `.github/workflows/pages.yml` also provides a GitHub Actions Pages deployment path; select **GitHub Actions** as the Pages source if using it.

## Important data and privacy note

This first release stores contributions in the visitor's browser using localStorage. Data is **not** uploaded to a server and is **not automatically shared** between visitors. Use JSON export/import to exchange contributions manually. Do not enter personal or sensitive information. Geolocation is requested only after the visitor presses the location button.

Map tiles and map data are provided by OpenStreetMap. See https://www.openstreetmap.org/copyright. Leaflet is loaded from unpkg CDN. An internet connection is required for the map.

## Data quality and safety

Contributions are community reports, not verified accessibility certifications. Check conditions with the venue before travelling. AmanMap does not guarantee that a route or place is accessible.

## Contributing

Issues and pull requests are welcome. Please report bugs, suggest features, and help translate the interface. Keep reports respectful, factual, and free of personal data.

## License

MIT — see [LICENSE](LICENSE).
