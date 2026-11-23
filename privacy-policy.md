---
title: Cawdio privacy policy
permalink: /privacy-policy.html
---

# Cawdio privacy policy

_Last updated November 23, 2026_

Cawdio has no Cawdio accounts, analytics or developer-operated servers.

## Browser extension

On YouTube Music, the extension reads the current track's title, artist, album, artwork URL and song link, along with playback position, duration, pause state and whether an ad is showing. It sends these details to Cawdio for Windows over the loopback interface (`127.0.0.1`) to provide now-playing information. The extension also reads and changes the desktop app's “Share on Discord” setting when you use its popup.

The extension stores the desktop access token and port in local browser storage. Its popup uses temporary session storage for diagnostics, which can include the last reported song title and connection status. Native messaging provides the access token and port. The extension itself communicates only with the desktop app on the same PC.

The Cawdio extension's use of information received from Chrome complies with the [Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data/), including its Limited Use requirements.

## Desktop app

- **Discord status.** Sharing is on by default. The desktop app sends current track details, which may include artwork and the song link, to Discord through the local Discord app for display on your profile. You can turn sharing off in the Cawdio tray menu or extension popup.
- **Cover art.** The desktop app can request the cover image supplied by YouTube Music from its image host. If you enable online cover lookup, Cawdio can send track information to Apple iTunes Search and, if needed, Deezer to find cover art. You can turn online lookup off in the tray menu.
- **Paired devices.** Cawdio streams the PC's captured audio and playback information to devices you pair. The browser player uses WebRTC on your local network or through a private network such as Tailscale. Native connections use iroh and may go through n0's public relays by default. With iroh, a relay can observe connection metadata while the stream contents remain end-to-end encrypted. Cawdio does not download or save music files.

## Removing local data

Run `cawdio.exe unregister-browsers` to remove Cawdio's browser registrations, then uninstall the extension to remove its browser storage. Quit Cawdio and delete `%APPDATA%\Cawdio` to erase its local settings, pairing information and logs.

## Contact

Open an issue in the public [Cawdio website repository]({{ site.github.repository_url }}/issues).
