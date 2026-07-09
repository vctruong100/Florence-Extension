# Florence Automator Extension

A Manifest V3 browser extension version of Florence Automator. It runs as a content script on `https://us.v2.researchbinders.com/*` and displays a fixed sidebar on the right side of the page.

## Files

- `manifest.json` - Extension manifest (MV3).
- `Florence Extension.js` - Content script containing all automator logic.
- `Chrome_Web_Store_Publishing_Answers.txt` - Suggested Chrome Web Store submission answers.
- `icon16.png`, `icon48.png`, `icon128.png` - Extension icons.

## Loading the extension (developer mode)

1. Open Chrome/Edge and go to `chrome://extensions/`.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select this repository folder (`Florence Extension`).
5. Navigate to `https://us.v2.researchbinders.com/` and refresh.
6. The Florence Automator sidebar should appear on the right side of the page.

## Usage

- Press the configured keybind (default `F2`) to show or hide the sidebar.
- Click any feature button in the sidebar to run the corresponding automator workflow.
- Use the configuration icon (gear) to change the keybind, reorder/hide buttons, or hide logs.

## Notes

- The sidebar is docked to the right edge and adds a `360px` right offset to the page so the underlying page content is not covered.
- `GM.xmlHttpRequest` is not available in extension content scripts; the script falls back to `fetch` automatically.
- Settings such as keybind, button layout, and visibility are stored locally on the Research Binders origin or in extension storage, depending on the feature.

## Publishing

The extension includes the required package icons and a `Chrome_Web_Store_Publishing_Answers.txt` file with suggested permission justifications, privacy disclosures, and reviewer test instructions.
