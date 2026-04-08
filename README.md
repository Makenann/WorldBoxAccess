# WorldBoxAccess
Screen reader accessibility for WorldBox
This mod adds screen reader output, keyboard-friendly navigation, accessible managers, inspect windows, powers, scanner systems, and major gameplay support for WorldBox.
Note: this project is now in a strong beta state. The mod is functionally complete, but runtime edge cases may still appear during broader tester use.
## Table of Contents
- Installation
- What This Mod Covers
- Main Controls
- Gameplay Navigation
- Powers And Placement
- Managers And Favorites
- Inspect Windows
- Scanner System
- Creature Focus
- Events
- Settings And Other Windows
- Building From Source
- Tester Feedback
## Installation
### Requirements
- WorldBox
- BepInEx installed for WorldBox
- `Tolk.dll`
- `nvdaControllerClient64.dll`
### Step 1: Install BepInEx
Install BepInEx for WorldBox first. Start the game once after installing it so the `BepInEx` folders are created, then close the game.
Expected structure after BepInEx is installed:
```text
WorldBox\
├── BepInEx\
│   ├── core\
│   └── plugins\
├── worldbox.exe
└── ...
```
### Step 2: Install WorldBoxAccess
Copy the files like this:
```text
WorldBox\
├── BepInEx\
│   └── plugins\
│       └── WorldBoxAccess.dll
├── Tolk.dll
├── nvdaControllerClient64.dll
└── ...
```
### Step 3: Start the Game
Launch WorldBox.
If the mod loaded correctly, you should hear:
`WorldBoxAccess loaded. F1 for help.`
## What This Mod Covers
Current accessibility coverage includes:
- startup and menu access
- tutorial accessibility
- map browsing with keyboard tile navigation
- powers menu and map placement flows
- exact rectangle placement for many power families
- one-shot power targeting
- scanner navigation
- creature follow/focus navigation
- directional world navigation
- event speech and event history menu
- inspect windows for units, cities, kingdoms, and deeper civilization windows
- manager hub and favorites
- rename and favorite actions
- world info, settings, saves, laws, and other major built-in windows
## Main Controls
These are the main global controls. Use `F1` in-game for context-sensitive help.
- `F1`: read help for the current context
- `F2`: open Managers
- `F3`: open Favorites
- `Tab`: open the powers menu
- `Shift+Tab`: open the gameplay toolbar
- `Alt+E`: open the event menu
- `Alt+1` through `Alt+0`: set game speed
- `Space`: pause or resume time
- `Escape`: go back or open quit, depending on context
## Gameplay Navigation
### Map Cursor
The map cursor is the core gameplay navigation layer.
- `Arrow Keys`: move between tiles
- `Enter`: inspect the current tile or use the current map power, depending on context
The mod speaks:
- coordinates
- terrain and biome
- buildings
- units on the tile
- city and kingdom context
### Directional Navigation
Directional navigation jumps between nearby world objects.
- `Shift+Up` / `Shift+Down`: cycle categories
- `Shift+Left` / `Shift+Right`: change tile distance in `Tiles`
- `Ctrl+Arrow Keys`: move to the nearest object in that direction
Current categories:
- kingdoms
- cities
- biomes
- creatures
- buildings
- tiles
## Powers And Placement
The powers menu is fully keyboard-accessible.
- `Tab`: open powers
- `Up` / `Down`: move between categories and powers
- `Right Arrow`: expand category
- `Left Arrow`: collapse or return
- `Enter`: activate current power
The mod supports multiple placement models, depending on how the real game power works:
- single tile targeting
- exact rectangle selection
- one-shot special targeting
- info/inspect targeting
Many powers now have spoken effect hints so players know whether a power is:
- single target
- rectangle based
- brush based
- moving cloud / moving area
- charge-and-release
## Managers And Favorites
### Managers Hub
`F2` opens a blind-first hub that launches the real global WorldBox manager windows.
Current manager entries include:
- world info
- kingdoms
- cities
- wars
- alliances
- clans
- families
- languages
- religions
- cultures
- subspecies
- plots
- armies
Inside the hub:
- `Up` / `Down`: move between managers
- `Enter` or `Right Arrow`: open current manager
- `Escape`: close the hub
### Favorites
`F3` opens Favorites.
The favorites window can be used to review favorite units, and favorite state can also be toggled from many inspect and manager flows.
## Inspect Windows
Inspect windows are one of the main strengths of the mod.
Accessible inspect support includes:
- units
- cities
- kingdoms
- alliances
- armies
- plots
- wars
- languages
- cultures
- religions
- clans
- families
- subspecies
The mod adds:
- top summary rows for important information
- direct related-object actions
- rename where the real game supports it
- favorite actions where safe and supported
Examples of direct inspect actions:
- open home city
- open kingdom
- open alliance
- open culture / language / religion
- open clan / family / plot / subspecies
- start civilization
- found city
- open capital / king / heir
- open founder / leader / captain / instigator
## Scanner System
The scanner gives a structured way to search and jump through the world.
- `Ctrl+PageUp` / `Ctrl+PageDown`: change categories
- `Shift+PageUp` / `Shift+PageDown`: change subcategories
- `PageUp` / `PageDown`: change item positions
- `Alt+PageUp` / `Alt+PageDown`: read detailed items
- `Home`: move to current scanner result
- `Alt+Home`: toggle scanner auto-move
Scanner categories currently include:
- creatures
- buildings
- nature
## Creature Focus
Creature focus is a fast follow system for live units.
- `Ctrl+,` / `Ctrl+.`: change creature categories
- `,` / `.`: change creature within current category
This system moves the camera and map focus to the selected creature and speaks:
- name
- current activity
- combat target when useful
- health state
- role context
- city / kingdom context when relevant
## Events
The event system is a major accessibility layer for WorldBox.
### Event Menu
- `Alt+E`: open event history
- `Up` / `Down`: move between events
- `Left` / `Right`: change event categories
- `Enter`: read selected event
- `Space`: jump to event location
- `Delete`: remove selected event
- `Escape`: close the event menu
### Event Coverage
The event system combines:
- real built-in WorldBox history
- custom blind-first event coverage where the base game does not log enough information
This includes broad support for:
- kingdom and city events
- war and alliance events
- civilization milestones
- creature deaths and important births
- disasters
- culture, language, religion, clan, family, and related world-state changes
## Settings And Other Windows
The mod also includes accessibility support for major built-in windows such as:
- settings
- save/load
- quit
- world laws
- world info
- event history
- equipment rain editor
- tutorial flows
`F1` gives context help in these windows too.
## Building From Source
Build and deploy with the provided PowerShell scripts:
- `scripts\Build-Mod.ps1`
- `scripts\Deploy-Mod.ps1`
Do not use raw `dotnet build` as the normal workflow for this project.
Important project references:
- [docs/game-api.md](docs/game-api.md)
- [project_status.md](project_status.md)
- [docs/distribution-guide.md](docs/distribution-guide.md)
## Tester Feedback
The most useful bug reports include:
- the exact spoken line
- the exact keys pressed
- which screen or menu was open
- what should have happened instead
At this stage, the most important remaining work is live beta feedback and runtime edge-case cleanup.
