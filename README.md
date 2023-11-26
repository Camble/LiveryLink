# Livery Link

## About

Livery Link's purpose is twofold:
- A desktop application to simplify downloading, installing & managing DCS Liveries.
- An automatic livery sharing mod for DCS.

[![Watch the video][screenshot]](https://youtu.be/h0i65DmegYQ)

Click the above screenshot to watch the video

[![Download][download]](https://github.com/Camble/LiveryLink/releases/download/v0.10.3/LiveryLink.v0.10.3.+.Runtime.zip)

![Options][options-screenshot]

## Requirements

- .NET 7 is required to run Livery Link. Choose the `+ Runtime.zip` version if you don't have .NET 7 installed.


## Getting Started

See [releases](https://github.com/Camble/LiveryLink/releases) for download links.


## How Does It Work?

- Livery Link auto-starts with DCS World.
- When you connect to a server which has Livery Link running, your client will connect.
- When you spawn an aircraft, any liveries you installed with Livery Link will be shared with other players.
- When another player shares a livery with the server, your client will download and install it automatically.


## Installation

1. Extract all contents into the folder of your choice.
1. Run `LiveryLink.exe` to initialize the app.
1. Locate your `Saved Games\DCS` folder if prompted.
1. Choose `Yes` to install the scripts.

As the DCS mod & script installation only happens once on first run, if you have any issues, select `Reset config` from the `Tools` menu. This is especially important if you relocate `LiveryLink.exe` to another folder, as the launcher won't know where to find it.


## Recent Changes

### 0.10.3

- Fixed an issue when sharing more than one livery


### 0.10.2

 - Added support to install liveries for community mod aircraft
 - Fixed socket timeout issue when installing livery for the first time
 - Display DCS server name in status bar when connected


### 0.10.1

- Fixed `Value cannot be null` error on upgrade to v0.10.0


### 0.10.0

- Added a very early livery browser to the client UI
- Track when shared liveries were last seen
- Improved server handshake to ensure client and server versions match
- Warn if DCS is running when attempting to install the script
- Fixed an issue with receiving multiple shared liveries
- Added .tga to the list of allowed file types for installation
- Improved server connection logic
- Implemented some missing user options
- Fixed error when connecting to server
- Fixed a bug preventing notifications
- Many other bugfixes and improvements

### v0.9.0

- Options window for user customisation
- Completely reworked notification system
- Check for updates automatically
- Fixed only sharing one livery per module

### 0.8.0

- Improved upgrade process for new versions
- Refactored most of the server logic
- Various bugfixes & server stability changes
- Fixed auto-launch
- Improved logging
- Fixed bug preventing sharing from working

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


## Livery Sharing

In order to automatically share liveries to other players, they must also have Livery Link, and the server you are flying on must be running Livery Link Server.

The server will be made available for DCS server hosts with the official v1.0 release.


## Known Issues

- 7z extraction is **SLOW**


## Roadmap

- [x] Auto-launch with DCS
- [x] 7z support
- [x] RAR support
- [x] Progress indicator
- [x] Installer (partly done - automatically installs scripts)
- [x] Update checker
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
[options-screenshot]: https://github.com/Camble/LiveryLink/blob/main/screenshot-0.9.0-options.png
[download]: https://github.com/Camble/LiveryLink/blob/main/download.png