# VSCode & Linux Notes

## VSCode Shortcuts:

### Productivity

| Shortcut | Action |
|----------|--------|
| Ctrl + P | Open Search Bar |
| Ctrl + B | Toggle Explorer |
| Ctrl + / | Single Line Comment |
| Ctrl + Shift + A | Multiline Comment |
| Ctrl + Arrows | Scrollbar |
| Ctrl + ` | Toggle Terminal |
| Ctrl + F | Find Text |
| Ctrl + S | Save File |
| Ctrl + W | Close File |
| Ctrl + K + Z | Zen Mode |
| Ctrl + Shift + I | Format the Entire Code File |
| Ctrl + K or Ctrl + F | Format Selected Text |

### Text Editing

| Shortcut | Action |
|----------|--------|
| Ctrl + A | Select All |
| Ctrl + C | Copy |
| Ctrl + V | Paste |
| Ctrl + Z | Undo |
| Ctrl + Y | Redo |
| Ctrl + X | Cut and Copy |
| Shift + Ctrl + C | Special Copy (In Terminal) |
| Shift + Ctrl + V | Special Paste (In Terminal) |
| Shift + Ctrl + Arrows | Fixed Multiline Cursor (Vertical) |
| Ctrl + Click | Flexible Multiline Cursor |
| Shift + Left/Right Arrows | Select characters or lines |
| Shift + Ctrl + Left/Right Arrows | Select full words and lines |
| Alt + Numbers | Navigate Between Open Files |
| Alt + Arrows | Move Code Line |

## Linux Commands and Terminal Shortcut

### 1. Terminal:
| Shortcut           | Action                                    |
| ------------------ | ----------------------------------------- |
| `Ctrl + Shift + T` | Open new terminal tab                     |
| `Ctrl + Shift + N` | Open new terminal window                  |
| `Ctrl + Shift + C` | Copy selected text                        |
| `Ctrl + Shift + V` | Paste text                                |
| `Ctrl + L`         | Clear terminal                            |
| `Ctrl + C`         | Stop running command                      |
| `Ctrl + Z`         | Suspend running command                   |
| `Ctrl + D`         | Exit terminal / logout                    |
| `Ctrl + R`         | Search command history (reverse-i-search) |
| `ALT + Tab`        | Switch between open applications          |

### 2. File and Folder Management
| Command                     | Description                                       |
| --------------------------- | ------------------------------------------------- |
| `ls`                        | List files in the current directory               |
| `ls -l`                     | Detailed list with permissions, owner, size, date |
| `ls -a`                     | List all files including hidden (`.`) files       |
| `cd <directory>`            | Change directory                                  |
| `cd ..`                     | Go up one directory                               |
| `pwd`                       | Print working directory                           |
| `mkdir <foldername>`        | Create a new folder                               |
| `rmdir <foldername>`        | Remove empty folder                               |
| `rm -r <foldername>`        | Remove folder and contents recursively            |
| `touch <filename>`          | Create a new empty file                           |
| `cp <source> <destination>` | Copy file or folder (`-r` for folder)             |
| `mv <source> <destination>` | Move or rename file/folder                        |
| `rm <filename>`             | Delete a file                                     |
| `file <filename>`           | Show file type                                    |
| `cat <filename>`            | Display file contents                             |
| `less <filename>`           | View file contents page by page                   |
| `head <filename>`           | Show first 10 lines                               |
| `tail <filename>`           | Show last 10 lines                                |
| `tail -f <filename>`        | Follow file output in real time                   |


### 3. System Information
| Command    | Description                                                              |
| ---------- | ------------------------------------------------------------------------ |
| `uname -a` | Show kernel version and system info                                      |
| `hostname` | Show hostname                                                            |
| `uptime`   | Show system uptime and load                                              |
| `top`      | Display real-time running processes                                      |
| `htop`     | Interactive process viewer (needs installation: `sudo apt install htop`) |
| `df -h`    | Show disk usage in human-readable format                                 |
| `free -h`  | Show RAM usage                                                           |
| `lsblk`    | List block devices (disks and partitions)                                |
| `whoami`   | Show current user                                                        |
| `id`       | Show user ID and groups                                                  |


### 4. System Updates and Package Management (Debian/Raspberry Pi OS)
| Command                      | Description                              |
| ---------------------------- | ---------------------------------------- |
| `sudo apt update`            | Refresh package lists from repositories  |
| `sudo apt upgrade`           | Upgrade installed packages               |
| `sudo apt full-upgrade`      | Upgrade packages and handle dependencies |
| `sudo apt install <package>` | Install a new package                    |
| `sudo apt remove <package>`  | Remove a package                         |
| `sudo apt autoremove`        | Remove unused dependencies               |
| `sudo reboot`                | Reboot the system                        |
| `sudo shutdown now`          | Shutdown immediately                     |
| `sudo shutdown -h +5`        | Shutdown in 5 minutes                    |


### 5. SHA Key Verification
| Command                             | Description                    |
| ----------------------------------- | ------------------------------ | 
| `sha256sum <filename>`              | Compute SHA-256 hash of a file |                                          
| `sha1sum <filename>`                | Compute SHA-1 hash of a file   |                                          
| `md5sum <filename>`                 | Compute MD5 hash of a file     |                                          

`echo "<expected_hash>  <filename>" | sha256sum -c - ` ==>  Verify file against a known SHA-256 hash


### 6. Chromium:

| Shortcut             | Action                      |
| -------------------- | --------------------------- |
| `Ctrl + T`           | Open new tab                |
| `Ctrl + W`           | Close tab                   |
| `Ctrl + Shift + T`   | Reopen last closed tab      |
| `Ctrl + Tab`         | Switch to next tab          |
| `Ctrl + Shift + Tab` | Switch to previous tab      |
| `Ctrl + L`           | Focus address bar           |
| `Ctrl + R`           | Refresh page                |
| `Ctrl + Shift + R`   | Hard refresh (ignore cache) |
