# Livery Link

> Note: From v0.22.0, releases of Livery Link will include a zipped folder to make installation easier. If you are on v0.19.0 or earlier, you will need to manually update to the newer version before the auto-updater will handle this new folder structure.

## Requirements

- .NET 8 is required to run Livery Link. You will be prompted to install it if you don't already have it.

## About

Livery Link's purpose is twofold:
- A desktop application to simplify downloading, installing & managing DCS Liveries.
- An automatic livery sharing mod for DCS.

[![Download][download]](https://github.com/Camble/LiveryLink/releases/download/v0.22.3/LiveryLink.v0.22.3.zip)

Click the screenshot to watch a short video

[![Watch the video][screenshot]](https://youtu.be/h0i65DmegYQ)


## How Does It Work?

- Liveries must be installed with Livery Link to be shared.
- When you connect to a server which has Livery Link running, your client will connect.
- When you take off, your current livery will be shared with other players.
- When another player shares a livery with the server, your client will download and install it automatically.


## Installation

1. Extract all contents into the folder of your choice.
1. Run `LiveryLink.exe` to initialize the app.
1. Locate your `Saved Games\DCS` folder if prompted.
1. Choose `Yes` to install the scripts.


## Livery Sharing

In order to automatically share liveries to other players, they must also have Livery Link, and the server you are flying on must be running Livery Link Server.

The server will be made available for DCS server hosts with the v1.0 release. Pre-release is available for Patreon supporters.


## Recent Changes

### 0.23.0

- `Mods` & `Scripts` are now embedded into Livery Link, making the installation process simpler
- Fixed: NullReferenceException when extracting "solid" RAR archives (previous fix was a workaround for a specific example)
- Fixed: `manifest.json` AppVersion mistakenly updates when updating SeenCount of a livery

---

<details>
<summary>Changelog for previous versions</summary>

### 0.22.3

- Fixed: Received share is re-downloaded even when previously "Deleted Forever"

### 0.22.2

- Fixed: UI hangs and progress bar doesn't update when extracting liveries to disk

### 0.22.1

- Fixed: NullReferenceException when installing liveries from RAR.

### 0.22.0

- Feature: Delete Livery from within the new right-click context menu.
- Feature: Drag an image into the Livery Link window to use it as a thumbnail for that livery. Ideal for local files, which only display the default thumbnail.
- Improvement: When attempting to resolve which aircraft a livery is for and there are multiple matches (i.e. A10A, A10C, A10CII), check if there is one single installed module. If so, use this. Otherwise, the selection dialog will only display the possible modules.

---

### 0.21.3

- Fixed: Install notification gets stuck open

### 0.21.2

- Fixed: NullReferenceException when installing livery where texture files are not inside a subfolder
- Adjusted logging config to only keep 7 days of logs

### 0.21.1

- Fixed: Repeating "There was a problem installing the Livery Link mod" error
- Removed: F-5E 2024 from F-5E compatible modules

### 0.21.0

- Added: F-5E 2024
- Changed Livery name prefix from asterisk (*) to bullet (•) - I may make this customisable in future
- Improved error handling
- Improved performance of description.lua updates
- Server: Reduced logging noise 
- Server: Modified handshake
- Server: Fixed issue with sharing liveries when player reslots and returns to an aircraft

### 0.20.1

- Consolidate notifications when received liveries are installed
- Consolidate notifications when shared liveries are accepted
- Update Mig-29 texture definitions (fixes module detection)
- Increment livery ShareCount when shared livery is accepted

### 0.20.0

- Improved updater ready for future update with different folder structure
- Fixed: Double-clicking a livery won't open the folder where the path contains a comma

---

### 0.19.10

- Refactored aircraft detection by livery contents

### 0.19.9

- Fixed: Notification doesn't work when livery share has been accepted

### 0.19.8

- Fixed: Always prompted to select aircraft when installing livery

### 0.19.7

- Fixed: Ka-50 (Black Shark 3) liveries incorrectly installed as Black Shark 2
- Added used disk space to Livery card

### 0.19.6

- Fixed: Shared livery acceptance is incorrectly reported
- Fixed: DateLastSeen not updated correctly for livery packs
- Fixed: Certain image filetypes (png/jpg) are not extracted when installing liveries
- Fixed: Liveries requested from player even when in co-pilot seat

### 0.19.5

- Automatically highlight download URL text on focus
- Check for updates on exit

### 0.19.4

- Fixed: Always prompting to select aircraft when installing livery

### 0.19.3

- Fixed: Error when trying to open Options
- Fixed: Error when installing liveries for unknown modules

### 0.19.2

- Fixed an issue where corrupt `config.json` would prevent Livery Link from starting
- Added logging on startup to help diagnose future issues

### 0.19.1

- Improved module detection for user mod aircraft
- Fixed: Prompted to select aircraft every single livery in a pack

### 0.19.0

- Added notification when a shared livery is downloaded by other players
- Fixed: not prompted for module selection when installing unknown livery from disk
- Fixed: various issues when installing from disk
- General stability improvements

---

### 0.18.15

- Error when extracting invalid liveries from Zip now displays correctly for 7z and RAR archives.

### 0.18.14

- Removed: Test exception when installing liveries

### 0.18.13

- Fixed: Various errors during installation of liveries
- Added: About window

### 0.18.12

- Fixed: Liveries for third party mod aircraft don't show in the browser

### 0.18.11

- Fixed: Unable to install a livery from ED User Files that has no screenshot

### 0.18.10

- Clarified error messages when extraction fails

### 0.18.9

- Fixed: NullReferenceException when installing livery

### 0.18.8

- Added CH-47F

### 0.18.7

- Fixed: Duplicate error notification when installing an invalid livery

### 0.18.6

- Pressing `Enter` now works to install liveries

### 0.18.5

- Fixed: F-4E liveries not correctly detected (again)

### 0.18.4

- Fixed: Livery Link won't launch automatically with DCS

### 0.18.3

- Fixed: Incorrect livery name when `description.lua` uses `name_ru=` instead of `name=`

### 0.18.2

- Fixed: Liveries installed from local disk don't appear in the Livery browser

### 0.18.1

- Fixed: `Value cannot be null. (Parameter 'path2')` when installing liveries

### 0.18.0

- Added drag and drop livery installation

---

### 0.17.4

- Fixed: Unable to install liveries from non-English URLs

### 0.17.3

- Added support for OH58D Kiowa

### 0.17.2

- Fixed: Progress notification remains open if livery download is cancelled

### 0.17.1

- Fixed: F-4E liveries not correctly detected

### 0.17.0

- Added "Group by Aircraft" to Liveries menu
- Moved progress bar into notification instead of main window
- Refactored how liveries are stored in memory
- Standardised mod installation logic across Livery Link and Updater

---

### 0.16.6

- Fixed: updater won't launch automatically if username contains a space

### 0.16.5

- Fixed an issue when checking if DCS is running

### 0.16.4

- Added some logging for those who have auto-update problems

### 0.16.3

- Fixed: auto-updater installs DCS mod even if previously not installed by user

### 0.16.2

- Fixed a minor auto-updater issue 

### 0.16.1

- Fixed a minor issue with error logging

### 0.16.0

- Fixed conflict with F-4E Phantom II module

---

### 0.15.2

- Fixed: LiveryLink doesn't close automatically if DCS is running as an Administrator

### 0.15.1

- Fixed errors during Install/Removal of DCS Mod/Script

### 0.15.0 - Livery Browser Refactor

- Window can now also be resized horizontally
- Fixed: Deleting a module folder from the disk doesn't update the Livery Browser view

---

### 0.14.7

- Fixed some issues detecting DCS running process
- Added more notifications in the event of an error when downloading liveries


### 0.14.6

- Display an error if attempting to overwrite a mod file that's in use


### 0.14.5

- Fixed: `Livery not found` error when installing any livery

### 0.14.4

- Fixes a minor issue with the previous version

### 0.14.3

- Display error notification if livery could not be downloaded

### 0.14.2

- Fixed: Unable to detect if DCS has been closed if launched as Administrator

### 0.14.1

- Fixed: App can be launched more than once

### 0.14.0

- Improved how server/client communicate

---

### 0.13.8

- Fixed an issue communicating with DCS

### 0.13.7

- Fixed: settings not saved when closing settings window

### 0.13.6

- Fixed an issue detecting if DCS is running
- Fixed an issue opening connection to DCS to listen for events
- Minor tweaks to error handling

### 0.13.5

- Fixed: updater can only extract to existing folders

### 0.13.4

- Fixed a bug, which allowed multiple instances of Livery Link

### 0.13.3

- Added `Remove Mod` feature to `Tools` menu
- Fixed: Options window cannot be re-opened once closed

### 0.13.2

- Window can now be resized vertically
- Added `SeenCount` to keep track of how often liveries are seen
- Fixed: Options window can be opened twice
- Fixed: Issue reading livery details from folder


### 0.13.1

- Scripts installer now provides the option to postpone installation until DCS exits


### 0.13.0

- Improved sharing: only liveries selected by the player will be shared on takeoff

---

### 0.12.2

- Minor bugfixes

### 0.12.1

- Fixed: Crash on first run

### 0.12.0

- Browser will now update if a livery is deleted from the disk
- Liveries are sorted by `DateInstalled`
- Added `Liveries` menu with `Show All` option to separate your own liveries from those shared with you
- Added logging when liveries are installed
- Added notification when there was a failed livery installation
- `LiveryLinkUpdater.exe` now generates a log file to aid debugging
- Set IsInstalled to true if description.lua exists when loading liveries
- Fixed: Shared livery is downloaded twice if shared again when download is in progress

---

### 0.11.9

- Fixed an issue preventing shared liveries from being installed

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
</details>

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

<p align="right">(<a href="#livery-link">back to top</a>)</p>

[screenshot]: https://github.com/Camble/LiveryLink/blob/main/screenshot-0.17.0.png
[download]: https://github.com/Camble/LiveryLink/blob/main/download.png