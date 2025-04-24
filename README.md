# C# Windows Form Application: SafeNet System

## Overview

Welcome to the SafeNet System Windows Forms application! SafeNet is a lightweight Windows Forms application that creates a secure, locked environment on a Windows machine. It disables access to essential system functionalities, including Task Manager, keyboard shortcuts (e.g., Ctrl+Alt+Del, Alt+Tab, WinKey), and desktop interaction, until the correct password is entered.

This tool can be used to simulate kiosk-mode behavior or as a simple educational project for understanding Windows security, registry manipulation, and system hooks in C#.

## Features

### Disables Task Manager via Windows Registry edits
### Blocks system-level shortcuts like:
- Ctrl + Alt + Del
- Alt + Tab
- WinKey
- Ctrl + Esc

### Hides the Windows taskbar and desktop icons
### Unlocks system access only when the correct password is 
### Password is securely stored in a file (safenet.pass) and validated at runtime

## How It Works
- When the application launches:

### 1. System Access is Locked:
- Task Manager is disabled.
- Windows key, Alt+Tab, and other escape shortcuts are blocked.
- Desktop icons and the taskbar are hidden.
- The form appears without borders, taking over the screen.

### 2. Login Prompt:
- A password prompt appears.
- The password is checked against the contents of safenet.pass.

### 3. On Correct Password:
- Task Manager is re-enabled.
- Desktop icons and taskbar are restored.
- Application exits, returning full control to the user.

## Default Password
- The file safenet.pass should contain your password on a single line.
Default password: "password"
**Warning: Do not use this tool in production or shared environments without further security hardening.**

## How to Use
1. Clone or download the repository.
2. Open the project in Visual Studio.
3. Build and run the project.
4. A password prompt will appear. Use the default password or modify safenet.pass before launching.
5. After entering the correct password, the system is unlocked.

## Disclaimer
This project is intended for educational use only. Improper use of system-level hooks or registry modifications can lead to a poor user experience or even lock you out of your system. Use with caution and always test in a controlled environment.

