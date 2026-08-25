# Pharloom

Unofficial dark + light themes inspired by Hollow Knight: Silksong (Pharloom).
Fan palette only — not affiliated with Team Cherry.

Not on npm or the VS Code Marketplace yet. Install locally from this repo.

## Clone

```bash
git clone https://github.com/code4cake/pharloom-theme.git
cd pharloom-theme
```

---

## Cursor / VS Code

Works the same on **macOS**, **Linux**, and **Windows**.

### Install

1. Open Command Palette:
   - macOS: `Cmd+Shift+P`
   - Linux / Windows: `Ctrl+Shift+P`
2. Run **Developer: Install Extension from Location…**
3. Select the `pharloom-theme` folder (the one that contains `package.json`).
4. Run **Preferences: Color Theme** and pick **Pharloom Dark** or **Pharloom Light**.

#### Optional: symlink (live edits without reinstall)

**macOS / Linux**

```bash
# Cursor
ln -s "$(pwd)" ~/.cursor/extensions/pharloom-theme

# VS Code
ln -s "$(pwd)" ~/.vscode/extensions/pharloom-theme
```

Then **Developer: Reload Window**.

**Windows** (Command Prompt as admin, adjust paths):

```bat
mklink /J "%USERPROFILE%\.cursor\extensions\pharloom-theme" "C:\path\to\pharloom-theme"
mklink /J "%USERPROFILE%\.vscode\extensions\pharloom-theme" "C:\path\to\pharloom-theme"
```

### Uninstall

1. Switch to another color theme first (**Preferences: Color Theme**).
2. Either:
   - Extensions view → find **Pharloom** → **Uninstall**, or
   - Delete / unlink the extension folder:
     - Cursor: `~/.cursor/extensions/pharloom-theme`  
       Windows: `%USERPROFILE%\.cursor\extensions\pharloom-theme`
     - VS Code: `~/.vscode/extensions/pharloom-theme`  
       Windows: `%USERPROFILE%\.vscode\extensions\pharloom-theme`
3. **Developer: Reload Window**.

---

## Terminal

### macOS — iTerm2

**Install**

1. iTerm2 → **Settings** → **Profiles** → **Colors**
2. **Color Presets…** → **Import…**
3. Choose `terminal/Pharloom.itermcolors`
4. **Color Presets…** → **Pharloom**

**Uninstall**

1. Same **Colors** panel → **Color Presets…**
2. Choose another preset (or delete **Pharloom** if your iTerm version allows removing presets)
3. Optionally delete `Pharloom.itermcolors` from wherever you imported it (the repo copy can stay)

### Windows — Windows Terminal

**Install**

1. Open Windows Terminal → **Settings** → Open JSON file (`settings.json`).
2. Copy the scheme object from `terminal/Pharloom.windows-terminal.json`.
3. Paste it into the `"schemes"` array.
4. On your PowerShell (or other) profile, set:

```json
"colorScheme": "Pharloom"
```

**Uninstall**

1. Remove `"colorScheme": "Pharloom"` from the profile (or set another scheme).
2. Remove the `"name": "Pharloom"` object from `"schemes"`.
3. Save `settings.json`.

### Linux

There is no single preset file for every Linux terminal. Use the ANSI colors below (same as the Windows Terminal scheme) in **GNOME Terminal**, **Konsole**, **Tilix**, etc.:

| Slot | Hex |
|------|-----|
| Background | `#161218` |
| Foreground | `#E8DCC8` |
| Cursor | `#D4A84B` |
| Selection | `#3A2428` |
| Black / Bright black | `#161218` / `#7A6A72` |
| Red | `#C23B3B` |
| Green | `#3D7A6A` |
| Yellow | `#D4A84B` |
| Blue | `#B08A5A` |
| Magenta | `#C23B3B` |
| Cyan | `#3D7A6A` |
| White | `#E8DCC8` |

**Uninstall:** switch the profile back to your previous colors (or the system default).

### Optional — Ghostty (macOS / Linux)

Add to `~/.config/ghostty/config` (or merge into your existing config):

```ini
background = #161218
foreground = #E8DCC8
cursor-color = #D4A84B
selection-background = #3A2428
selection-foreground = #E8DCC8

palette = 0=#161218
palette = 1=#C23B3B
palette = 2=#3D7A6A
palette = 3=#D4A84B
palette = 4=#B08A5A
palette = 5=#C23B3B
palette = 6=#3D7A6A
palette = 7=#E8DCC8
palette = 8=#7A6A72
palette = 9=#C23B3B
palette = 10=#3D7A6A
palette = 11=#D4A84B
palette = 12=#B08A5A
palette = 13=#C23B3B
palette = 14=#3D7A6A
palette = 15=#E8DCC8
```

**Uninstall:** remove that block and restart Ghostty.

---

## Feedback

Try Dark + Light in the editor and the terminal palette, then tell me what to change, modify, or remove.