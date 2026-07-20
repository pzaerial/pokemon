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
  - a. Change RetroArch's save file location:
    - Go to `Settings → Directory` and choose `Save Files`. Browse to this repo.
    - Go to `Main Menu → Configuration File → Save Current Configuration` to lock in changes.
  - b. Write directly to ROM location:
    - DISCLAIMER: Don't share your ROM files with others who don't own the games. Use a private repo or .gitignore ROM files.
    - Go to `Settings → Saving` and toggle on `Write Saves to Content Directory`. This makes RetroArch write .sav files to that location.
