# WSL2 Commands

## Install WSL2
- `wsl --install`

Restart the PC to ensure WSL installs correctly.

---

### Show all available Linux distributions
```bash
wsl --list --online
```

### Install a specific distribution
```bash
wsl --install <distro-name>
```

### Enter directly into the default distribution
```bash
wsl
```

### Enter a specific distribution
```bash
wsl -d <DistroName>
```

### Enter a specific distribution with a specific username and directory
```bash
wsl -d <DistroName> -u <username> --cd /home/<username>
```

### Set a specific distribution as the default
```bash
wsl --set-default <DistroName>
```

### View installed distributions
```bash
wsl --list --verbose
```

### Backup an installed distribution
```bash
wsl --export <DistroName> D:\Backups\<name>.tar
```
**Example:**
```bash
wsl --export Ubuntu-22.04 D:\Backups\ubuntu.tar
```

### Unregister (delete) an installed distribution
```bash
wsl --unregister Ubuntu-22.04
```

### Restore a backup
```bash
wsl --import <new_name> <destination_path> <backup_file_path>
```

### Stop a running distribution
```bash
wsl --terminate Ubuntu-22.04
```

---

### Location of all WSL operating systems
```
C:\Users\<YourUser>\AppData\Local\Packages\
```
