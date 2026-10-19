# bepinex-installer

**One double-click installer that puts [BepInEx](https://github.com/BepInEx/BepInEx) into your
Gorilla Tag folder.** No unzipping, no hunting for the right folder — it finds the game, installs
BepInEx, and sets up the `plugins` folder so you can drop a menu in and go.

## What it does

1. **Finds Gorilla Tag automatically** — checks the usual Steam and Oculus library locations
2. **Downloads** the official BepInEx `v5.4.23.4` (win_x64) release straight from GitHub
3. **Extracts** it directly into the game folder
4. **Creates** `BepInEx/config` and `BepInEx/plugins`, ready for mods

If Gorilla Tag isn't in a known location, it asks for the path once and carries on.

## How to use

1. Download **`Beplnex.bat`** from this repo
2. Double-click it
3. Wait for "Done!" — then launch the game

> Windows may warn about a `.bat` from the internet: choose **More info → Run anyway**.
> The first game launch after installing generates the BepInEx config files.

## Then install a menu

Drop your menu DLL into the plugins folder, e.g. for [Mane.DB](https://github.com/harvs-phoenix/Mane.DB):

```
Gorilla Tag/BepInEx/plugins/Mane.DB/Mane.DB.dll
```

## Detected install locations

| Platform | Path |
| --- | --- |
| Steam (default) | `C:\Program Files (x86)\Steam\steamapps\common\Gorilla Tag` |
| Steam (D: library) | `D:\SteamLibrary\steamapps\common\Gorilla Tag` |
| Steam (alt D:) | `D:\Steam\steamapps\common\Gorilla Tag` |
| Oculus | `C:\Program Files\Oculus\Software\Software\another-axiom-gorilla-tag` |

Anything else — paste the folder path when prompted.

## Reinstall / uninstall

- **Re-running the installer is safe** — it overwrites the BepInEx files cleanly.
- **To uninstall mods**, just delete the `BepInEx` folder from the game directory.

## Credits

Based on community installer code — thanks to **II Community**. BepInEx itself is by the
[BepInEx team](https://BepInEx.github.io).
