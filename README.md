# Pokemon
Save states for Pokemon games to be managed as code.

## Setup

### RetroArch
1. Install [RetroArch](https://www.retroarch.com/?page=platforms).
  - Note for Windows: Don't install in `C:\Program Files` directory to avoid permission issues.
2. In `Main Menu → Online Updater`, update the following (at the bottom of the list):
  - Update Core Info Files
  - Update Assets
  - Update Databases
3. Still in `Online Updater`, click `Core Downloader` and download:
  - Nintendo - Game Boy Advance (mGBA)
  - Nintendo - Nintendo DS (melonDS)
4. Options for linking repo files to RetroArch save states:
  - a. Change RetroArch's save file location: (recommended)
    - Go to `Settings → Directory` and choose `Save Files`. Browse to this repo.
    - Go to `Main Menu → Configuration File → Save Current Configuration` to lock in changes.
  - b. Write directly to ROM location: (untested)
    - DISCLAIMER: Don't share your ROM files with others who don't own the games. Use a private repo or .gitignore ROM files.
    - Go to `Settings → Saving` and toggle on `Write Saves to Content Directory`. This makes RetroArch write .sav files to that location.

### Folder Structure Example
```bash
this-repo/
├── .gitignore
├── GBA/
│   ├── GAME.gba
│   └── GAME.sav
└── NDS/
    ├── GAME.nds
    └── GAME.sav
```

### Configure Emulator/Games
1. `Load Core` to select your emulator.
2. `Load Content → File Browser → Start Directory` to configure the git repo as the location to search from.
3. `Import Content → Scan Directory` to load items.

## Play
Select your emulator at the bottom of the menu, and select the game to play.
