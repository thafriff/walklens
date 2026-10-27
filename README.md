# WalkLens

A prototype web app that helps people in a Malaysian township walk to the station more safely. It maps walking hazards found on recorded walks, compares the fastest route with the safest one, and lets residents report problems.

> This is a design prototype. It runs entirely in the browser with sample data, and hazard detections on the recorded walk are set up for the demo rather than produced live.

## What it does

- **Navigate:** compares the fastest walk with the safest one, using routes that were audited on foot.
- **Hazard map:** shows reported and detected hazards on a real OpenStreetMap map, with place search as you type.
- **Recorded walks:** plays a real walk through Klang Jaya, with a box drawn around each hazard at the moment it appears on screen.
- **Walk sessions:** after a walk, shows instant health, savings and points, a per-trip fare, and a walking-view map.
- **Community feed:** residents can confirm a hazard or mark it as not a hazard, and follow its progress until it is fixed.
- **Snap a problem:** report a hazard with a photo and a location.
- **Rewards, Safe Arrival and Walk Buddy:** points for walking, a way to let family know you arrived, and a live alert demo.
- **Admin view:** a township map of every audited route, a review queue for findings, and an impact and agency scoreboard.

## Run it

It is a static site with no build step. From the project folder:

```
python -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly also works, but some browsers block the video and map files when run that way.

An internet connection is needed for the map tiles and place search. The app saves its sample data in your browser, and the **Reset demo data** option restores it.

## Built with

- HTML, CSS and vanilla JavaScript in a single `index.html`
- [Leaflet](https://leafletjs.com/) for maps, bundled in `vendor/leaflet`
- [OpenStreetMap](https://www.openstreetmap.org/copyright) tiles and [Photon](https://photon.komoot.io/) place search
- Recorded walk video and still frames in `media/`

## Project structure

```
index.html          the whole app
media/              recorded walk video, poster and frames
vendor/leaflet/     Leaflet library
```

Map data © OpenStreetMap contributors.
