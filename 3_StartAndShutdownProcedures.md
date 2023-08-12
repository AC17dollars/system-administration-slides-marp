---
marp: true
paginate: true
author: Abhinav Chalise, Saugat Neupane
headingDivider: 2
footer: 2023-08-13
header: Abhinav Chalise, Saugat Neupane
---

# Start and Shutdown Procedures

## Introduction and Necessity

Start and shutdown procedures are fundamental to managing the lifecycle of a computer system. Starting a system is essential to make it operational, while proper shutdown ensures that all processes are terminated safely before powering off. These procedures are required for routine usage, updates, maintenance, or resolving issues.

## System Startup

### Booting Process Overview

The system startup process involves several stages:

1. **BIOS/UEFI:** When the computer is powered on, the Basic Input/Output System (BIOS) or Unified Extensible Firmware Interface (UEFI) firmware is activated. The BIOS/UEFI performs hardware checks and locates the bootloader.

2. **Bootloader:** The bootloader (e.g., GRUB) is a program that allows the user to choose an operating system to boot. It also loads the kernel into memory.

---

3. **Kernel Loading:** The kernel (e.g., vmlinuz) is loaded into memory. It initializes hardware, mounts the root filesystem, and starts the init process.

4. **Init Process:** The init process (or its replacement) is the first process started by the kernel. It initializes the system and starts essential system services.

### Boot Flags

Boot flags are parameters passed to the bootloader or kernel during startup to modify its behavior. They can affect aspects such as boot modes, hardware settings, and debugging options.

## System Shutdown

### Preparing for Shutdown

Before shutting down a system, it's important to:

- Save all open files and applications.
- Stop running services and applications.
- Ensure backups are up to date.

---

### Terminating Processes and User Sessions

To gracefully terminate processes and user sessions:

- Use the `kill` command to send signals to processes. For example: `kill PID` or `killall process_name`.
- Use the `logout` command or press `Ctrl + D` to exit a user session.

### Shutting Down and Rebooting

To shut down or reboot the system:

- Use the `shutdown` command to schedule a system shutdown with optional parameters. Example: `sudo shutdown -h now` (Immediate shutdown).
- Use the `reboot` command to restart the system. Example: `sudo reboot`.
