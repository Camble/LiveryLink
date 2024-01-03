# Livery Link

## Requirements

- .NET 8 is required to run Livery Link. You will be prompted to install it if you don't already have it.

## About

Livery Link's purpose is twofold:
- A desktop application to simplify downloading, installing & managing DCS Liveries.
- An automatic livery sharing mod for DCS.

[![Download][download]](https://github.com/Camble/LiveryLink/releases/download/v0.11.8/LiveryLink.v0.11.8.zip)

Click the screenshot to watch a short video

[![Watch the video][screenshot]](https://youtu.be/h0i65DmegYQ)


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


## Livery Sharing

In order to automatically share liveries to other players, they must also have Livery Link, and the server you are flying on must be running Livery Link Server.

The server will be made available for DCS server hosts with the v1.0 release.


## Recent Changes

### 0.11.8

- Fixed: `Install Scripts` can't properly close DCS


### 0.11.7

- Fixed: Livery install hangs on first ever run of Livery Link

### 0.11.6

- Fixed: When a shared livery is installed, the module can appear twice in the UI
- Fixed: Thumbnail not downloaded when shared livery is installed
- Fixed: Notification on new version download not working

### 0.11.5

- Fixed an issue preventing shared liveries from being installed
- Temp folder will now be cleared when Livery Link exits

### 0.11.4

- Updater can now be run manually
- Reworked script installation flow - user will only be prompted if necessary
- Display friendly module name in Livery Browser
- Fixed: Updater installs latest DCS mod even if mod wasn't installed previously
- Fixed: installing multi-module livery shows duplicate modules in browser
- Fixed: Livery Link fails to launch automatically if moved to a new location

### 0.11.3

- Fixed: Updsate notification not displayed if auto update is enabled
- Fixed: Updater re-downloads the latest version even if it was previously downloaded

### 0.11.2

- Added sharing rules for multi-module liveries & livery packs
- Fixed: Livery thumbnail is overwritten every time an update is made
- Update `DateLastSeen` each time a shared livery is received
- Update `SizeOnDisk` for each previously installed livery

### 0.11.1

- Fixed updater not launching


### 0.11.0

- Updated to .NET 8
- Added auto updater
- Improved 7zip extraction speed (10x)
- Restyled livery browser
- Disk space is now recorded for each livery installed
- Linked Liveries for community modules will only be downloaded if the mod is installed
- Fixed: All liveries from the same pack have the same name
- Fixed: Can't delete Livery thumbnail while Livery Link is running
- Fixed: Liveries not shared properly when connecting to server
- Fixed an issue installing liveries where `description.lua` doesn't specify the livery name
- Properly fixed sharing multiple liveries
- Fixed an issue when sharing more than one livery
- Added support to install liveries for community mod aircraft
- Fixed socket timeout issue when installing livery for the first time
- Display DCS server name in status bar when connected
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


## Roadmap

- [x] Auto-launch with DCS
- [x] 7z support
- [x] RAR support
- [x] Progress indicator
- [x] Installer (partly done - automatically installs scripts)
- [x] Update checker
- [x] Auto-update
- [ ] Livery Manager UI for the desktop client
- [ ] Dark theme
- [ ] Livery auto-update
- [ ] Customize which liveries are shared with other players
- [ ] Customize which liveries to accept from other players
- [ ] Blacklist download of liveries for certain modules, or above a certain size
- [ ] Auto-delete old liveries
- [ ] Disk space quota
- [ ] Server software release
- [ ] Support to share "server-side" liveries (server owner can share livery with players who fly on their server)
- [ ] Optional support for liveries hosted on untrusted hosts
- [ ] Custom cockpit installer
- [ ] One-click default livery unlocker
- [ ] Livery optimizer (compress textures & symlink shared files)
- [ ] Mod options to customise auto-launch

<p align="right">(<a href="#livery-link">back to top</a>)</p>

[screenshot]: https://github.com/Camble/LiveryLink/blob/main/screenshot-0.11.0.png
[download]: https://github.com/Camble/LiveryLink/blob/main/download.png