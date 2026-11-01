# Sailing Analyser — GitHub Pages

This is the shared Sailing Analyser website. All race data is in `races/*.json`; the application lives in `index.html`.

## First publication
1. On github.com create a **public** repository named `sailing-races` (do not initialize with README).
2. Open the repository → **Add file** → **Upload files**.
3. Upload `index.html`, `races.json`, and `.nojekyll` from this package, then commit.
4. In repository **Settings → Pages**, select **Deploy from a branch**, `main`, `/ (root)`, and Save.
5. After deployment, visit `https://YOUR-USERNAME.github.io/sailing-races/`.

## Adding a race
1. Open your published Sailing Analyser, or open `index.html` on a desktop browser via a local web server.
2. Choose **Load GPX** and select your GPX. Define and save segments if desired.
3. Choose **Export race JSON for GitHub** and give the race a name.
4. In GitHub, navigate to the `races` folder and choose **Add file → Upload files**. Upload the exported JSON, and commit.
   If the folder is not visible yet, create it by choosing **Add file → Create new file**, naming it `races/.gitkeep`, and committing.
5. Edit `races.json` in the repository root, using the pencil icon, to add the race. Example:

```json
[
  {"name": "Sunday Race — 1 Nov 2026", "file": "races/race-2026-11-01.json"}
]
```

For additional races, add more objects separated by commas inside the square brackets. Commit changes.
6. Refresh your Pages site. The race appears in the **Published race** menu.
7. Share a direct race URL: `https://YOUR-USERNAME.github.io/sailing-races/?race=races%2Frace-2026-11-01.json`

## Notes
- Published JSON includes GPS positions, timestamps, derived SOG/COG, heart rate when available, and saved segments.
- The original GPX is not embedded in the published JSON. Use the separate compact HTML export when you need a portable original GPX.
- Satellite map tiles and Leaflet are loaded over the internet.
- This is a public site: anyone can see the uploaded race data.
- Browser-based GitHub uploads cannot automatically publish a file from your Sailing Analyser without GitHub authorization. This design avoids needing an access token.
- To view on iPad, open the HTTPS GitHub Pages URL, not the HTML preview in Files.
