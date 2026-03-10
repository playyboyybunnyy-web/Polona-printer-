# Polona-printer-
Polona printer Bluetooth driver for printing from a browser without downloading the native app.

## Requirements

- A **Chromium-based browser** (Google Chrome, Microsoft Edge, Brave, etc.) on desktop **or** Safari on iOS/macOS — required for the [Web Bluetooth API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Bluetooth_API).
- A **Polona Bluetooth thermal printer**.
- A PDF file you want to print.

## How to Launch

### Option 1 — Open directly in your browser (simplest)

1. Download or clone this repository.
2. Double-click `index.html` to open it in your browser, **or** drag it into an open browser window.

> **Note:** Some browsers block the Web Bluetooth API when the page is loaded from a `file://` URL. If the *Connect Printer* button doesn't work, use Option 2 below.

### Option 2 — Serve with a local HTTP server (recommended)

A local server ensures the Web Bluetooth API works correctly. Pick whichever option matches what you have installed:

**Python (built-in on macOS/Linux):**
```bash
python3 -m http.server 8080
```
Then open [http://localhost:8080](http://localhost:8080) in your browser.

**Node.js (npx — no install needed):**
```bash
npx serve .
```
Then open the URL shown in the terminal (usually [http://localhost:3000](http://localhost:3000)).

**Node.js (http-server):**
```bash
npx http-server .
```
Then open [http://localhost:8080](http://localhost:8080) in your browser.

## How to Use

1. Click **Connect Printer** and select your Polona printer from the Bluetooth device list.
2. Click **Choose File** and select a PDF to print.
3. *(Optional)* Click **Preview** to see a preview of the print output with the selected dithering mode.
4. Adjust **Print Width** and **Dithering Mode** as needed.
5. Click **Print** to send the job to the printer.
6. Click **Disconnect** when done.

## Troubleshooting

| Problem | Solution |
|---|---|
| *Connect Printer* button does nothing | Use a Chromium-based browser (Chrome, Edge, Brave) or Safari on iOS |
| Bluetooth device list is empty | Make sure the printer is powered on and in pairing/discoverable mode |
| Web Bluetooth not available | Serve the file via a local HTTP server (see Option 2) instead of opening from `file://` |
| Print comes out very light or dark | Try a different **Dithering Mode** from the dropdown |
