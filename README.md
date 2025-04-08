
# Google Fonts Auto Installer for macOS

Easily install and keep Google Fonts updated on macOS — without needing any extra software.

## 🚀 Features
- Installs all Google Fonts directly to your `~/Library/Fonts` folder
- Automatically updates the font list **every week** via `launchd`
- No Terminal interaction required (just double-click the script)

## 📦 How to use

1. Download and unzip the archive
2. Double-click `install-google-fonts.command`
3. It will:
   - Clone the [Google Fonts GitHub repo](https://github.com/google/fonts) locally
   - Add a background updater that pulls changes every 7 days

## 🔧 Requirements
- macOS 10.13 or newer
- Git (installed by default on macOS)

## 📁 Fonts location
All fonts are stored in:
```
~/Library/Fonts/google-fonts
```

## 🧼 Uninstall

You now have two `.command` scripts included for convenience — no Terminal required:

- `disable-sync.command` — disables the automatic weekly update
- `uninstall-google-fonts.command` — removes the fonts and disables the updater

If you prefer doing it manually, here are the equivalent commands:

To stop automatic updates:
```bash
launchctl unload ~/Library/LaunchAgents/com.bento.googlefonts.update.plist
rm ~/Library/LaunchAgents/com.bento.googlefonts.update.plist
```

To remove the fonts:
```bash
rm -rf ~/Library/Fonts/google-fonts
```

## 🧠 Alternatives

If you're looking for a more advanced or selective CLI tool, check out [fnt](https://github.com/alexmyczko/fnt) — a great solution for developers who prefer a leaner setup and full control over which fonts are installed.

## 🙌 Credits
Made by the community — feel free to fork, improve, or contribute.

## 🪪 License
This project is licensed under the [MIT License](LICENSE).
