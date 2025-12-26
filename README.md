# firefox-tab-numbers

![Firefox tab numbers](assets/tab-numbers-default-theme.png)

Displays numeric labels for Firefox tabs **above and to the left of the favicon** in the native tab bar using `userChrome.css`.

This is a **UI customization**, not a Firefox WebExtension. Firefox extensions cannot modify the native tab strip; this solution uses Firefox’s supported `userChrome.css` mechanism instead.

---

## Features

- Numbers all tabs in the top tab bar
- Number is rendered directly inside the tab UI
- Positioned above / left of the favicon for minimal visual noise
- No JavaScript, no background processes
- Does not interfere with tab clicking or dragging
- Optional handling for pinned tabs

---

## Requirements

- Firefox (desktop)
- `toolkit.legacyUserProfileCustomizations.stylesheets` enabled

---

## Installation

### 1. Enable userChrome.css support
1. Open `about:config`
2. Set the following preference to `true`: toolkit.legacyUserProfileCustomizations.stylesheets

### 2. Open your Firefox profile directory
- Go to `about:support`
- Under **Profile Folder**, click **Open Folder**

### 3. Create the chrome directory and file
Inside your profile folder:
    chrome/
    └── userChrome.css

If the `chrome` folder does not exist, create it.

### 4. Add the CSS
Copy the contents of [`userChrome.css`](./userChrome.css) into the file.

### 5. Restart Firefox
The changes only apply after a full restart.

---

## Notes

- This customization affects **only your local Firefox profile**
- It cannot be distributed as a normal Firefox add-on
- Firefox updates may occasionally require minor CSS adjustments
- Pinned tabs can be excluded from numbering (see CSS comments)

---

## Tested On

- Firefox Stable (default density)
- macOS

Other platforms and densities should work but are not guaranteed.

---

## License

MIT License. See [`LICENSE`](./LICENSE) for details.


