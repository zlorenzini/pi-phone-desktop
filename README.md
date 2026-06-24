# pi-phone-desktop

Mirror and desktop-mode your Android phone on a Raspberry Pi — no manual
build steps, no SDL3 version hunting, no Android SDK download.

This package bundles [scrcpy](https://github.com/Genymobile/scrcpy)
(Apache-2.0, by Genymobile and contributors) and adds two ready-to-use
launchers under **Accessories**:

- **Phone Mirror** — plain screen mirroring and control over USB or wireless ADB.
- **Phone Desktop Mode** — opens your phone's native Android Desktop Mode
  (Android 16+) in a resizable window on your Pi, using scrcpy's virtual
  display support. This works on any phone running Android 16 or later —
  it's a stock Android feature, not tied to any particular manufacturer.

## Requirements

- Raspberry Pi OS (Debian trixie or later), arm64
- An Android phone with USB debugging enabled (Settings → About phone →
  tap Build number 7 times → Developer options → USB debugging)
- For Phone Desktop Mode specifically: Android 16 or later on the phone

## Install

Download the latest `.deb` from
[Releases](https://github.com/zach/pi-phone-desktop/releases) and run:

```sh
sudo apt install ./pi-phone-desktop_*.deb
```

`apt install ./file.deb` resolves and installs any missing library
dependencies automatically from the standard Raspberry Pi OS repos.

## Usage

1. Plug in your phone via USB (or set up wireless ADB) and accept the
   "Allow USB debugging" prompt on the phone.
2. Open **Phone Mirror** or **Phone Desktop Mode** from the Accessories
   menu.

## Not yet included

- A connect-time popup offering these launchers automatically when you
  plug in a phone (planned for a future release)
- 32-bit (armhf) builds

## Credits

This package exists to save people the trouble of building
[scrcpy](https://github.com/Genymobile/scrcpy) from source on a Pi. All
the actual mirroring/desktop-mode functionality is scrcpy's — go star
their repo.
