# Borland Blue Theme for VS Code

A VS Code theme inspired by the classic Vim `blue` color scheme and the old Borland C / blue-screen office-editor look derived from the original IBM PC of the 1980's.

## Visual Goals

- Cobalt blue workspace background
- High-contrast yellow default text
- Cyan line numbers and accents
- Orange/yellow search highlights

## Vim Color Match

The editor background maps exactly to the Vim named color used in the original `blue.vim`:

- `guibg=darkBlue` -> `#00008B`

The original `guifg=yellow` (`#FFFF00`) is rendered as a slightly dimmer `#F2F200`. Syntax foregrounds are softened by a similar amount to compensate for VS Code's denser font rendering while retaining the classic palette.

## Install Permanently (recommended)

1. Install the packager (one-time, requires [Node.js](https://nodejs.org)):
   ```powershell
   npm install
   ```

2. Build the VSIX package:
   ```powershell
   npm run package
   ```
   This produces `borland-blue-vscode-theme-0.0.1.vsix` in the same folder (no prompts).

3. In VS Code, press `Ctrl+Shift+P` → **Extensions: Install from VSIX...**

4. Browse to the `.vsix` file and open it. Click **Reload** when prompted.

5. Press `Ctrl+K`, `Ctrl+T` → select **Borland Blue**.

The theme is now your permanent default across all VS Code windows.

> After editing the theme JSON, re-run step 2 and reinstall to pick up changes.

## Install Temporarily (development/preview)

1. Open this folder in VS Code.
2. Press `F5` → starts an Extension Development Host window.
3. In that new window: `Ctrl+K`, `Ctrl+T` → select **Borland Blue**.

This is session-only — the theme is gone when the host window closes.

## Notes

The palette is intentionally high-contrast and nostalgic. If you want a softer variant (dimmer yellow or lighter blue), you can duplicate this theme JSON and tweak:

- `editor.background`
- `editor.foreground`
- `editorLineNumber.foreground`
- `tokenColors`
