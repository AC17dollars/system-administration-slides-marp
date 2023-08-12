---
marp: true
paginate: true
author: Abhinav Chalise, Saugat Neupane
headingDivider: 2
footer: 2023-08-13
header: Abhinav Chalise, Saugat Neupane
---

# Setting up Operational Environment for a New User

## Role of a System Administrator

A system administrator is required to set up the operational environment for a new user due to the need for specialized privileges and expertise. System administrators have the necessary permissions to configure system-wide settings, manage software installations, and ensure security measures are implemented. General users do not possess these administrative rights and may inadvertently make changes that impact the system's stability or security.

## Creating and Configuring User Account

1. **Creating User Account:** Use the `adduser` or `useradd` command to create a new user account.

   Example: `sudo adduser newuser`

2. **Assigning Password:** Set a password for the new user using the `passwd` command.

   Example: `sudo passwd newuser`

---

3. **Adding to a Group:** Assign the user to a specific group, such as `general_user`.

   Example: `sudo usermod -aG general_user newuser`

4. **Granting Sudo Permissions:** To provide sudo permissions, add the user to the `sudo` group.

   Example: `sudo usermod -aG sudo newuser`

## Installing Applications and Packages

Install required applications using package managers:

- **APT (Debian/Ubuntu):** `sudo apt install package_name`
- **YUM (RHEL/CentOS):** `sudo yum install package_name`
- **Pacman (Arch Linux):** `sudo pacman -S package_name`
- **Flatpak:** `flatpak install package_name`
- **AppImage:** Download the AppImage and make it executable: `chmod +x appimage_file`

## User Environment Setup

- **Desktop Shortcuts:** Create shortcuts for commonly used applications on the user's desktop.
- **Default Applications:** Set default applications for file types using the system settings.
- **Shells:** Configure the user's shell. Install additional shells with package managers if needed.

## Profile Configuration

- Configure shell profiles like `.bashrc`, `.zshrc`, and other desktop and path configurations.
- Install and configure additional tools like `gitconfig`, `vimrc`, and other user-specific settings.

## Permissions

Define user permissions based on their role and requirements:

- Limit access to critical system files and directories.
- Grant read/write permissions to specific folders the user needs access to.

## Network and System Access

- Set up SSH keys for secure remote access.
- Configure GPG keys if encryption and authentication are required.
- Provide access to network resources, printers, and the internet.
- Install a browser for internet access.

## Documentation and Development Environment

- Ensure access to man pages for documentation (`man` command).
- Install development tools like GCC, text editors (Vim, Emacs, Nano), and IDEs (VSCode) if needed.
- Set up a comprehensive development environment with necessary libraries and tools.
