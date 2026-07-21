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
These are the options you have for managing `.sav` files, which are used between iOS and desktop OS. **To generate these, you must use the ingame "save" features on desktop OS. IOS emulators like Delta already use only these. Reminder that this is either `Start` or `X` depending on the game you're playing.
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

### Enable Auto-Flush Save States (Optional)
By default, save states are persisted to disk **only on graceful exits of the program**. Instead, we can make RetroArch save every few seconds.
This will help you keep track of your `.state` save state files.
1. Go to `Settings → Saving` and find `SaveRAM Autosave Interval`. Change from `Disabled` to `10 seconds`.
2. Go back to `Main Menu → Configuration File → Save Current Configuration` to save changes.


### Configure Emulator/Games
1. `Load Core` to select your emulator.
2. `Load Content → File Browser → Start Directory` to configure the git repo as the location to search from.
3. `Import Content → Scan Directory` to load items.

## Gameplay
Select your emulator at the bottom of the menu, and select the game to play.

### Emulator Keybinds
| Keybind (Windows / Mac) | Functionality |
| :--- | :--- |
| **`Up` / `Down` / `Left` / `Right` Arrows** | Move character / Navigate menus |
| **`X`** | **A Button** (Confirm / Interact) |
| **`Z`** | **B Button** (Cancel / Run) |
| **`Enter`** *(or `Right Shift` on Mac)* | **Start Button** (Open Pokémon menu) |
| **`Right Shift`** *(or `Return` on Mac)* | **Select Button** (Registered Key Item) |
| **`Q` / `W`** | **L / R Triggers** (GBA/DS) |
| **`S` / `A`** | **X / Y Buttons** (DS only) |
| **`F1`** *(or `fn` + `F1` on Mac)* | Open RetroArch Menu Overlay |
| **`Spacebar` (Hold)** | **Fast-Forward** (Speed up battles/grinding) |
| **`P`** | Pause Emulation |
| **`F2`** *(or `fn` + `F2` on Mac)* | **Save State** (Local machine only) |
| **`F4`** *(or `fn` + `F4` on Mac)* | **Load State** (Local machine only) |
| **`Esc` (Press Twice)** | Instantly Close RetroArch |

For manual rebinds, Press `F1` (or `fn + F1` on Mac) to open quick menu, Press Back twice to reach the Main Menu, then go to `Settings → Input → RetroPad Binds → Port 1 Controls` and rebind what you need.