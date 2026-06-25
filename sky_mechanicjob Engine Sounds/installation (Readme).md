# Engine Sounds Installation Guide

## Overview

This package adds custom engine sound support for the mechanic job system.

The configuration contains pre-configured engine sounds that can be selected directly in-game.

---

## Requirements

Before installing the configuration, make sure you have downloaded and installed the required engine sound pack.

Download the sound pack from the **trusted download link provided in the Folder**.

> **Important:**
> The engine sound pack must be installed correctly on your server before any custom engine sounds will work.

---

## Installation

### Step 1 - Download the Sound Pack

Download and install the engine sound pack using the trusted link included in the Folder.

Follow the installation instructions provided with the sound pack.

---

### Step 2 - Replace the Configuration File

Navigate to:

```text
sky_mechanicjob/config/
```

Replace the existing file:

```text
engine_sounds_config.lua
```

with the provided version from this package.

---

## Adding New Engine Sounds

To add a new engine sound, open:

```text
sky_mechanicjob/config/engine_sounds_config.lua
```

Locate the `sounds` table:

```lua
sounds = {
    { audioName = "SULTAN2", label = "Karin Sultan RS" },
}
```

Add a new entry using the following format:

```lua
{ audioName = "SOUNDNAME", label = "Display Name" },
```

### Example

```lua
{ audioName = "R35SOUND", label = "Nissan GT-R R35" },
```

### Parameters

| Parameter   | Description                                  |
| ----------- | -------------------------------------------- |
| `audioName` | The sound name from the installed sound pack |
| `label`     | The name displayed inside the mechanic menu  |

---

## Example

```lua
sounds = {
    { audioName = "R35SOUND", label = "Nissan GT-R R35" },
    { audioName = "AUDR8TTENG", label = "Audi R8 Twin Turbo" },
    { audioName = "LAMBOV10", label = "Lamborghini V10" }
}
```

---

## Notes

* The `audioName` must exactly match the sound name included in the installed sound pack.
* Engine sounds will not appear if the corresponding sound is missing from the server.
* Always restart the Server after modifying the configuration.

```text
ensure sky_mechanicjob
```

---

## Support

If an engine sound does not work:

1. Verify that the sound pack is installed correctly.
2. Verify that the `audioName` matches the sound pack name exactly.
3. Verify that `engine_sounds_config.lua` has been replaced inside:

```text
sky_mechanicjob/config/
```

4. Restart the Server and test again.

```
```
