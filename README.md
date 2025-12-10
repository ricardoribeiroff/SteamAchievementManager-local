# Steam Achievement Manager (SAM) - LOCAL SAVE FORK

This repository contains a modified fork of the original Steam Achievement Manager (SAM) open-source tool.

**The core functionality of this fork has been changed:** **Achievement modifications are NOT pushed to the Steam API.** Instead, the tool captures the selected achievement state and saves it locally to a persistent INI file.

## 💾 Local Achievement Saving Feature

When the "Store" or "Commit" button is pressed, this application performs the following actions:

1.  **Fixed Base Path:** The tool targets a fixed directory on the system: `C:\Users\Public\Documents\Steam\RUNE`.
2.  **Game Directory Creation:** A subdirectory is created within the base path, named after the game's **AppID**.
3.  **Local File Saving:** The achievement states are saved to a file named **`achievements.ini`** within the AppID folder.

### INI File Format

The generated `achievements.ini` uses a custom section structure, including the Unix timestamp for when the achievement was last marked as unlocked:

```ini
[ACHIEVEMENT_01]
Achieved=1
UnlockTime=1765384860

[ACHIEVEMENT_37]
Achieved=1
UnlockTime=1765384980