# [To-Userscript-Web](https://assgrabber.github.io/To-Userscript-Web/)
Chrome/Firefox extensions to UserScript.

# Extension to Userscript

A single HTML file that converts a Chrome or Firefox extension into a `.user.js` userscript, entirely in your browser. No install, no build step, no PC required.

## What it does

Pick a `.zip`, `.crx`, or `.xpi` and it produces one userscript that runs the extension's features on top of Tampermonkey, Violentmonkey, or the iOS Userscripts app:

- Rebuilds the `chrome.*` / `browser.*` APIs the extension uses (storage, messaging, tabs, alarms, notifications, context menus, translations, cookies, and more)
- Bundles content scripts, background scripts, and ES modules (including dynamic `import()`)
- Emulates the extension's network-blocking and redirect rules
- Opens the popup and options page in an overlay, accessible from your userscript app's menu or a floating button
- Inlines images, fonts, and other files so nothing is missing
- Supports keyboard shortcuts defined in the manifest
- Can also fetch the extension file directly from a Chrome Web Store or Firefox Add-ons link

## How to use it

1. Open `extension-to-userscript.html` in any browser.
2. Choose the extension file (or paste a store link to download one first).
3. Review the settings if needed — script name, which sites it runs on, language, etc.
4. Tap **Copy userscript** and paste it into a new script in your userscript manager, or **Save file** to download it.

## Limitations

Extensions built around blocking ad networks, replacing the new tab page, or DevTools panels won't fully carry over. Requests the browser makes before the userscript loads, and rules that modify request headers, can't be emulated. Everything else — especially extensions that enhance a specific website — usually works well.

Inspired by [to-userscript](https://github.com/Explosion-Scratch/to-userscript).
