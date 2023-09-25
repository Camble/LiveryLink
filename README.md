# Livery Link

## About

[![Watch the video][screenshot]](https://youtu.be/OmfYs3eZ3ro)

Livery Link's purpose is twofold:
- A desktop application to simplify downloading, installing & managing DCS Liveries.
- An automatic livery sharing mod for DCS.


## How Does It Work?

- Livery Link auto-starts with DCS World.
- When you connect to a server which has Livery Link running, your client will connect.
- When you jump in an aircraft, any liveries you installed with Livery Link will be shared with the server, and the other players.
- When another player shares a livery with the server, your client will download and install it automatically.


## Requirements

- .NET 7 is required to run Livery Link


## Recent Changes

### v0.7.0

- Added `config.json` file - created on first run and can be edited in the absence of an options page
- Added `LiveryCount` and disable auto-download of received packs (downloads with more than one livery)
- Make use of `Share` option for liveries. Defaults are `true` for manual installs, `false` for received liveries
- Add `DateInstalled` and `DateLastSeen` to `manifest.json`
- Su-27 liveries now install for J-11A as well
- Refactored livery sharing between server and clients
- Fixed install button becoming disabled after an error
- Fixed "The process cannot access the file because it is being used by another process"
- Automatically close when DCS exits
## Installation

1. Extract all contents into a folder.
1. Run `LiveryLink.exe`.
1. Locate your `DCS\Saved Games\` folder if prompted.
1. Choose `Yes` to install the scripts.

As the DCS mod & script installation only happens once on first run, if you have any issues, either delete `config.json` or select `Tools` then `Reset config`. This is especially important if you relocate `LiveryLink.exe` to another folder, as the launcher won't know where to find it.


## Desktop Client

The UI is currently very barebones. Paste in a Livery URL from [DCS User Files](https://www.digitalcombatsimulator.com/en/files/) to install it.


## Livery Sharing

In order to automatically share liveries to other players, they must also have Livery Link, and the server you are flying on must be running Livery Link Server.

The server will be made available for DCS server hosts with the official v1.0 release.


## Getting Started

See [releases](https://github.com/Camble/LiveryLink/releases) for download links.


## Known Issues

- Detected or chosen folders cannot be changed yet. Settings can be cleared by deleting or modifying the `user.config` file from `%AppData%\Local\LiveryLink`
- Currently only ZIP files can be installed. RAR & 7z support is coming in a future release.


## Roadmap

- [x] Auto-launch with DCS
- [x] 7z support
- [x] RAR support
- [x] Progress indicator
- [x] Installer (partly done - automatically installs scripts)
- [ ] Livery Manager UI for the desktop client
- [ ] Auto-updater
- [ ] Customize which liveries are shared with other players
- [ ] Customize which liveries to accept from other players
- [ ] Blacklist download of liveries for certain modules, or above a certain size
- [ ] Auto-delete old liveries
- [ ] Disk space quota
- [ ] Server software release
- [ ] Support to share "server-side" liveries (server owner can share livery with players who fly on their server)
- [ ] Custom cockpit installer
- [ ] One-click default livery unlocker
- [ ] In-game mod options page to customise auto-launch
- [ ] Dark theme

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[screenshot]: https://github.com/Camble/LiveryLink/blob/main/screenshot-0.6.0.png