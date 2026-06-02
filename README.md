Markdown

# 🌌 DISCORD-ORBS-

A quick guide to unlocking Discord's built-in Developer Tools and modifying window configurations by replacing your `settings.json` file.

---

## 🪟 Windows Setup

### 1. Open the Discord Configuration Folder
* Press **Windows + R** on your keyboard to open the **Run** dialog box.
* Alternatively, search for **Run** in the Windows search bar and open it.
* Type or paste the following path and press **Enter**:
```cmd
  %appdata%\discord

2. Modify the Settings File

    In the File Explorer window that opens, look for the file named settings.json.

    Open it with a text editor (like Notepad), delete all the existing code inside, and replace it completely with the block below:

JSON

{
  "IS_MAXIMIZED": true,
  "IS_MINIMIZED": false,
  "WINDOW_BOUNDS": {
    "x": 112,
    "y": 60,
    "width": 1284,
    "height": 724
  },
  "DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true,
  "MIN_WIDTH": 940,
  "MIN_HEIGHT": 500,
  "chromiumSwitches": {}
}

    Save and close the file, then restart Discord.

🐧 Linux Setup

For Linux users, you can instantly wipe and rewrite the configuration file using a single terminal command.
Run the Ultimate One-Liner

Fully close Discord first (killall Discord), then open your terminal and execute this entire block:
Bash

cat << 'EOF' > $(find ~ -name "settings.json" 2>/dev/null | grep -i discord | head -n 1)
{
  "IS_MAXIMIZED": true,
  "IS_MINIMIZED": false,
  "WINDOW_BOUNDS": {
    "x": 112,
    "y": 60,
    "width": 1284,
    "height": 724
  },
  "DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true,
  "MIN_WIDTH": 940,
  "MIN_HEIGHT": 500,
  "chromiumSwitches": {}
}
EOF

    🛠️ Note: Once configured, launch Discord and press Ctrl + Shift + I to toggle the Developer Tools Console.
