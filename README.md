# Livery Link

## About

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


## Installation

The only installation required is to copy the `Mods` and `Scripts` folder into your `Saved Games\DCS World\` folder if you want to share or receive shared liveries.
Run `LiveryLink.exe` once to complete the setup.


## Desktop Client

The UI is currently very barebones. Paste in a Livery URL from [DCS User Files](https://www.digitalcombatsimulator.com/en/files/) to install it.

There is no progress bar yet, but you should be notified when complete.

# Settings

If you need to clear the stored settings (e.g. your chosen liveries folder location), delete the `%AppData%\Local\LiveryLink` folder.


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
- [x] 7z support (upcoming v0.5.0)
- [x] RAR support (upcoming v0.5.0)
- [ ] An actual UI (Livery Manager) for the desktop client
- [ ] Auto-updater
- [ ] Installer
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

<p align="right">(<a href="#readme-top">back to top</a>)</p>