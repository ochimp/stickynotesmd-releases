# Changelog

## Version 1.2.0 Update (2026-07-18)

### Enhancements

- **Edit notes right in the Note List.** Click **Edit** (or press ⌘E) to edit the selected note in place, and **Done** (or ⌘E again) to switch back to preview — no need to open a window. Press **↩** or click **Open as Sticky** to pop the note out into its own sticky.
- **Standard menu bar.** When the Note List, Settings, or About window is open, the usual macOS menus (App, File, Edit, View, Window, Help) are available at the top of the screen — even when the Dock icon is hidden.
- **New About window.** See the app icon, version, a link to stickynotesmd.com, and the full changelog — from the Note List's cog menu, the menu-bar icon, or the app menu.

### Bug Fixes

- A note saved off-screen (synced from another Mac, or left on a display you've since disconnected) now opens where you can see it instead of only reappearing after a relaunch.

## Version 1.1.5 Update (2026-07-07)

### Enhancements

- **Export All Notes to Markdown Files** — from Settings → Data, pick a folder and every note is saved as its own `.md` file, named after its first line. Your notes, yours to take anywhere.

### Bug Fixes

- iCloud sync now reliably syncs your notes across Macs signed in to the same iCloud account. (Install this update on each of your Macs.)

## Version 1.1.4 Update (2026-07-05)

### Enhancements

- You can now select and copy rendered Markdown text in the Note List and in sticky notes — not just the raw Markdown while editing.
- The Note List's cog button now opens a menu: Show / Hide Open Notes, Settings, Hide Note List, and Quit.
- Added keyboard shortcuts — in a note: ⌘W close, ⌘P pin, ⌘E toggle preview, ⌘Q quit; in the Note List: ⌘N new note, ⌘P pin, ⌘E edit, ⌘W hide list, ⌘, settings, ⌘Q quit.
- The note toolbar's color swatch and pin icon are now easier to see.

### Bug Fixes

- Pressing Return at the start of a list item no longer duplicates the bullet — it moves the line down as expected.

## Version 1.1.3 Update (2026-07-04)

### Enhancements

- The Note List's New Note, Pin, and Sort buttons are now always visible in a bottom bar instead of hiding behind an overflow menu on narrow windows.

### Bug Fixes

- Update prompts no longer get hidden behind the Note List or Settings window.
- Fixed the Note List disappearing when turning off "Show in Dock".

## Version 1.1.2 Update (2026-07-04)

### Enhancements

- Sticky Notes now checks for updates about once a week.

### Bug Fixes

- Fixed an error that prevented updates from installing ("An error occurred while launching the installer").

## Version 1.1.1 Update (2026-07-04)

### Enhancements

- The Note List now opens automatically when Sticky Notes launches, so it's clear the app started and you always have a window to work from.

### Bug Fixes

- Fixed the Note List vanishing when you toggled **Show in Dock** while it was behind the Settings window.

## Version 1.1.0 Update (2026-07-03)

### Features

- iCloud sync now works end to end. Choose **iCloud** under Settings → Storage to keep your notes in sync across your Macs signed in to the same iCloud account.
- Adds a live sync-status indicator in Settings that shows exactly where your notes are being saved — syncing with iCloud, stored on this Mac, or a clear warning if iCloud is signed out or unavailable — so the app never claims to be syncing when it isn't.
- Switching your storage location now shows a confirmation explaining what will happen and relaunches automatically. Switching to iCloud merges the notes already on your Mac with your iCloud notes; nothing is deleted.

### Enhancements

- Adds a **Settings** button to the Note List and a **Close** button to the Settings window, so both are easy to reach even when the Dock icon is hidden. The Settings window also stays on top until you close it.
- The show/hide Note List shortcut now reliably brings the list to the front when it's hidden behind other windows, instead of hiding an already-buried window (which made it look like nothing happened).
- Changes the default **Show / hide note list** shortcut to ⌥⌘K.

## Version 1.0.4 Update (2026-05-17)

### Features

- Adds a delete button to notes in the Note List view, with a confirmation dialog to prevent accidental deletion. The button appears on row hover and is also available in the detail view's toolbar.
- New notes now pick a random color from the palette instead of always starting yellow, and consecutive new notes avoid repeating the previous color.
- Adds syntax highlighting for fenced code blocks in preview mode, covering ~190 languages (JSON, TypeScript, JavaScript, Python, Swift, Bash, and many more) via HighlighterSwift / Highlight.js. Uses the `atom-one-light` and `atom-one-dark` themes to follow the system color scheme.

### Enhancements

- Routes all delete actions (row button, detail toolbar, and context menu) through a single confirmation prompt for consistent, undo-safe behavior.
- Replaces the previous Swift-only code highlighter scaffolding (which was never fully wired up) with a multi-language highlighter that works across all common languages.
- Implements Sparkle "gentle reminders" for background update checks: when an update is found, the dock icon appears with a "1" badge and a banner notification is posted, then the app's previous dock-icon preference is restored once the update session ends. Tapping the banner surfaces Sparkle's standard update alert.
