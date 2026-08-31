# WorldBoxAccess
Screen reader accessibility for WorldBox.
WorldBoxAccess adds screen reader output, keyboard-friendly navigation, accessible managers, inspect windows, powers, scanner systems, and major gameplay support for WorldBox.
Note: this project is now in a strong beta state. The mod is functionally complete, but runtime edge cases may still appear during broader tester use.
## Installation
### Requirements
- WorldBox
- the WorldBoxAccess release package
### Step 1: Extract The Release Package
The release package already includes:
- BepInEx
- `WorldBoxAccess.dll`
- `Tolk.dll`
- `nvdaControllerClient64.dll`
Extract everything from the zip archive directly into the main WorldBox game folder.
### Step 2: Start The Game
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
- creature follow and focus navigation
- directional world navigation
- event speech and event history menu
- inspect windows for units, cities, kingdoms, and deeper civilization windows
- manager hub and favorites
- world info, settings, saves, laws, and other major built-in windows
## Main Controls
These are the main global controls. Use `F1` in-game for context-sensitive help.
- `F1`: read help for the current context
- `F2`: open Managers
- `F3`: open Favorites
- `F4`: open the gameplay toolbar
- `Tab`: open the powers menu
- `Alt+E`: open the event menu
- `Alt+1` through `Alt+0`: set game speed
- `Space`: pause or resume time
- `Escape`: go back or open quit, depending on context
## Map Cursor
The map cursor is the core gameplay navigation layer.
- `Arrow Keys`: move between tiles
- `Enter`: inspect the current tile or use the current map power, depending on context
The mod speaks:
- coordinates
- terrain and biome
- buildings
- units on the tile
- city and kingdom context
## Directional Navigation
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
## Powers Menu
The powers menu is fully keyboard-accessible.
- `Tab`: open powers
- `Up` / `Down`: move between categories and powers
- `Right Arrow`: expand category
- `Left Arrow`: collapse or return
- `Enter`: activate current power
- `Escape`: close the powers menu
## Power Placement
The mod supports multiple placement models, depending on how the real game power works:
- single tile targeting
- exact rectangle selection
- one-shot special targeting
- info and inspect targeting
Many powers now have spoken effect hints so players know whether a power is:
- single target
- rectangle based
- brush based
- moving cloud or moving area
- charge-and-release
## Managers
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
- plots
- armies
Inside the hub:
- `Up` / `Down`: move between managers
- `Enter` or `Right Arrow`: open current manager
- `Escape`: close the hub
## Favorites
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
The mod adds:
- top summary rows for important information
- direct related-object actions
- rename where the real game supports it
- favorite actions where safe and supported
Examples of direct inspect actions:
- open home city
- open kingdom
- open alliance
- open culture, language, or religion
- open clan, family, or plot
- start civilization
- found city
- open capital, king, or heir
- open founder, leader, captain, or instigator
## Scanner
The scanner gives a structured way to search and jump through the world.
- `Ctrl+PageUp` / `Ctrl+PageDown`: change categories
- `Shift+PageUp` / `Shift+PageDown`: change subcategories
- `PageUp` / `PageDown`: change items
- `Alt+PageUp` / `Alt+PageDown`: change current locations for the selected item
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
- city and kingdom context when relevant
## Event Menu
`Alt+E` opens the event history menu.
- `Up` / `Down`: move between events
- `Left` / `Right`: change event categories
- `Enter`: read selected event
- `Space`: jump to event location
- `Delete`: remove selected event
- `Shift+Delete`: remove all events in the current category
- `Escape`: close the event menu
## Event Coverage
The event system combines real built-in WorldBox history with custom blind-first event coverage where the base game does not log enough information.
This includes broad support for:
- kingdom and city events
- war and alliance events
- civilization milestones
- creature deaths and important births
- disasters
- achievement unlocks
- culture, language, religion, clan, family, and related world-state changes
## Settings And Other Windows
The mod also includes accessibility support for major built-in windows such as:
- settings
- save and load
- quit
- world laws
- world info
- event history
- trait editor
- equipment rain editor
- tutorial flows
`F1` gives context help in these windows too.
## Tester Feedback
The most useful bug reports include:
- the exact spoken line
- the exact keys pressed
- which screen or menu was open
- what should have happened instead
At this stage, the most important remaining work is live beta feedback and runtime edge-case cleanup.
