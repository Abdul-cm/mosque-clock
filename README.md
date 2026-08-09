# مسجد كلوك | Mosque Clock

A self-contained, offline digital clock for mosque displays. It rotates every few seconds between a large clock view and a full prayer-times table — no server, no build step, no internet connection required once the page has loaded. The interface is in Arabic (RTL).

## Features

- **Big, readable clock** with Gregorian and Hijri (Islamic) date, sized for TVs and monitors.
- **Auto-rotating slides** — clock view ⇄ prayer-times table, on a configurable interval.
- **Auto-calculated prayer times** from your latitude/longitude using standard solar-position astronomy (no external API — works fully offline).
- **Next-prayer countdown**, with the upcoming prayer highlighted on the table.
- **Iqama times** shown alongside each Adhan time, with a configurable offset per prayer.
- **Settings panel** (gear icon) for mosque name, city label, location, calculation method, Asr method, time format, and slide interval — saved locally in the browser so it persists across restarts.
- **Fullscreen / kiosk mode** button, ideal for a dedicated screen.
- Single HTML file — easy to copy to any display device and open in a browser.

## Getting started

1. Open [`index.html`](index.html) in any modern browser (Chrome, Edge, Firefox).
2. Click the ⚙ settings icon (bottom-left) and set:
   - **Mosque name** and **city label**
   - **Latitude / longitude** for your location — type them in, or click **تحديد موقعي** (Detect My Location) to use the browser's geolocation
   - **Calculation method** (Muslim World League, ISNA, Egyptian, Umm al-Qura, or Karachi) and **Asr method** (Standard or Hanafi)
   - **Iqama offsets** (minutes after Adhan) for each prayer
3. Click **حفظ** (Save). Click the ⛶ icon to enter fullscreen for display on a TV/monitor.

Settings are stored in the browser's `localStorage`, so they persist between reloads and reboots on the same device/browser.

## Displaying it on a screen

- **Local file**: copy `index.html` to the display's PC/laptop, open it in a browser, and go fullscreen (F11 or the ⛶ button). Leave the tab open.
- **GitHub Pages**: enable Pages for this repo (Settings → Pages → deploy from the `master` branch) to get a public URL you can open directly on any networked display.
- For a dedicated kiosk screen, most browsers support launching directly into fullscreen/kiosk mode from the command line, e.g.:
  ```
  chrome --kiosk "https://your-pages-url/"
  ```

## Accuracy note

Prayer times are computed geometrically from your coordinates and are generally accurate to within a minute or two, but can drift further at high latitudes or near the solstices. Compare against your mosque's official printed calendar after first setup, and adjust the calculation method if needed.

## Tech

No dependencies, no build tools — just HTML, CSS, and vanilla JavaScript in a single file.
