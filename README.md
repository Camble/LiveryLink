# Livery Link

## About

Livery Link's purpose is twofold:
- A desktop application to simplify downloading, installing & managing DCS Liveries.
- An automatic livery sharing mod for DCS.

## Requirements

- .NET 7 is required to run Livery Link

## Installation

Livery Link will run without installation. However, the script must be installed in your `Saved Games\DCS\Scripts\Hooks` folder if you want to share or receive shared liveries.


## Desktop Client

The UI is currently very barebones. Paste in a Livery URL from [DCS User Files](https://www.digitalcombatsimulator.com/en/files/) to install it.

There is no progress bar yet, but you should be notified when complete.


## Livery Sharing

In order to automatically share liveries to other players, they must also have Livery Link, and the server you are flying on must be running Livery Link Server.


## Getting Started

See [releases](https://github.com/Camble/LiveryLink/releases) for download links.

## Known Issues

- Detected or chosen folders cannot be changed yet. Settings can be cleared by deleting or modifying the `user.config` file from `%AppData%\Local\LiveryLink`
- Currently only ZIP files can be installed. RAR & 7z support is coming in a future release.

## Roadmap

- [ ] An actual UI (Livery Manager) for the desktop client
- [ ] Auto-launch with DCS
- [ ] RAR support
- [ ] 7z support
- [ ] Customize which liveries are shared with other players
- [ ] Customize which liveries to accept from other players
- [ ] Blacklist download of liveries for certain modules, or above a certain size
- [ ] Auto-delete old liveries
- [ ] Disk space quota
- [ ] Support to share "server-side" liveries (server owner can share livery with players who fly on their server)

<p align="right">(<a href="#readme-top">back to top</a>)</p>