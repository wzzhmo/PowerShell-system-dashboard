PowerShell System Dashboard

A simple PowerShell setup for Windows using Fastfetch and Windows Terminal.

I made this project to customize my PowerShell and display my system information when the terminal starts.

Preview

Features

* Fastfetch system information
* Custom ASCII art
* Custom PowerShell profile
* Windows Terminal customization
* Catppuccin theme
* Fastfetch starts automatically

Requirements

* Windows
* PowerShell
* Windows Terminal
* Fastfetch

Install Fastfetch with:

winget install fastfetch

Installation

1. Windows Terminal

Open Windows Terminal:

Settings → Open JSON file

Make a backup of your settings.json, then copy the settings from:

PowerShell/Terminal

into your Windows Terminal settings.

2. PowerShell Profile

Open PowerShell and run:

New-Item -Path $PROFILE.CurrentUserAllHosts -Type File -Force

Then open the profile:

notepad $PROFILE

Copy the contents of:

PowerShell/micro

into your profile.

3. Fastfetch

Create this folder:

%USERPROFILE%\.config\fastfetch

Then copy:

Fastfetch/hmod/config.jsonc
Fastfetch/hmod/hm.txt

into it.

Open config.jsonc and change the path to hm.txt to match your Windows username.

For example:

C:/Users/YourUsername/.config/fastfetch/hm.txt

4. Done

Restart Windows Terminal.

Fastfetch should now start automatically with PowerShell.

Customization

You can change the Fastfetch settings in:

Fastfetch/hmod/config.jsonc

You can also change the ASCII art in:

Fastfetch/hmod/hm.txt

Uninstall

Remove the changes from:

* PowerShell profile
* Windows Terminal settings.json
* %USERPROFILE%\.config\fastfetch

Built With

* PowerShell
* Windows Terminal
* Fastfetch

Made with ❤️ and PowerShell.
