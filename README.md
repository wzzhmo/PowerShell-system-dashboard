PowerShell System Dashboard

A customized PowerShell terminal setup for Windows, featuring Fastfetch system information, custom ASCII art, and a clean Windows Terminal configuration.

Built as my first PowerShell / GitHub project while learning and experimenting with terminal customization.

Preview

✨ Features

* 🖥️ System information using Fastfetch
* 🎨 Custom Windows Terminal configuration
* 🌙 Catppuccin-inspired terminal theme
* 🐚 Customized PowerShell profile
* 🖼️ Custom ASCII art
* ⚡ Fastfetch automatically runs when PowerShell starts
* 🪶 Lightweight and simple setup
* 🛠️ Easy to customize

📁 Project Structure

PowerShell-system-dashboard/
│
├── Fastfetch/
│   └── hmod/
│       ├── config.jsonc
│       └── hm.txt
│
├── PowerShell/
│   ├── Terminal
│   └── micro
│
├── finalresult.png
└── README.md

📋 Requirements

Before installing, make sure you have:

* Windows
* Windows Terminal
* PowerShell
* Fastfetch

Fastfetch can be installed using winget:

winget install fastfetch

🚀 Installation

1. Configure Windows Terminal

Open Windows Terminal and go to:

Settings → Open JSON file

Make a backup of your current settings.json first.

Then copy the configuration from:

PowerShell/Terminal

and add it to your Windows Terminal configuration.

⚠️ Be careful when replacing your existing settings.json. Creating a backup first is recommended.

⸻

2. Create the PowerShell Profile

Open PowerShell and run:

New-Item -Path $PROFILE.CurrentUserAllHosts -Type File -Force

This creates your PowerShell profile if it doesn’t already exist.

⸻

3. Install Fastfetch

If you haven’t installed Fastfetch yet:

winget install fastfetch

You can verify the installation with:

fastfetch

⸻

4. Create the Fastfetch Configuration Folder

Create the following folder:

%USERPROFILE%\.config\fastfetch

The final structure should look like:

%USERPROFILE%\
└── .config\
    └── fastfetch\
        ├── config.jsonc
        └── hm.txt

Copy these files from the repository:

Fastfetch/hmod/config.jsonc
Fastfetch/hmod/hm.txt

into your Fastfetch folder.

⸻

5. Update Your Username

Open:

config.jsonc

and make sure the path to hm.txt points to your own user directory.

For example:

C:/Users/YourUsername/.config/fastfetch/hm.txt

Replace YourUsername with your Windows username.

⸻

6. Configure the PowerShell Profile

Open your PowerShell profile:

notepad $PROFILE

Copy the contents of:

PowerShell/micro

into your PowerShell profile.

Make sure the Fastfetch configuration path matches your own username/path.

⸻

▶️ Test It

Close and reopen Windows Terminal.

When PowerShell starts, Fastfetch should automatically display your system information and the custom dashboard.

If it doesn’t work, try running:

fastfetch

to make sure Fastfetch itself is installed correctly.

🎨 Customization

You can customize the dashboard by editing:

Fastfetch/hmod/config.jsonc

You can also replace:

Fastfetch/hmod/hm.txt

with your own ASCII art.

The Windows Terminal appearance can be customized from:

PowerShell/Terminal

🧹 Uninstall

To remove the customization, simply remove the changes made to:

* Your PowerShell profile
* Your Windows Terminal settings.json
* %USERPROFILE%\.config\fastfetch

Your original Windows Terminal configuration can be restored from the backup you created before installation.

🤝 Contributing

This is a personal learning project, but suggestions and improvements are welcome.

If you find a bug or have an idea for improving the project, feel free to open an Issue or Pull Request.

❤️ Credits

Built with:

* PowerShell
* Windows Terminal
* Fastfetch

Thanks for checking out my project!

If you like it, ⭐ consider giving the repository a star.

⸻

Made with ❤️ and PowerShell
